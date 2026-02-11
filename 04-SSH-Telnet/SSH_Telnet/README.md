# SSH and Telnet Access Labs

## Purpose
In this set of labs, I configured secure remote access to network devices. My goal was to replace insecure Telnet access with SSH and enforce authenticated management sessions.

## Topology Overview
The topology includes routers and switches configured for local authentication and remote management.

## Key Configurations
- Enabling SSH version 2
- Generating RSA keys
- Configuring local user authentication
- Restricting VTY lines to SSH only
- Testing Telnet vs SSH behavior

## Verification Commands
- show ip ssh
- show running-config | section vty
- show users
- ssh -l <user> <ip>

## Troubleshooting Notes
I validated that Telnet was disabled, confirmed successful SSH authentication, and ensured that VTY access aligned with security best practices.
