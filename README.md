# Mairard — Character Registration Bot

Bot lives inside ticket channels. Players register their characters, an admin assigns the LCF or OCF role manually after reviewing.

---

## Setup

1. Invite the bot to your server
2. Run `/setup #channel` to set where logs go
3. That's it — no roles or channels to create

---

## How it works

1. Player opens a ticket via Ticket Tool
2. They run `/addchar` for each character inside the ticket
3. Each addition shows up in the log channel automatically
4. Admin assigns the LCF or OCF role manually
5. Ticket gets closed

---

## Player Commands

- `/addchar` — Add a character. Pick LCF or OCF, then fill in name, class and clan
- `/remove_char` — Pick a character from your list to remove
- `/my_chars` — See all your registered characters
- `/help` — Show available commands

---

## Admin Commands

- `/setup #channel` — Set the log channel
- `/admin_add @user` — Add a character for someone, auto-assigns their role
- `/admin_delete @user` — Pick one of a player's characters to remove
- `/admin_edit @user` — Edit a player's character details
- `/list` — Full character list split by LCF and OCF
- `/search [query]` — Search by name, clan or Discord user. Leave empty for full list
- `/deleted_chars` — See the last 50 removed characters with dates
- `/export` — Download all registrations as a CSV
- `/import_data` — Bulk import via CSV upload
- `/purge` — Wipes everything for this server. Asks for confirmation first

---

## Notes

- Deleted characters aren't gone — they stay in the database and show up in `/deleted_chars`
- Character names are unique per player (case-insensitive)
- The bot won't join servers it's not supposed to be in
