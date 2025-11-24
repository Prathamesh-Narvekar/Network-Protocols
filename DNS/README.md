# DNS (DOMAIN NAME SYSTEM)
## What Is DNS?
DNS (Domain Name System) resolves domain names (like google.com) into IP addresses (like 142.250.190.14) so devices can locate each other on the internet or a local network.

## What happens when you make a DNS Request?
When you type a website name (like www.youtube.com) in your browser, your computer needs to find its IP address to connect. This process uses DNS (Domain Name System), which works like the internet's phonebook.
### 1. Check Your Computer's Cache
Your computer first checks if it already knows the IP address for that website from a previous visit.
- If yes → Done!
- If no → It asks a Recursive DNS Server.

### 2. Recursive DNS Server
This is usually provided by your ISP (Internet Service Provider), but you can use others like Google DNS or Cloudflare DNS.
- It also checks its own cache.
- If found → Sends it back to you.
- If not → It starts asking other servers.

### 3. Root DNS Servers
These are the top-level servers of the internet.
- They don’t know the exact IP, but they know where to look next.
- They point to the TLD (Top-Level Domain) server based on your domain ending (.com, .org, etc.).

### 4. TLD Server
This server knows which authoritative server is responsible for your domain (e.g., youtube.com).
- It gives the address of that authoritative server.
	
### 5. Authoritative DNS Server
This is the final source of truth for the domain.
- It has the actual DNS records (like IP address).
- Sends the answer back to the Recursive DNS Server.

### 6. Caching
The Recursive DNS Server saves this answer for a certain time (called TTL – Time To Live) so next time it’s faster.
Your computer also caches it.

## Why DNS Matters
- Humans remember names, not numbers.
- DNS automates the translation of names to IPs.
- Without DNS, you'd need to memorize IPs for every website or service.

## Real-World Analogy
Imagine calling a friend by name. Your phone uses a contact list (DNS) to find their number and make the call. DNS works the same way for computers.

## Cisco Packet Tracer Simulation: DNS Resolution
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
## Key Takeaways
- DNS resolves names to IPs, enabling user-friendly access to services.
- DNS servers store mappings and respond to client queries.
- Packet Tracer lets you simulate DNS resolution and test web access via domain names.
