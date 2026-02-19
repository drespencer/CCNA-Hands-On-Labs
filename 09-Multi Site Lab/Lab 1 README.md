Multi‑Site VLAN Configuration with Trunking, Access Ports, SVIs, and Routed Interfaces
Purpose
This lab focuses on building a complete switching foundation across three sites using VLAN segmentation, trunking, access‑port configuration, SVIs, and routed interfaces. The goal is to create a consistent Layer‑2 and Layer‑3 design that supports management, user, server, voice, and wireless networks across a multi‑switch enterprise environment.

Topology Overview
The environment includes three sites with different switching requirements:

Site 1 uses a distribution switch and multiple access switches to support VLANs for management, users, and servers.

Site 2 uses a single switch supporting management, user, and voice VLANs.

Site 3 uses three switches supporting management, user, and WLAN/voice VLANs.

Inter‑switch links operate as trunks to carry all VLANs, while endpoint‑facing ports operate in access mode. Layer‑3 switches in Site 1 host SVIs to provide default gateways and inter‑VLAN routing.

Key Configurations
VLAN creation across all switches according to site‑specific assignments.

Trunk ports configured between switches to carry all VLANs.

Access ports assigned to the correct VLANs for PCs, servers, IP phones, APs, and WLCs.

Voice VLANs configured where required using switchport voice vlan.

SVIs created on Layer‑3 switches in Site 1 to provide gateway addresses for VLANs 10, 11, and 12.

Routed ports configured using no switchport for uplinks requiring Layer‑3 forwarding.

Verification
I validated the configuration by confirming:

All VLANs were created and active.

Trunk and access ports were assigned correctly.

SVIs were up with proper IPv4 addressing.

Routed ports were operational.

Inter‑switch VLAN propagation and endpoint connectivity behaved as expected.
