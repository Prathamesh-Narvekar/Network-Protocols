## ARP (ADRESS RESOLUTION PROTOCOL)

<div align = center>
  <img width="803" height="460" alt="ARP_Protocol" src="https://github.com/user-attachments/assets/a6fa7644-05e0-4d22-b1e7-43132fbeaec1" />
</div>

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
