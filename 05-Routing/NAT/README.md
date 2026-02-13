# NAT Lab

## Purpose
In this lab, I practiced configuring NAT to translate private IP addresses into public ones. My goal was to understand static NAT, dynamic NAT, and PAT.

## Topology Overview
This lab uses a router between an internal LAN and an external network to demonstrate translation behavior.

## Key Configurations
- Configuring inside and outside interfaces
- Creating static NAT mappings
- Setting up PAT using overload
- Testing translations with internal hosts

## Verification Commands
show ip nat translations  
show ip nat statistics  
show running-config  

## Troubleshooting Notes
I confirmed that inside and outside interfaces were assigned correctly, validated translation entries, and ensured that ACLs matched the intended traffic.
