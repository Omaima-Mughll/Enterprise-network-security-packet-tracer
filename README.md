# Enterprise Network Security Design — Cisco Packet Tracer
**Tool:** Cisco Packet Tracer

## Overview
A three-site enterprise network (Branch Office A, Branch Office B, and a Head Office/Data Center with a dedicated DMZ) designed and 
built in Cisco Packet Tracer around **Zero Trust principles**. Every zone is segmented by VLAN and subnet, admin access requires 
authenticated SSH from a restricted management subnet, the DMZ is isolated from the internal LAN by firewall policy, and inbound WAN traffic 
is denied by default except for the specific services required (HTTP, FTP, SMTP, POP3). This project presents the design and implementation of a secure enterprise network using Cisco Packet Tracer.
The network is designed to represent a realistic enterprise environment consisting of a Head Office, Branch Offices, internal network segments, 
servers, routing infrastructure, and security controls.
The main objective of this project is to demonstrate how networking and security technologies can be combined to build a reliable, segmented, and secure enterprise network.

## Network Architecture:
- **Branch Office A** — Router, Switch, DHCP server, App server, 3 client PCs, 4 department VLANs (HR/IT/Finance/Servers)
- **Branch Office B** — Same layout as Branch A, linked to HQ via a Site-to-Site GRE tunnel
- **Head Office / Data Center** — Router, Cisco ASA Firewall, Internal LAN, DMZ (Web/FTP/Email servers)
- **ISP Router** — Interconnects all three sites, running OSPF

## Network Components
- Head Office
- Branch A
- Branch B
- Cisco Routers
- Cisco Switches
- ASA Firewall
- VLANs
- DHCP Server
- DNS Server
- Web Server
- FTP Server
- Email Server
- PCs and network devices

## Security Features
- VLAN segmentation
- Access Control Lists (ACLs)
- NAT
- ASA Firewall
- SSH for secure device management
- Port Security
- Network segmentation
- Controlled access between network zones

## Network Services
- DHCP
- DNS
- HTTP
- FTP
- Email
- SSH
  
## Key Features
- Zero Trust architecture: VLAN/subnet segmentation, SSH-only admin access, and default-deny inbound policy across every zone.
- Three-site topology: Branch Office A, Branch Office B, and a Head Office/Data Center with a dedicated DMZ, linked through an ISP transit router.
- VLSM/CIDR IP addressing: 16 subnets sized precisely, from /30 point-to-point links to /24 department LANs.
- OSPF dynamic routing: Single-area OSPF across all sites, with HQ's static routes redistributed network-wide.
- Core network services: DHCP, local DNS, HTTP, FTP, and SMTP/POP3 configured and verified end-to-end.
- Cisco ASA firewall and NAT: Default-deny inbound ACLs, static NAT for DMZ publishing, and dynamic PAT for internal clients.
- Site-to-Site GRE tunnel: Secure branch-to-HQ connectivity.
- Layer 2 hardening: Port security with sticky MAC, shutdown-on-violation, and all unused ports disabled.
- Inter-VLAN access control: ACLs blocking direct HR to Finance traffic while preserving normal routing.
- Transparent documentation: Real Packet Tracer simulator limitations root-caused and explained, not hidden.

## VLAN and Network Segmentation:
VLANs are used to logically separate different departments and network segments.
Network segmentation helps reduce unnecessary communication between different groups and provides an additional layer of security.
The project demonstrates communication between authorized VLANs while using security controls to restrict unwanted traffic.

## Routing:
Routing is configured to provide communication between different network segments and locations.
Dynamic routing is used where appropriate to allow routers to exchange network information and maintain connectivity between different
parts of the enterprise network.

## Network Services:
Several network services are configured as part of the enterprise environment.

### DHCP:
DHCP is used to automatically assign IP addresses and other network configuration information to client devices.

### DNS:
DNS is configured to resolve hostnames to IP addresses and provide name resolution for network services.

### Web Server:
A web server is configured to demonstrate access to an enterprise-hosted web service.

### FTP Server:
An FTP server is configured to provide file transfer functionality within the network.

### Email Server:
An email server is configured to demonstrate enterprise email communication.

## Network Security:
Security is an important component of this project.
Several security mechanisms are implemented to protect the network and control access between different network segments.
Security controls include:
- VLAN-based network segmentation
- Access Control Lists (ACLs)
- Firewall rules
- Network Address Translation (NAT)
- Port security
- SSH-based remote management
- Restricted management access
- Separation of internal and external network traffic

These controls help reduce unauthorized access and limit unnecessary traffic between network segments.

## Remote Management:
SSH is configured for secure remote management of network devices.
Telnet is avoided for administrative access because SSH provides encrypted communication and is more appropriate for secure network management.

## Testing and Verification:
Network connectivity and services were tested using Cisco Packet
Tracer simulation and verification tools.
Testing includes:
- Ping tests between network segments
- VLAN connectivity verification
- Routing verification
- DHCP address assignment
- DNS name resolution
- NAT verification
- ACL and firewall behavior
- SSH connectivity
- Server accessibility

## Project Objectives
The main objectives of this project are:
1. Design an enterprise network topology.
2. Implement network segmentation using VLANs.
3. Configure routing between different networks.
4. Implement essential network services.
5. Apply security controls to protect network resources.
6. Configure secure remote management.
7. Test and verify network connectivity and services.

## Conclusion
This project demonstrates the practical implementation of an enterprise network with integrated networking and security technologies.
The combination of VLAN segmentation, routing, network services, firewall controls, ACLs, NAT, port security, and SSH provides a foundation 
for a more secure and manageable enterprise network.

## How to Open
1. Install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) (free with a Cisco Networking Academy account).
2. Open `TASK_06.pkt`.
3. Explore device configurations via each device's **CLI** tab, and inspect VLANs, routing tables, ACLs, NAT, and firewall rules directly in the simulator.
