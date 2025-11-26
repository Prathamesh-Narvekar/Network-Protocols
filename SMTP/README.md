# SMTP

## What is SMTP?
SMTP (Simple Mail Transfer Protocol) is the standard protocol used to send emails across the Internet. It works at the application layer of the OSI model and is responsible for sending, relaying, and forwarding email messages from a client (like Outlook or Gmail) to a mail server and then to the recipient’s mail server.

 ## Key Characteristics
- Protocol Type: Application layer protocol.
- Default Ports:
  - Port 25 → Traditional SMTP (server-to-server relay).
  - Port 587 → Submission port (modern email clients use this).
  - Port 465 → SMTP over SSL (deprecated but still used).
- Transport Protocol: Uses TCP for reliable delivery.
- Direction: Sending emails only (receiving is handled by POP3 or IMAP).

## How SMTP Works (Step-by-Step)
- Mail Composition
  - User writes an email in a client (e.g., Gmail, Outlook).
- Mail Submission
  - The client connects to the SMTP server (e.g., smtp.gmail.com) on port 587.
- Mail Transfer
  - SMTP server forwards the email to the recipient’s mail server using SMTP.
- Mail Delivery
  - Recipient’s server stores the email, which can be retrieved via POP3 or IMAP.

## SMTP Commands
- SMTP uses text-based commands:
  - HELO or EHLO → Identify the client to the server.
  - MAIL FROM: → Sender’s email address.
  - RCPT TO: → Recipient’s email address.
  - DATA → Start sending the message body.
  - QUIT → End the session.

## SMTP VS POP3 VS IMAP

| Aspect            | SMTP (Simple Mail Transfer Protocol) | POP3 (Post Office Protocol v3)        | IMAP (Internet Message Access Protocol) |
|-------------------|---------------------------------------|----------------------------------------|-------------------------------------------|
| **Purpose**       | Sending emails                      | Receiving emails (download & delete) | Receiving & managing emails (sync)       |
| **Direction**     | Outgoing mail only                  | Incoming mail only                   | Incoming mail only                        |
| **Default Ports** | 25, 587 (submission), 465 (SSL)     | 110 (or 995 for SSL)                 | 143 (or 993 for SSL)                      |
| **Storage**       | Not applicable                      | Downloads emails to client, removes from server | Keeps emails on server, syncs with client |
| **Security**      | STARTTLS or SSL/TLS for encryption  | SSL/TLS for secure retrieval         | SSL/TLS for secure retrieval              |
| **Use Case**      | Sending mail from client to server or server to server | Simple email download               | Advanced email management across devices  |
 
## Summary:
SMTP = Send mail protocol, works with POP3/IMAP for receiving. Modern email systems use SMTP + TLS + Authentication for security.
