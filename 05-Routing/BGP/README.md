# BGP Lab

## Purpose
In this lab, I worked on configuring eBGP between autonomous systems. My goal was to understand neighbor formation, route advertisement, and basic path selection.

## Topology Overview
This lab uses routers in different ASNs to demonstrate eBGP peering, network advertisement, and next‑hop behavior.

## Key Configurations
- Establishing eBGP neighbor relationships
- Advertising networks into BGP
- Verifying BGP tables and best‑path selection
- Testing reachability across AS boundaries

## Verification Commands
show ip bgp summary  
show ip bgp  
show ip route bgp  

## Troubleshooting Notes
I checked for mismatched AS numbers, validated that neighbor IPs were reachable, and confirmed that advertised networks appeared in the BGP table.
