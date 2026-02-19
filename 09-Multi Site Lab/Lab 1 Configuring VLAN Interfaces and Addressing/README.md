Lab 1 – Configuring VLANs, Interfaces, and Addressing
Purpose
This lab walked through the foundational Layer 2 and Layer 3 setup for a multi‑switch environment across three sites. The focus was on creating VLANs, configuring trunk and access ports, and bringing up SVIs and routed ports. The goal was to build clean segmentation, predictable switch behavior, and a functional Layer 3 edge for inter‑VLAN communication.

Topology Overview
The environment included multiple 2960/3650 switches across Site 1, Site 2, and Site 3. Each site had its own VLAN design:

Site 1: VLANs 10 (Mgmt), 11 (Users), 12 (Servers)

Site 2: VLANs 2 (Mgmt), 22 (Users), 222 (Voice)

Site 3: VLANs 3 (Mgmt), 33 (Users), 133 (Voice/WLAN)

Switch roles were split between distribution and access layers, with trunks interconnecting switches and access ports mapped to endpoints like PCs, servers, phones, APs, and WLCs.

From the document:

“Site 1 will host three VLANs for various purposes on four separate switches…”
“To pass VLAN traffic between switches, the connecting ports need to be configured as trunk ports…”

Key Configurations
VLAN Creation
I created VLANs on all switches according to the site‑specific tables. Each VLAN was named and saved to the startup config.
Examples from the document:

“vlan 10
name Management”
“vlan 12
name Servers”

Trunk Ports
Trunks were configured on all inter‑switch links using switchport mode trunk.
When required, I enabled dot1q encapsulation to override auto‑negotiation.
This ensured all VLANs could traverse the uplinks cleanly.

Access Ports
Access ports were assigned to the correct VLANs based on the endpoint they served.
Examples included:

PCs in VLAN 11 or 33

Servers in VLAN 12

Voice ports using switchport voice vlan 222

APs and WLCs in VLAN 133

SVIs (VLAN Interfaces)
On SW1‑1 through SW1‑4, I created SVIs for VLANs 10, 11, and 12.
Each SVI received its assigned IPv4 address and mask, then was brought up with no shutdown.

From the document:

“interface vlan 10
ip address 192.168.10.1 255.255.255.0
no shutdown”

Routed Ports
The lab introduced routed ports later in the task, converting switch interfaces to Layer 3 mode where needed.
This allowed the distribution switches to participate in routing rather than relying solely on SVIs.

Verification Commands
Throughout the lab, I used these commands to confirm the configuration:

show vlan brief — verified VLAN creation and port assignments

show interfaces trunk — confirmed trunk status

show ip interface brief — checked SVI and routed port states

copy running-config startup-config — saved progress after each major step

The document repeatedly emphasized verification:

“Verify that the configuration has succeeded by using the command show vlan brief.”

Troubleshooting Notes
A few operational reminders stood out during the lab:

SVIs stay down until at least one access or trunk port in that VLAN is up.

Some switches require switchport trunk encapsulation dot1q before allowing trunk mode.

Voice VLANs must use the switchport voice vlan command, not switchport access vlan.

Default dynamic port behavior (DTP auto) can cause unexpected trunking unless explicitly set.
