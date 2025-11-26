# IMAP

## What is IMAP?
IMAP is an email protocol used by clients (like Outlook, Gmail, Thunderbird) to retrieve and manage emails stored on a mail server. Unlike POP3, IMAP keeps emails on the server and allows you to sync across multiple devices.

## Key Characteristics
- Protocol Type: Application layer protocol.
- Default Ports:
  - 143 → IMAP (unencrypted)
  - 993 → IMAP over SSL/TLS (secure)
- Transport Protocol: Uses TCP for reliable communication.
- Direction: Incoming mail only (receiving and managing emails).

## How IMAP Works
- Email arrives at the mail server (via SMTP).
- Client connects to the server using IMAP.
- Emails remain on the server; the client downloads copies or headers.
- Actions (read, delete, move) are synced across all devices because changes happen on the server.

## Features of IMAP
- Multi-device support: Perfect for smartphones, laptops, and webmail.
- Folder management: Create, rename, and organize folders on the server.
- Partial download: Download headers first, full message later.
- Synchronization: Keeps all devices updated.

## IMAP Commands
- IMAP uses text-based commands like:
  - LOGIN → Authenticate user.
  - SELECT → Choose a mailbox (folder).
  - FETCH → Retrieve messages.
  - STORE → Change message flags (read/unread).
  - LOGOUT → End session.
 
## Advantages
- Emails stay on the server → accessible from anywhere.
- Great for multiple devices.
- Supports advanced features like folders and flags.

## Disadvantages
- Requires constant internet connection.
- Uses more server storage.
