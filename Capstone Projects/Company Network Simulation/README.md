Company Network Simulation – Packet Tracer Lab

Overview
This lab demonstrates a segmented enterprise network built in Cisco Packet Tracer. The design includes: A Trusted Internal LAN for employee workstations. DMZ hosting the company’s public web server. An Untrusted Internet segment simulating external users. A Gateway Router providing DHCP, routing, and NAT. A DNS + Web Server hosting www.company.com. An External Client accessing the company website from the Internet.

***The goal is to show end‑to‑end connectivity between internal hosts, DMZ services, and external users.***

Topology Summary
The network is divided into three security zones:

1. Internal LAN – 192.168.1.0/24 (Trusted)

  PC0

  PC1
  
  Switch0 (2960)
  
  Router0 G0/0 (Default Gateway: 192.168.1.1)

3. DMZ – 10.0.0.0/24 (Protected Server Network)

  Server0 (Web + DNS) – 10.0.0.10
  
  Switch1 (2960)
  
  Router0 G0/1 (10.0.0.1)

5. Internet – 8.8.8.0/24 (Untrusted)

  Router1 (ISP) – 8.8.8.1
  
  Access Point (Layer‑2 AP)
  
  Laptop0 (External Client) – 8.8.8.50

7. Router‑to‑Router Link

  Router0 S0/0/0 – 200.0.0.1
  
  Router1 S0/0/0 – 200.0.0.2

Device List

  Device Type	Quantity	Purpose

  Routers (2911)	2	Gateway + ISP

  Switches (2960)	2	LAN + DMZ
  
  Access Point	1	Wireless Internet client
  
  PCs	2	Internal clients
  
  Laptop	1	External Internet client
  
  Server	1	Web + DNS

IP Addressing Plan

Internal LAN

Device	IP	Notes

  Router0 G0/0	192.168.1.1	Default gateway
  
  PC0	DHCP	Assigned by Router0
  
  PC1	DHCP	Assigned by Router0

DMZ

Device	IP	Notes

  Router0 G0/1	10.0.0.1	DMZ gateway
  
  Server0	10.0.0.10	Web + DNS

Internet

Device	IP	Notes

  Router1 G0/0	8.8.8.1	Internet gateway
  
  Laptop0	8.8.8.50	Static external client

Router Link
  
  Device	IP
  
  Router0 S0/0/0	200.0.0.1
  
  Router1 S0/0/0	200.0.0.2

Router0 Configuration (Gateway Router)


interface g0/0
  
  ip address 192.168.1.1 255.255.255.0
  
  no shutdown

interface g0/1
  
  ip address 10.0.0.1 255.255.255.0
  
  no shutdown

interface s0/0/0
  
  ip address 200.0.0.1 255.255.255.252
  
  clock rate 64000
  
  no shutdown

DHCP for Internal LAN
  
  ip dhcp pool INTERNAL
  
  network 192.168.1.0 255.255.255.0
  
  default-router 192.168.1.1
  
  dns-server 10.0.0.10
 
Default Route to ISP
  
  ip route 0.0.0.0 0.0.0.0 200.0.0.2

NAT Overload (PAT)

  access-list 1 permit 192.168.1.0 0.0.0.255
  
  ip nat inside source list 1 interface s0/0/0 overload
  
  interface g0/0  
  
  ip nat inside
  
  interface s0/0/0

  ip nat outside

Router1 Configuration (ISP)

  Interfaces
  
  interface g0/0
  
  ip address 8.8.8.1 255.255.255.0
  
  no shutdown

interface s0/0/0
  
  ip address 200.0.0.2 255.255.255.252
  
  no shutdown
  
Static Routes Back to Company
  
  ip route 10.0.0.0 255.255.255.0 200.0.0.1
  
  ip route 192.168.1.0 255.255.255.0 200.0.0.1

Server Configuration (Web + DNS)

IP Settings

  IP: 10.0.0.10
  
  Mask: 255.255.255.0
  
  Gateway: 10.0.0.1
  
  DNS Records

Name |	Type |	Value

company.com |	A |	10.0.0.10

www.company.com |	CNAME |	company.com

HTTP Service

HTTP: ON

Custom index.html page created

External Access Point Configuration

Connected to Router1 G0/0 via LAN port

DHCP: OFF

Acts as a Layer‑2 wireless bridge

Laptop0 Static IP

  IP: 8.8.8.50
  
  Mask: 255.255.255.0
  
  Gateway: 8.8.8.1
  
  DNS: 10.0.0.10

Verification

1. Internal Clients Ping Each Other

  ping 192.168.1.2; 192.168.1.3

2. Internal Clients Access Web Server

  Browser:
  
  http://www.company.com

3. External Client Access Web Server

  Laptop browser:
  
  http://www.company.com

4. DNS Resolution

  ping company.com
  
  ping www.company.com

5. End‑to‑End Connectivity

  ping 10.0.0.10
  
  ping 8.8.8.1


Lessons I Learned:

How to segment networks using LAN, DMZ, and Internet zones

How to configure DHCP, DNS, NAT, and static routing

How to host a public web server in a DMZ

How to simulate external Internet access in Packet Tracer

How to use an Access Point as a simple wireless bridge

Files Included

Company_Network.pkt (Packet Tracer file)

README.md (This documentation)

Screenshots from the Lab
