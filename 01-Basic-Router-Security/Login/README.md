# Login Security Lab

## Purpose
In this lab, I focused on securing login access to the router. My goal was to understand how to protect console and VTY lines, enforce proper authentication, and prevent unauthorized access to device management.

## Topology Overview
This lab uses a single router connected through console and remote access methods to highlight password protection, login behavior, and secure access control.

## Key Configurations
- Setting console and VTY line passwords
- Enforcing login authentication on all management lines
- Configuring local user accounts for secure access
- Applying service password‑encryption for added protection
- Testing login behavior through console and remote sessions

## Verification Commands
show running-config  
show line vty 0 4  
show users  
show login  

## Troubleshooting Notes
I verified that all management lines required authentication, confirmed that passwords were encrypted, and tested both console and remote logins to ensure access was properly restricted. I also checked for leftover default or unsecured access methods.
