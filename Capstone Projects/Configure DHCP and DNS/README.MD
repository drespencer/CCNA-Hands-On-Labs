5.4.1 – Configure DHCP and DNS

Overview
In this lab, I explored how DHCP and DNS services operate inside a small LAN environment using Cisco Packet Tracer. I started by examining how clients behave when no DHCP server is available, then configured a DHCP scope to automatically assign IPv4 settings. Finally, I enabled DNS services and created A and CNAME records so clients could access a web server using friendly hostnames instead of IP addresses.

Objectives
Observe APIPA behavior when DHCP is unavailable
Configure a DHCP server with gateway, DNS, and address pool settings
Verify that clients receive correct IPv4 information from DHCP
Enable DNS services and create A and CNAME records
Test name resolution to access a web server by hostname

Topology
Client1 (DHCP client)
DHCP Server – 192.168.1.2
DNS Server – 192.168.1.3
Web Server – 192.168.1.4
Default Gateway – 192.168.1.1
All devices are connected on the 192.168.1.0/24 network.

Task Summary

Task A – Investigating APIPA
Client1 was configured for DHCP but received an APIPA address because no DHCP service was active.
Verified via ipconfig that the client self‑assigned a 169.254.18.48 address.
Confirmed the DHCP server had correct static settings but the DHCP service was turned off.

Task B – Configuring DHCP
I enabled DHCP and created a valid address pool:
Default Gateway: 192.168.1.1
DNS Server: 192.168.1.3
Start IP: 192.168.1.11
Max Users: 10

Service: On
After saving the configuration, Client1 successfully received:
A valid IPv4 address from the pool
Correct subnet mask
Gateway and DNS settings (grayed out because they’re DHCP‑assigned)

Task C – Configuring DNS
With DHCP working, I configured DNS so clients could reach the web server by name:
Verified the Web Server was reachable at 192.168.1.4
Enabled DNS service on the DNS server

Added the following records:

A Record:
Name: web
Address: 192.168.1.4

CNAME Record:
Name: www.company.com
Host: web

Client1 was then able to access:
http://web
http://www.company.com  

Verification Steps
Ran ipconfig on Client1 to confirm DHCP‑assigned settings
Successfully pinged devices across the LAN
Accessed the web server using both hostname and FQDN
Confirmed DNS resolution worked as expected

Lessons Learned
APIPA addresses indicate DHCP failure but allow limited local connectivity
DHCP scopes must include gateway and DNS information for full client functionality
DNS A records map hostnames to IPs, while CNAMEs provide aliasing
Properly configured DHCP + DNS dramatically improves usability in small networks

Files Included
5.4.1-Configure-DHCP-and-DNS.pkt (lab file)
Screenshots (if added)
This README.md
