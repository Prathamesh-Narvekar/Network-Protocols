# HTTP AND HTTPS

## What is HTTP?
- HTTP (HyperText Transfer Protocol) is the foundation of data communication on the web. It defines how messages are formatted and transmitted between:
  - Client (usually a web browser)
  - Server (where the website or resource resides)
- When you type a URL like http://example.com, your browser uses HTTP to request data from the server.

## Key Characteristics of HTTP
- Protocol Type: Application layer protocol (OSI Model).
- Port: Default is 80.
- Stateless: Each request is independent; the server does not retain session info by default.
  - <i>Stateless means: When you send a request to a website (like opening a page), the server treats it as a completely new request. It doesn’t remember what you did before.
      - Example:
        - You visit a shopping site and add an item to your cart.
        - If the site uses plain HTTP (stateless), the server won’t remember your cart unless extra mechanisms (like cookies or sessions) are used.
    - So, each request is independent, and the server doesn’t keep track of your previous actions by default.</i>
- Plain Text Transmission: Data is sent in clear text, making it vulnerable to interception.

## What is HTTPS?
- HTTPS (HyperText Transfer Protocol Secure) is the secure version of HTTP. It uses SSL/TLS encryption to protect data during transmission.
- When you visit https://example.com, the communication between your browser and the server is encrypted.

## Key Characteristics of HTTPS
- Protocol Type: HTTP + SSL/TLS.
- Port: Default is 443.
- Encrypted Communication: Prevents eavesdropping and tampering.
- Authentication: Uses digital certificates to verify the server’s identity.
- Integrity: Ensures data is not altered during transmission.

## How HTTPS Works (Step-by-Step)
- Client Hello: Browser requests a secure connection.
- Server Hello: Server responds with its SSL/TLS certificate.
- Certificate Verification: Browser checks if the certificate is valid and trusted.
- Key Exchange: Browser and server agree on encryption keys.
- Secure Communication: All data is encrypted using symmetric encryption.

## Difference Between HTTP and HTTPS


| Aspect            | HTTP                                   | HTTPS                                  |
|-------------------|----------------------------------------|----------------------------------------|
| **Security**      | No encryption (data in plain text)    | Encrypted using SSL/TLS               |
| **Port**          | 80                                    | 443                                    |
| **Data Integrity**| Vulnerable to tampering              | Ensures integrity                     |
| **Authentication**| None                                  | Server identity verified via certificate |
| **Performance**   | Slightly faster (no encryption)      | Slight overhead due to encryption     |
| **SEO Impact**    | Neutral                               | Preferred by search engines (ranking boost) |
| **Use Case**      | Non-sensitive data                   | Sensitive data (login, payments)      |
