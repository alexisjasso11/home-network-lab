# Home Network Lab — Proxmox / pfSense / Managed Switch

## Lab Summary
Built a physical and virtualized home network lab to gain hands-on experience with real-world networking concepts including network segmentation, firewall management, and infrastructure troubleshooting.

## Hardware Used
![Lenovo](https://img.shields.io/badge/Lenovo_ThinkCentre-E2231A?style=for-the-badge&logo=lenovo&logoColor=white)
![Netgear](https://img.shields.io/badge/Netgear-FF6600?style=for-the-badge&logo=netgear&logoColor=white)
- Mini PC (M625Q)
  - Proxmox hypervisor to host pfSense VM
- Managed 8 port switch (GS308E)
  - Configured VLANs and trunking to connect and segment devices
- Laptop (ThinkPad)
  - Managed pfSense firewall dashboard via HTTPS web interface as well as Netgear switch via HTTPS web interface

## Software & Tools
![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![pfSense](https://img.shields.io/badge/pfSense-212121?style=for-the-badge&logo=pfsense&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
- Proxmox VE — hypervisor and virtual machine management
- pfSense — firewall, routing, and DHCP management
- VLANs and trunking configured via managed switch

## What I Built & Configured
- Deployed multiple virtual machines across segmented VLANs
### Network Topology
![Network Diagram](network_topology.png)
- Configured pfSense firewall rules to control inter-VLAN traffic
- Set up DHCP scopes per VLAN for automatic IP assignment
- Implemented trunking between switch and pfSense for VLAN routing
- Diagnosed and resolved various connectivity issues across the environment

## Troubleshooting & Challenges

### Static IP Configuration for pfSense Web Interface Access
- Encountered multiple connectivity issues when attempting to access the 
  pfSense web interface via HTTP from laptop
- Diagnosed the issue through various methods but
  concluded with static IP assignment
- Resolved by manually configuring a static IP address on the 
  ThinkPad to match the correct subnet of the pfSense LAN interface
- Ensured the static IP was outside the DHCP scope to avoid 
  address conflicts on the network
- Successfully accessed the pfSense dashboard via HTTP after 
  correct static IP configuration
- Learned the importance of proper IP addressing and subnet 
  alignment when managing network devices through a web interface

## What I Learned
Gained practical understanding of how enterprise networks are structured, how traffic flows between segments, and how firewalls enforce security policies at the network level. This directly maps to concepts tested in CompTIA Security+ and foundational cloud networking in Azure and AWS.
