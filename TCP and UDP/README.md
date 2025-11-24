## TCP AND UDP 
### What is TCP (Transmission Control Protocol)? 
TCP is a connection-oriented protocol that ensures reliable, ordered, and error-checked delivery of data between applications.  
**Key Features:**
- Three-way handshake: Establishes a connection before data is sent (SYN → SYN-ACK → ACK).
- Reliable: Guarantees that all data arrives and in the correct order.
- Error checking: Detects and retransmits lost or corrupted packets.
- Flow control: Prevents overwhelming the receiver.
- Use Cases: Web browsing (HTTP/HTTPS), email (SMTP), file transfers (FTP), remote login (SSH).

### What is UDP (User Datagram Protocol)?
UDP is a connectionless protocol that sends data without establishing a connection, making it faster but less reliable.  
**Key Features:**
- No handshake: Just sends data — no setup or confirmation.
- Unreliable: No guarantee of delivery, order, or duplication protection.
- Lightweight: Minimal overhead, making it faster.
- Use Cases: Video streaming, online gaming, VoIP, DNS queries.

### TCP vs UDP: The Transport Layer Titans

| Feature | TCP(Transmission Control Protocol) | UDP(User Datagram Protocol) |
| --- | --- | --- |
| Connection | Connection-oriented (3-way handshake) | Connectionless |
| Reliability | Reliable (acknowledgments, retransmissions) | Unreliable (no guarantee of delivery) |
| Speed | Slower due to overhead | Faster, minimal overhead |
| Use Cases | Web (HTTP/HTTPS), Email (SMTP), File Transfer (FTP) | Streaming (video/audio), DNS, VoIP, Gaming |
| Ordering | Guarantees packet order | No ordering |
| Error Checking | Yes, with correction | Yes, without correction |

### Cisco Packet Tracer Simulation: TCP vs UDP
- Add two PCs and a server
- Connect them via a switch
- Assign IPs:
	- PC0: 192.168.1.10
	- Server: 192.168.1.100
- Configure Services on Server:
	- Enable HTTP (uses TCP)
	- Enable TFTP (uses UDP)
- On PC0:
	- Use Web Browser to access http://192.168.1.100 → observe TCP behavior
	- Use TFTP client to upload/download a file → observe UDP behavior
- Use Simulation Mode:
	- Filter by TCP and UDP
	- Watch how TCP establishes a connection (SYN, SYN-ACK, ACK)
	- See how UDP sends data without handshake

### Key Takeaways
- TCP = Reliable, Ordered, Slower
- UDP = Fast, Lightweight, Unreliable
- Use TCP when accuracy matters, UDP when speed is critical
- Packet Tracer lets you visualize the handshake and packet flow

