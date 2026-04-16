6.3.1 – Exploring NAT

Overview
In this lab, I explored how Network Address Translation (NAT) operates on Cisco routers by configuring Static NAT, Dynamic NAT, and Port Address Translation (PAT). I verified how internal private addresses are translated when accessing external networks and used packet captures to observe the NAT process in real time.

This lab demonstrates how NAT preserves public IPv4 address space while allowing internal hosts to reach external destinations.

Objectives
Examine traffic flow before NAT is configured
Configure Static NAT and verify translation
Configure Dynamic NAT with a pool
Configure PAT (overload) for multiple internal clients
Use Packet Tracer’s Sniffer tool to observe NAT behavior
Validate connectivity to external resources using IP and DNS names

Topology
Router1 – Inside NAT boundary
Router2 – Outside NAT boundary / Internet simulation
Client1 – Internal host
DNS Server – Provides name resolution for external sites
Sniffer1 / Sniffer2 – Capture packets before and after NAT
Internet1 – Simulated external web resource

(Topology image referenced in repo: 6.3.1 Lab Topology.png )

Task Breakdown
1. Baseline Testing (Before NAT)
Client1 attempted to reach external sites such as company.com and something.com.
DNS queries resolved, but traffic failed because private addresses were not routable on the outside network.
Sniffer tools showed packets leaving with internal source IPs, confirming NAT was not yet active.

2. Static NAT Configuration
On Router2, I mapped a single inside local address to an inside global address:

Code
ip nat inside source static <inside-local> <inside-global>
Verified translation using:

Code
show ip nat translations
show ip nat statistics
Sniffer1 captured packets showing the internal IP being rewritten to the static global address.

(Images: Router2 NAT Static Config.png, Sniffer1 packet to something.com.png )

3. Dynamic NAT Configuration
Configured a NAT pool and ACL to define which internal hosts were eligible for translation:

Code
ip nat pool NAT-POOL 209.165.200.225 209.165.200.230 netmask 255.255.255.248
access-list 1 permit 192.168.1.0 0.0.0.255
ip nat inside source list 1 pool NAT-POOL
Verified that internal hosts were assigned addresses from the pool.

Sniffer2 showed translated packets using different global addresses.

(Images: Router1 NAT Configuration.png, Sniffer2 network traffic to something.com.png )

4. PAT (NAT Overload) Configuration
Enabled PAT so multiple internal hosts could share a single public IP:

Code
ip nat inside source list 1 interface g0/0 overload
Observed unique port numbers being assigned to each translation.

Sniffer captures confirmed port‑level multiplexing.

(Images: Router2 NAT Configuration.png, Sniffer1 traffic to something.com after NAT Config.png )

5. Verification
Client1 successfully accessed external resources using both IP and DNS names.
DNS server resolved company.com and something.com correctly.
Internet1 responded to HTTP requests once NAT was active.
Translation tables populated as expected for Static NAT, Dynamic NAT, and PAT.

(Images: Client1 resolved to Company.com.png, Internet1 company.com site resolved.png )

Key Commands Used
Code
show ip nat translations
show ip nat statistics
debug ip nat
ip nat inside
ip nat outside
ip nat inside source static ...
ip nat inside source list ... pool ...
ip nat inside source list ... interface ... overload

Lessons Learned
NAT is essential for enabling private networks to communicate with external networks.
Static NAT provides one‑to‑one mapping, while Dynamic NAT uses a pool of addresses.
PAT is the most efficient method, allowing many internal hosts to share a single public IP.
Packet captures are extremely useful for visualizing how NAT rewrites source addresses and ports.
DNS resolution must work correctly for hostname‑based testing to succeed.

Files Included
NAT 6.3.1 Lab Completion Configuration.pkt
Packet captures and screenshots 
