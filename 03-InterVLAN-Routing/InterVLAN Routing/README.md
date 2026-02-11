# Inter-VLAN Routing Labs

## Purpose
These labs focus on enabling communication between VLANs using router-on-a-stick and troubleshooting multi-VLAN environments.

## Topology Overview
A router connects to a multilayer switch using subinterfaces. Multiple VLANs are configured across access switches.

## Key Configurations
- Router-on-a-stick subinterfaces
- Encapsulation dot1Q settings
- Default gateway assignments
- Inter-VLAN troubleshooting

## Verification Commands
- show ip interface brief
- show interfaces g0/0.<subinterface>
- show vlan brief
- ping between VLANs

## Troubleshooting Notes
I diagnosed issues such as missing encapsulation, incorrect IP addressing, and gateway misconfigurations that prevented inter-VLAN communication.
