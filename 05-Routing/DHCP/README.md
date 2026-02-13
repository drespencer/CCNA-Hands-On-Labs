# DHCP Lab

## Purpose
In this lab, I focused on configuring DHCP services on a router. My goal was to understand how IP addresses, gateways, and DNS settings are assigned dynamically.

## Topology Overview
This lab uses a router acting as a DHCP server for a connected LAN.

## Key Configurations
- Creating DHCP pools
- Setting default gateways and DNS servers
- Excluding reserved addresses
- Testing address assignment from clients

## Verification Commands
show ip dhcp binding  
show ip dhcp pool  
show running-config  

## Troubleshooting Notes
I verified that clients received correct IP settings, checked for overlapping exclusions, and confirmed that the DHCP service was enabled.
