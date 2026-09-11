---
name: entergram-triage-chat-to-ticket
description: Triage an active Telegram chat into a tracked Entergram ticket, leaving an internal comment and assigning it.
api: Entergram Public API
base_url: https://api.entergram.com
auth: X-API-Key header (REST) or OAuth2 bearer (MCP)
operations:
  - list-chats
  - get-chat
  - list-chat-messages
  - create-chat-comment
  - create-ticket
  - update-ticket
  - list-chat-linked-tickets
---

# Triage a Telegram chat into a ticket

Turn an active Telegram conversation into a trackable Entergram ticket.

## Steps

1. **Find the chat.** `GET /v1/chats` (`list-chats`), optionally filtering with `search`, `chat_type`
   or `account_id`. Confirm details with `GET /v1/chats/{chat_id}` (`get-chat`).
2. **Read recent context.** `GET /v1/chats/{chat_id}/messages` (`list-chat-messages`) with an
   `account_id`; page with `before_message_id` / `limit`.
3. **Check for an existing ticket.** `GET /v1/chats/{chat_id}/tickets` (`list-chat-linked-tickets`)
   so you do not duplicate one.
4. **Create the ticket.** `POST /v1/tickets` (`create-ticket`) with the linked chat, a title/summary,
   `priority`, and `assignedToId` for the owning member.
5. **Leave an internal note.** `POST /v1/chats/{chat_id}/comments` (`create-chat-comment`) recording
   why the chat was escalated — this is workspace-internal and never sent to the Telegram user.
6. **Update as it progresses.** `PATCH /v1/tickets/{ticket_id}` (`update-ticket`) to change status,
   priority or assignee.

## Conventions

- Errors are RFC 9457 `application/problem+json`; on `422` inspect `errors[]` for field-level detail.
- Respect `429` responses — back off using the `Retry-After` header.
- Requires `chats.read`, `chats.write`, `tickets.read`, `tickets.write` scopes on the MCP path.
