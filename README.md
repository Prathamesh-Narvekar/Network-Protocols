<h1>NETWORK PROTOCOLS</h1>
A network protocol is a set of rules that govern data communication between different devices in the network. It determines what is being communicated, how it is being communicated, and when it is being communicated. It permits connected devices to communicate with each other, irrespective of internal and structural differences.

<h2>ICMP (INTERNET CONTROL MESSAGE PROTOCOL) </h2>
<ul>
  <li>Concept: ICMP (Internet Control Message Protocol) is used for error reporting and diagnostics. Tools like ping and traceroute rely on it.</li>
  <li>Analogy: Think of ICMP like a postal service “delivery receipt” – it tells you if your letter (packet) reached the destination or not.</li>
  <li>Packet Tracer Lab:
    <ul>
      <li>Place 2 PCs in Packet Tracer.</li>
      <li>Connect them with a switch.</li>
      <li>Assign IP addresses (e.g., PC1: 192.168.1.1, PC2: 192.168.1.2).</li>
      <li>Use the ping command from PC1 to PC2.</li>
      <li>Observe ICMP Echo Request and Echo Reply.</li>
    </ul>
  </li>
  <li>Visual Guide: <a href="https://www.youtube.com/watch?v=ebL2JIGcYw0">You can follow this ICMP simulation tutorial on YouTube.</a></li>
	
  <li>Key Takeaway: ICMP doesn’t carry data—it just reports on the status of IP communication.
    <ul>
      <li>ICMP is essential for troubleshooting — it helps you know if devices are reachable.</li>
      <li>Ping uses ICMP Echo Request and Echo Reply.</li>
      <li>ICMP doesn’t carry user data, just control messages.</li>
      <li>You can simulate ICMP easily in Packet Tracer with basic topology.</li>
    </ul>
  </li>
</ul>

<h2>ARP (ADRESS RESOLUTION PROTOCOL)</h2>
<b>What Is ARP?</b>
<p>ARP (Address Resolution Protocol) is used to map an IP address to a MAC address. It operates at the boundary of the Network Layer (Layer 3) and the Data Link Layer (Layer 2) of the OSI model.</p>
<b>Why It Matters</b>
<p>When a device wants to send data to another device on the same network, it needs the destination’s MAC address. If it only knows the IP, it uses ARP to find the MAC.</p>
<b>How ARP Works</b>

1.	Host A wants to talk to Host B (knows IP, needs MAC).
2.	Host A sends an ARP Request: “Who has IP 192.168.1.2?”
3.	Host B replies with an ARP Reply: “192.168.1.2 is at MAC AA:BB:CC:DD:EE:FF.”
4.	Host A stores this in its ARP table and sends the data.

<b>Cisco Packet Tracer Simulation: ARP</b>
Lab Setup
1.	Open Packet Tracer
2.	Add two PCs and a switch
3.	Connect PCs to switch with copper straight-through cables
4.	Assign IPs:<ul><li>PC0: 192.168.1.1 / 255.255.255.0</li><li>PC1: 192.168.1.2 / 255.255.255.0</li></ul>
5.	Configure IPs via Desktop → IP Configuration
6.	Ping from PC0 to PC1 to trigger ARP
7.	View ARP Table:<ul><li>On PC0 → Desktop → Command Prompt → Type: arp -a</li><li>You’ll see PC1’s IP mapped to its MAC address</li></ul>

<p><b>Visual Demo:</b>  <a href="https://www.youtube.com/watch?v=lOaoDLxKuYI">You can follow this ARP simulation tutorial on YouTube.</a></p>
<b>Key Takeaways</b><ul>
	<li>ARP is essential for LAN communication — it bridges IP and MAC.</li>
	<li>It uses broadcast for discovery, reply is unicast.</li>
	<li>ARP tables cache mappings to avoid repeated requests.</li>
	<li>You can inspect ARP tables using arp -a in Packet Tracer.</li>
</ul>

