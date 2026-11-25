Secure Multi-VLAN Enterprise Branch Network

Project Overview

This project demonstrates the design, configuration, implementation, and verification of a secure enterprise branch network using Cisco Packet Tracer.

The network is designed to provide departmental segmentation, controlled inter-VLAN communication, automated IP address allocation, simulated internet connectivity, and secure network device management.

Network Topology

The network consists of a Cisco 2911 branch router, a Cisco 2960 Layer 2 switch, a Cisco 1941 ISP router, fifteen end-user PCs distributed across four departments, and one public server.

The topology diagram is available in the topology folder, and the complete Packet Tracer project is included in this repository.

VLAN and IP Addressing

The network uses VLAN 10 for HR with the network 192.168.10.0/28 and gateway 192.168.10.1.

VLAN 20 is assigned to Sales with the network 192.168.10.16/28 and gateway 192.168.10.17.

VLAN 30 is assigned to IT with the network 192.168.10.32/28 and gateway 192.168.10.33.

VLAN 40 is assigned to Guest with the network 192.168.10.48/29 and gateway 192.168.10.49.

VLAN 99 is used for network management with the network 192.168.10.56/29 and gateway 192.168.10.57.

VLAN 999 is configured as the unused native VLAN without an IP address.

Network Configuration

Router-on-a-stick is implemented to provide inter-VLAN routing. VLSM is used for efficient IP address allocation, and DHCP is configured to automatically assign addresses to end-user devices.

Static routing provides connectivity between the branch network and the simulated ISP network. NAT/PAT enables internal departmental networks to access the simulated public network.

Extended access control lists are configured to restrict Guest VLAN access to internal network resources while allowing access to the public network.

Network Security

SSH version 2 is configured for secure remote management of the router and switch. Switch access ports use sticky MAC address port security with a maximum of one secure MAC address per port and restrict-mode violation handling.

PortFast and BPDU Guard are enabled on endpoint-facing switch ports. Unused switch ports and the unused router interface are administratively shut down. The trunk link uses VLAN 999 as its native VLAN.

Testing and Verification

The network was tested through DHCP lease verification, inter-VLAN connectivity tests, switch management connectivity, Guest VLAN access restrictions, and public server connectivity.

SSH access to the router and switch was verified. NAT/PAT operation and switch port-security status were also checked through Cisco IOS verification commands.

Tools and Technologies

Cisco Packet Tracer was used to build and simulate the network. Cisco IOS CLI was used for device configuration and verification. GitHub is used to document and showcase the project.

Project Status

The core network configuration and verification have been completed. This project is a practical demonstration of enterprise branch networking, VLAN segmentation, routing, addressing, network security, and troubleshooting.