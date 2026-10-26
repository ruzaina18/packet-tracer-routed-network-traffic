# Packet Tracer: Observe Traffic Flow in a Routed Network

## Project Overview
This Cisco Packet Tracer lab demonstrates the difference between an unrouted LAN and a network divided into multiple IPv4 subnets. It explores how ARP broadcasts behave before and after routing is introduced between departmental networks.

## Objectives
- Observe ARP broadcasts in a single LAN.
- Analyze Ethernet frames and IP packets.
- Reconfigure a network to route between department subnets.
- Observe DHCP address renewal.
- Compare broadcast traffic before and after network segmentation.
- Understand the benefits of subnetting in an enterprise network.

## Tools and Technologies
- Cisco Packet Tracer
- IPv4 addressing and subnetting
- ARP (Address Resolution Protocol)
- DHCP (Dynamic Host Configuration Protocol)
- ICMP (Internet Control Message Protocol)
- Ethernet switching and IP routing

## Network Scenario
XYZ LLC initially operates a single LAN shared by the Accounting, Finance, and Sales departments. The network is redesigned to place departments on separate IPv4 networks connected through an Edge router.

### Initial Network
All departments share the `192.168.1.0/24` network.

### Redesigned Network
The intended addressing plan is:
- Accounting: `192.168.1.0/24`
- Finance: `192.168.2.0/24` (verify against the completed activity)
- Sales: `192.168.3.0/24` (verify against the completed activity)

The Edge router routes traffic between these networks and provides connectivity toward the ISP.

## Tasks Performed
1. Inspected the ARP cache on Sales 1.
2. Generated ARP requests by pinging another host.
3. Observed broadcast traffic in Simulation Mode.
4. Connected departmental switches to router interfaces.
5. Renewed DHCP addresses on Finance and Sales hosts.
6. Inspected ARP broadcasts after subnetting.
7. Compared traffic flow before and after routing.

## Key Findings

### Unrouted LAN
- ARP requests use the Ethernet broadcast address `FFFF.FFFF.FFFF`.
- Devices in the same broadcast domain receive the ARP broadcast.
- A large shared broadcast domain creates unnecessary network overhead.

### Routed Network
- Each department has its own IPv4 subnet.
- Routers separate broadcast domains by default.
- ARP broadcasts remain within their local Layer 2 broadcast domain.
- Inter-subnet communication requires routing through the gateway.
- Subnetting can improve traffic management, scalability, and security policy enforcement.

## OSI Model Concepts
- Layer 2 — Ethernet frames, MAC addresses, switching, and ARP.
- Layer 3 — IPv4 addressing, subnetting, and routing.
- Layer 4 — ICMP-based connectivity testing is used to verify reachability.

## Skills Demonstrated
- ARP and broadcast analysis
- IPv4 subnetting fundamentals
- DHCP troubleshooting
- Router and switch connectivity
- ICMP ping testing
- Enterprise network segmentation
- Packet Tracer Simulation Mode analysis

## Evidence
Add screenshots of:
- The original network topology.
- The ARP request and its broadcast destination MAC.
- The reconfigured routed topology.
- DHCP-renewed IP addresses.
- The ARP request after network segmentation.
- Successful connectivity tests.

## Conclusion
This lab demonstrates how separating departments into different IPv4 networks limits unnecessary broadcast traffic and enables communication through a router. Network segmentation improves manageability and can support better security when combined with appropriate access-control policies.

## Disclaimer
This project is a simulated learning exercise in Cisco Packet Tracer and does not represent a production enterprise deployment.
