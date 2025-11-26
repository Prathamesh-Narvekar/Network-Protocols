# SSH

## What is SSH?
- SSH (Secure Shell) is a cryptographic network protocol used to securely connect to remote systems over an unsecured network. It provides:
  - Secure remote login
  - Command execution
  - File transfer
  - Tunneling and port forwarding
- SSH is the modern replacement for older insecure protocols like Telnet and rlogin.

## Key Features of SSH
- Encryption
  - All data (including passwords) is encrypted, preventing eavesdropping.
- Authentication
  - Password-based authentication
  - Public key authentication (more secure)
- Integrity
  - Ensures data is not altered during transmission.
- Confidentiality
  - Protects sensitive information from interception.

## Default Settings
- Port: 22
- Transport Protocol: TCP
- OSI Layer: Application Layer

## How SSH Works (Step-by-Step)
- Client initiates connection to the SSH server.
- Server sends its public key to the client.
- Client verifies the server’s identity (using known hosts).
- Key exchange happens to establish a secure session.
- Authentication:
  - Password OR
  - Public/Private key pair
- Secure channel established → Commands and data are encrypted.

## Advantages of SSH
- Strong encryption and security.
- Supports tunneling and port forwarding.
- Widely used for remote administration and automation.

## SSH vs Telnet
- SSH = Secure, encrypted, modern.
- Telnet = Insecure, plain text, obsolete.

## Summary
SSH is essential for secure remote access and is the industry standard for system administration, cloud servers, and DevOps.
