# TELNET

## What is TELNET?
TELNET (Telecommunication Network) is a network protocol that allows a user to remotely access and manage devices or servers over a TCP/IP network. It provides a command-line interface for communication with another machine.

## Key Characteristics
- Protocol Type: Application layer protocol (OSI Model).
- Default Port: 23.
- Purpose: Remote login and command execution.
- Transport Protocol: Uses TCP for reliable communication.
- Plain Text Transmission: Data (including usernames and passwords) is sent unencrypted, making it insecure.

## How TELNET Works
- You open a TELNET client and connect to a remote host (e.g., telnet example.com).
- The server responds, and you can enter commands as if you were physically at that machine.
- Communication happens in plain text, so anyone intercepting the traffic can read it.

## Why TELNET is Rarely Used Today
- Security Risk: No encryption → vulnerable to eavesdropping and attacks.
- Replaced by SSH: Secure Shell (SSH) provides encrypted remote access.

## Common Use Cases (Historically)
- Remote administration of servers.
- Testing network services.
- Accessing text-based applications.

## Difference between TELNET and SSH

| Aspect            | TELNET                                  | SSH (Secure Shell)                      |
|-------------------|-----------------------------------------|-----------------------------------------|
| **Purpose**       | Remote login and command execution     | Secure remote login and command execution |
| **Default Port**  | 23                                     | 22                                      |
| **Security**      | No encryption (plain text)            | Encrypted using SSH protocol (secure)   |
| **Authentication**| Basic username/password               | Strong authentication (password, keys)  |
| **Data Integrity**| Vulnerable to interception and tampering | Ensures integrity and confidentiality    |
| **Transport Protocol** | TCP                              | TCP                                     |
| **Use Case**      | Legacy systems, testing               | Modern remote administration, secure file transfer |
| **Relevance Today**| Obsolete due to security risks       | Widely used and recommended             |


## Summary:
TELNET = Remote access protocol, insecure, replaced by SSH for modern systems.

