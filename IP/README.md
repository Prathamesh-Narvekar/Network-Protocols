## IP (INTERNET PROTOCOL) 

<div align = center>
	<img width="611" height="322" alt="IP_Protocol" src="https://github.com/user-attachments/assets/c0845819-1176-4164-b60f-c8980c1e6e3a" />
</div>

## What is IP?
IP (Internet Protocol) is responsible for addressing and routing packets between devices across networks. It ensures that data sent from one device reaches the correct destination.  
**Key Concepts**
- IP Address: A unique identifier for each device on a network (e.g., 192.168.1.1).
- IPv4 vs IPv6:
	- IPv4: 32-bit, written as four decimal numbers (e.g., 192.168.0.1)
	- IPv6: 128-bit, written in hexadecimal (e.g., 2001:0db8:85a3::8a2e:0370:7334)
- Routing: IP works with routers to forward packets across networks.
- Connectionless: IP doesn’t guarantee delivery — it just sends packets.

## Real-World Analogy
Think of IP like a postal system. Each device has an address, and IP ensures the packet (letter) gets routed through various hubs (routers) to reach the destination.

## Cisco Packet Tracer Simulation: IP Routing
- Open Packet Tracer
- Add two routers, two switches, and four PCs (two per network)
- Connect PCs to switches, switches to routers
- Assign IPs:
	- Network 1: 192.168.1.0/24
		- PC0: 192.168.1.10
		- PC1: 192.168.1.11
	- Network 2: 192.168.2.0/24
		- PC2: 192.168.2.10
		- PC3: 192.168.2.11
- Configure routers:
	- Assign IPs to router interfaces
	- Enable routing (static or dynamic like RIP)
- Test connectivity:
	- Ping from PC0 to PC2
	- If routing is correct, you’ll get replies
 - Optional: IPv6 Setup
	- Assign IPv6 addresses to PCs and routers
	- Use ping with IPv6 format

## Key Takeaways
- IP is essential for identifying and locating devices on a network.
- Routers use IP to forward packets between networks.
- IPv4 is still dominant, but IPv6 is growing due to address exhaustion.
- Packet Tracer lets you visualize IP routing and test connectivity.
