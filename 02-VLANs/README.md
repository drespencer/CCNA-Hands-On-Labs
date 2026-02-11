# VLAN Configuration Labs

## Purpose
In these labs, I built and verified VLAN segmentation across multiple switches. My goal was to create isolated broadcast domains and ensure proper trunking between switches.

## Topology Overview
The topology includes multiple access switches connected via 802.1Q trunks. End devices are placed in different VLANs to validate segmentation.

## Key Configurations
- Creating VLANs
- Assigning switchports to VLANs
- Configuring 802.1Q trunking
- Verifying VLAN propagation

## Verification Commands
- show vlan brief
- show interfaces trunk
- show mac-address-table
- show interfaces switchport

## Troubleshooting Notes
I resolved issues related to native VLAN mismatches, incorrect access port assignments, and trunk encapsulation errors.
