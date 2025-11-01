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
  <li>Key Takeaway: ICMP doesn’t carry data—it just reports on the status of IP communication.
    <ul>
      <li>ICMP is essential for troubleshooting — it helps you know if devices are reachable.</li>
      <li>Ping uses ICMP Echo Request and Echo Reply.</li>
      <li>ICMP doesn’t carry user data, just control messages.</li>
      <li>You can simulate ICMP easily in Packet Tracer with basic topology.</li>
    </ul>
  </li>
</ul>
