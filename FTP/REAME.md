# FTP (FILE TRANSFER PROTOCOL)

## What is FTP?
FTP (File Transfer Protocol) is a standard network protocol used to transfer files between a client and a server over a TCP/IP network (like the Internet or a local network). It’s one of the oldest protocols for file sharing.

## Key Characteristics
- Protocol Type: Application layer protocol (OSI Model).
- Default Ports:
  - Port 21 → Control connection (commands)
  - Port 20 → Data transfer (in active mode)
- Transport Protocol: Uses TCP for reliable communication.
- Purpose: Uploading, downloading, and managing files on remote servers.

## How FTP Works
- FTP uses two separate channels:
  - Control Channel (Port 21): For sending commands (e.g., login, list files).  
  - Data Channel (Port 20 or negotiated): For transferring actual file data.

 ## Modes of FTP
- Active Mode:
  - Client connects to the server on Port 21 (control channel).
  - When a file transfer is needed, the client tells the server: “I’m listening on port X, please connect to me.”
  - The server initiates the data connection from its Port 20 to the client’s chosen port.
  - Problem: Firewalls often block incoming connections to the client, so the server cannot connect back. This causes failures in modern networks.
- For Better Understanding:
  - Active Mode = The Server is the Delivery Guy
    - You (the client) call the pizza shop (FTP server) and place an order (control connection on port 21).
    - The shop says: “Okay, I’ll deliver the pizza to your house. Tell me your address and keep your door open.”
    - You give them your address (your port number), and then wait for them to come to you.
    - Problem? If your apartment has security guards (firewall) who don’t allow strangers in, the delivery guy (server) can’t reach you.
    - Result: Pizza never arrives!  

- Passive Mode:
  - Client connects to the server on Port 21 (control channel).
  - When a file transfer is needed, the server tells the client: “I’m listening on port Y, please connect to me.”
  - The client initiates the data connection to the server’s chosen port.
  - Advantage: Works better with firewalls because the client initiates both connections (control and data), avoiding blocked incoming connections.
- For Better Understanding:
  - Passive Mode = You Go Pick Up the Pizza
    - You (the client) call the pizza shop and place an order (control connection on port 21).
    - The shop says: “Great! I’ll be waiting at counter number 123 (random port). Come and pick it up.”
    - You go to the shop and collect your pizza (you initiate the data connection).
    - No security issues because you are allowed to go out.
    - Result: Pizza delivered successfully!
      
## Authentication
- Anonymous FTP: No login required (public file access).
- Authenticated FTP: Requires username and password.

## Security Concerns
- Plain Text Transmission: Usernames, passwords, and data are sent unencrypted.
- Vulnerable to sniffing and attacks.
- Solution: Use FTPS (FTP Secure) or SFTP (SSH File Transfer Protocol) for encryption.

## Common FTP Commands
- ftp hostname → Connect to FTP server.
- ls → List files.
- get filename → Download file.
- put filename → Upload file.
- bye → Exit FTP session.

## Advantages
- Simple and widely supported.
- Good for transferring large files.

## Disadvantages
- Insecure by default.
- Requires additional configuration for firewalls.

## FTP vs SFTP vs FTPS

| Aspect            | FTP                                   | SFTP (SSH File Transfer Protocol)       | FTPS (FTP Secure)                        |
|-------------------|---------------------------------------|------------------------------------------|-------------------------------------------|
| **Protocol**      | File Transfer Protocol               | SSH-based protocol                      | FTP over SSL/TLS                         |
| **Encryption**    | None (plain text)                   | Yes (via SSH)                           | Yes (via SSL/TLS)                        |
| **Default Port**  | 21 (control), 20 (data)             | 22                                      | 21 + SSL/TLS                             |
| **Authentication**| Username & Password (plain text)    | Username/Password or SSH keys           | Username/Password with SSL/TLS           |
| **Security**      | Low (vulnerable to sniffing)        | High (strong encryption)                | High (strong encryption)                 |
| **Firewall Friendly** | Difficult (multiple ports)      | Easy (single port)                      | Moderate (requires multiple ports)       |
| **Use Case**      | Legacy file transfers               | Secure file transfers over SSH          | Secure file transfers for FTP-based systems |
| **Relevance Today**| Obsolete for sensitive data        | Widely used and recommended             | Used in enterprise environments           |
