# Basic Router Configuration Lab

## Purpose
In this lab, I focused on building the foundational configuration required for a new router. My goal was to practice initial setup tasks such as securing access, assigning interface addresses, and preparing the device for management and future network integration.

## Topology Overview
This lab uses a single router connected to a switch to highlight basic device initialization. The setup demonstrates hostname configuration, password protection, interface activation, and essential management settings.

## Key Configurations
- Setting the hostname and securing privileged EXEC mode
- Configuring console and VTY line access
- Assigning IP addresses to router interfaces
- Enabling basic management features
- Saving the running configuration to ensure persistence

## Verification Commands
show running-config  
show ip interface brief  
show version  
show users  

## Troubleshooting Notes
I verified that all interfaces were configured correctly, confirmed that passwords were applied to the proper lines, and ensured that the router booted with the expected startup configuration. I also checked for inactive interfaces and corrected any missing IP assignments.
