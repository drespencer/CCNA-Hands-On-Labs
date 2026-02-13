# EtherChannel Lab

## Purpose
In this lab, I worked on bundling multiple physical links into a single logical interface using EtherChannel. My goal was to improve redundancy and bandwidth while ensuring consistent switchport configurations.

## Topology Overview
This lab uses two switches connected with multiple parallel links to demonstrate LACP and PAgP channel formation.

## Key Configurations
- Configuring LACP or PAgP channel groups
- Ensuring matching switchport settings across member interfaces
- Verifying port-channel creation and status
- Testing load balancing across bundled links

## Verification Commands
show etherchannel summary  
show interfaces port-channel <id>  
show interfaces switchport  

## Troubleshooting Notes
I checked for mismatched configurations that prevent channel formation and confirmed that the port-channel interface was operational. I also validated that traffic flowed correctly across the aggregated links.
