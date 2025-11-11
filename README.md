# NETWORK PROTOCOLS
A **network protocol** is a set of rules that govern data communication between different devices in the network. It determines what is being communicated, how it is being communicated, and when it is being communicated. It permits connected devices to communicate with each other, irrespective of internal and structural differences.

## ICMP (INTERNET CONTROL MESSAGE PROTOCOL)
- Concept: ICMP (Internet Control Message Protocol) is used for error reporting and diagnostics. Tools like ping and traceroute rely on it.
- Analogy: Think of ICMP like a postal service “delivery receipt” – it tells you if your letter (packet) reached the destination or not.
- Packet Tracer Lab:
	- Place 2 PCs in Packet Tracer.
	- Connect them with a switch.
    - Assign IP addresses (e.g., PC1: 192.168.1.1, PC2: 192.168.1.2).
  	- Use the ping command from PC1 to PC2.
  	- Observe ICMP Echo Request and Echo Reply.
- Visual Guide: [Click Here](https://www.youtube.com/watch?v=ebL2JIGcYw0).
- Key Takeaway: ICMP doesn’t carry data—it just reports on the status of IP communication.
	- ICMP is essential for troubleshooting — it helps you know if devices are reachable.
	- Ping uses ICMP Echo Request and Echo Reply.
	- ICMP doesn’t carry user data, just control messages.
	- You can simulate ICMP easily in Packet Tracer with basic topology.

## ARP (ADRESS RESOLUTION PROTOCOL)
### What Is ARP?
ARP (Address Resolution Protocol) is used to map an IP address to a MAC address. It operates at the boundary of the Network Layer (Layer 3) and the Data Link Layer (Layer 2) of the OSI model.  

### Why It Matters
When a device wants to send data to another device on the same network, it needs the destination’s MAC address. If it only knows the IP, it uses ARP to find the MAC.  

### How ARP Works
1. Host A wants to talk to Host B (knows IP, needs MAC).
2. Host A sends an ARP Request: “Who has IP 192.168.1.2?”
3. Host B replies with an ARP Reply: “192.168.1.2 is at MAC AA:BB:CC:DD:EE:FF.”
4. Host A stores this in its ARP table and sends the data.

### Cisco Packet Tracer Simulation: ARP Lab Setup
- Open Packet Tracer
- Add two PCs and a switch
- Connect PCs to switch with copper straight-through cables
- Assign IPs:
     - PC0: 192.168.1.1 / 255.255.255.0
     - PC1: 192.168.1.2 / 255.255.255.0
- Configure IPs via Desktop → IP Configuration
- Ping from PC0 to PC1 to trigger ARP
- View ARP Table:
   - On PC0 → Desktop → Command Prompt → Type: arp -a
   - You’ll see PC1’s IP mapped to its MAC address

**Visual Demo: [Click Here](https://www.youtube.com/watch?v=lOaoDLxKuYI).**

### Key Takeaway
- ARP is essential for LAN communication — it bridges IP and MAC.
- It uses broadcast for discovery, reply is unicast.
- ARP tables cache mappings to avoid repeated request.
- You can inspect ARP tables using arp -a in Packet Tracer.


## IP (INTERNET PROTOCOL) 
### What is IP?
IP (Internet Protocol) is responsible for addressing and routing packets between devices across networks. It ensures that data sent from one device reaches the correct destination.  
**Key Concepts**
- IP Address: A unique identifier for each device on a network (e.g., 192.168.1.1).
- IPv4 vs IPv6:
	- IPv4: 32-bit, written as four decimal numbers (e.g., 192.168.0.1)
	- IPv6: 128-bit, written in hexadecimal (e.g., 2001:0db8:85a3::8a2e:0370:7334)
- Routing: IP works with routers to forward packets across networks.
- Connectionless: IP doesn’t guarantee delivery — it just sends packets.

### Real-World Analogy
Think of IP like a postal system. Each device has an address, and IP ensures the packet (letter) gets routed through various hubs (routers) to reach the destination.

### Cisco Packet Tracer Simulation: IP Routing
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

### Key Takeaways
- IP is essential for identifying and locating devices on a network.
- Routers use IP to forward packets between networks.
- IPv4 is still dominant, but IPv6 is growing due to address exhaustion.
- Packet Tracer lets you visualize IP routing and test connectivity.

## DNS (DOMAIN NAME SYSTEM)
### What Is DNS?
DNS (Domain Name System) resolves domain names (like google.com) into IP addresses (like 142.250.190.14) so devices can locate each other on the internet or a local network.

### Why DNS Matters
- Humans remember names, not numbers.
- DNS automates the translation of names to IPs.
- Without DNS, you'd need to memorize IPs for every website or service.

### Real-World Analogy
Imagine calling a friend by name. Your phone uses a contact list (DNS) to find their number and make the call. DNS works the same way for computers.

### Cisco Packet Tracer Simulation: DNS Resolution
- Add 2 PCs and 1 Server
- Connect all devices to a switch
- Assign IPs:
	- PC0: 192.168.1.10
	- Server: 192.168.1.100
- Configure Server:
	- Click Server → Services → DNS
	- Add a DNS entry: www.example.com → 192.168.1.100
- Configure PC0:
	- Desktop → IP Configuration
	- Set DNS Server to 192.168.1.100
- Test DNS:
	- PC0 → Desktop → Web Browser
	- Enter http://www.example.com
	- If DNS is working, the page loads from the server
- Optional Expansion
	- Add multiple DNS entries
	- Simulate DNS failure by removing the entry
	- Use Simulation Mode to observe DNS request and response packets
### Key Takeaways
- DNS resolves names to IPs, enabling user-friendly access to services.
- DNS servers store mappings and respond to client queries.
- Packet Tracer lets you simulate DNS resolution and test web access via domain names.



