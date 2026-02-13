# VTP Lab

## Purpose
In this lab, I explored how VTP distributes VLAN information across switches. My goal was to understand VTP modes, domain configuration, and how VLAN changes propagate through the network.

## Topology Overview
This lab uses a multi-switch topology with a designated VTP server and multiple clients to highlight VLAN synchronization.

## Key Configurations
- Setting the VTP domain name
- Configuring VTP server, client, and transparent modes
- Creating VLANs on the server and verifying propagation
- Checking revision numbers to confirm synchronization

## Troubleshooting Notes
I verified that all switches shared the same VTP domain and confirmed that VLANs created on the server appeared on the clients. I also checked for mismatched domain names and incorrect modes, which commonly break VTP synchronization.
