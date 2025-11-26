# POP3

## What is POP3?
POP3 is a standard email protocol used by email clients to retrieve emails from a mail server. It’s designed for downloading messages from the server to the client and then (usually) deleting them from the server.

## Key Characteristics
- Protocol Type: Application layer protocol.
- Default Port:
  - 110 → Standard POP3
  - 995 → POP3 over SSL/TLS (secure)
- Transport Protocol: Uses TCP for reliable communication.
- Direction: Incoming mail only (receiving emails).

## How POP3 Works
- Email arrives at the mail server (via SMTP).
- Client connects to the server using POP3.
- Client downloads emails to the local device.
- Emails are usually deleted from the server after download (though some clients allow keeping a copy).

## POP3 Commands
- POP3 uses simple text-based commands:
  - USER → Provide username.
  - PASS → Provide password.
  - STAT → Get mailbox status.
  - LIST → List messages.
  - RETR → Retrieve a message.
  - DELE → Delete a message.
  - QUIT → End session.
 
## Advantages
- Simple and lightweight.
- Works well for single-device email access.

## Disadvantages
- Not good for multiple devices (emails are removed from the server).
- Limited functionality (no folder sync, no advanced management).
- Insecure without SSL/TLS.

## POP3 vs IMAP

| Aspect            | POP3 (Post Office Protocol v3)       | IMAP (Internet Message Access Protocol) |
|-------------------|---------------------------------------|-------------------------------------------|
| **Purpose**       | Retrieve emails from server          | Retrieve and manage emails on server     |
| **Default Ports** | 110 (or 995 for SSL/TLS)             | 143 (or 993 for SSL/TLS)                 |
| **Storage**       | Downloads emails and usually deletes from server | Keeps emails on server, syncs with client |
| **Multi-Device Support** | Poor (emails stored locally)  | Excellent (sync across multiple devices) |
| **Folder Management** | Not supported                   | Supported (folders, labels)              |
| **Security**      | SSL/TLS for encryption               | SSL/TLS for encryption                   |
| **Use Case**      | Single-device email access           | Modern email clients and multi-device access |
| **Modern Usage**  | Rare (legacy systems)                | Common and recommended                   |
