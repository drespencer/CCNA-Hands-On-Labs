# Static Routing Lab

## Purpose
In this lab, I focused on configuring static and default routes. My goal was to understand how routers forward traffic when using manually defined paths.

## Topology Overview
This lab uses a multi‑router topology to demonstrate next‑hop routing, exit interfaces, and floating static routes.

## Key Configurations
- Creating static routes to remote networks
- Configuring default routes
- Using floating static routes for backup paths
- Testing reachability across multiple hops

## Verification Commands
show ip route  
show running-config  
ping <destination>  

## Troubleshooting Notes
I confirmed that next‑hop IPs were reachable, validated that static routes appeared in the routing table, and checked for administrative distance conflicts.
