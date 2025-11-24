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
