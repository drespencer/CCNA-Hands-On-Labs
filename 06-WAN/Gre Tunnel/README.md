# GRE Tunnel Lab

## Purpose
In this lab, I worked on building GRE tunnels between routers. My goal was to understand how GRE encapsulates traffic, supports routing protocols, and enables connectivity between remote networks.

## Topology Overview
This lab uses two routers connected over an intermediate network to demonstrate GRE tunnel creation, routing over tunnels, and end‑to‑end reachability.

## Key Configurations
- Creating tunnel interfaces
- Setting tunnel source and destination addresses
- Assigning IP addresses to tunnel interfaces
- Advertising tunnel networks through routing protocols

## Verification Commands
show interface tunnel  
show ip interface brief  
show ip route  
ping <remote-tunnel-ip>  

## Troubleshooting Notes
I verified that the tunnel endpoints were reachable, confirmed that the tunnel interface was up/up, and ensured that routing protocols recognized and used the tunnel path correctly.
