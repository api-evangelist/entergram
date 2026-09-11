---
name: entergram-send-telegram-message
description: Send a Telegram message (text or media) to a chat through Entergram with idempotent retries.
api: Entergram Public API
base_url: https://api.entergram.com
auth: X-API-Key header (REST) or OAuth2 bearer (MCP)
operations:
  - list-accounts
  - list-chats
  - create-chat-message
  - create-chat-media-upload-tickets
  - upload-chat-media-bytes
  - create-chat-media-message
  - get-chat-message
---

# Send a Telegram message through Entergram

Send a text or media message from a connected personal Telegram account into a chat.

## Steps

1. **Pick the sending account.** `GET /v1/accounts` (`list-accounts`) and note the `accountId` of the
   connected Telegram account to send from.
2. **Locate the chat.** `GET /v1/chats` (`list-chats`) to resolve the target `chat_id`.
3. **Send text.** `POST /v1/chats/{chat_id}/messages` (`create-chat-message`) with `accountId`, `text`,
   and a client-supplied `idempotencyKey`. Reusing the same `idempotencyKey` on a retry prevents a
   duplicate send.
4. **Send media (three-step upload).**
   a. `POST /v1/chats/{chat_id}/messages/media/uploads` (`create-chat-media-upload-tickets`) with
      `accountId`, the file list, and an `idempotencyKey` — returns upload tickets.
   b. `PUT /v1/messages/media/uploads/{upload_id}` (`upload-chat-media-bytes`) to upload raw bytes,
      passing `X-File-Name` and `X-File-Content-Type`.
   c. `POST /v1/chats/{chat_id}/messages/media` (`create-chat-media-message`) to send the uploaded media.
5. **Confirm.** `GET /v1/chats/{chat_id}/messages/{message_id}` (`get-chat-message`).

## Conventions

- **Idempotency is partial** — the `idempotencyKey` body field protects `create-chat-message`,
  `create-chat-media-message`, `create-chat-media-upload-tickets` and `run-live-chat-command`. There is
  no global Idempotency-Key header.
- Errors are RFC 9457 `application/problem+json`. Handle `413` (payload too large) on media uploads and
  `429` (rate limited — honor `Retry-After`).
- Requires `messages.read` / `messages.write` scopes on the MCP path.
