# DHCP PROTOCOL

## What Is DHCP?
DHCP (Dynamic Host Configuration Protocol) is an application layer protocol that dynamically assigns IP addresses and other network settings (like subnet mask, default gateway, DNS) to devices when they join a network.
- Why DHCP Matters
  - Eliminates manual IP configuration
  - Prevents IP conflicts
  - Simplifies network management, especially in large networks

## Real-World Analogy: Hotel Reception Desk 🏨
Imagine checking into a hotel. You don’t choose your room number — the receptionist assigns one from the available pool. DHCP works the same way: when a device joins the network, the DHCP server assigns it an IP address from a predefined pool.

## Cisco Packet Tracer Simulation: DHCP Setup
- Setup with DHCP Server
  - Add a Server, Switch, and 2 PCs
  - Connect all devices via the switch
  - Assign static IP to the Server (e.g., 192.168.1.1)
  - Configure DHCP on Server:
    - Click Server → Services → DHCP
    - Enable DHCP
    - Set:
      - Default Gateway: 192.168.1.1
      - DNS Server: 192.168.1.1
      - Start IP: 192.168.1.10
      - Subnet Mask: 255.255.255.0
      - Maximum Users: 50
- Configure PCs:
  - Desktop → IP Configuration → Select “DHCP”
  - IP will be assigned automatically

## Key Takeaways
- DHCP automates IP assignment, reducing errors and saving time
- Can be configured on servers or routers
- Packet Tracer lets you simulate both methods and observe IP allocation
