# RIP Lab

## Purpose
In this lab, I practiced configuring RIP and observing how distance‑vector routing behaves. My goal was to understand hop count metrics, split horizon, and route advertisement behavior.

## Topology Overview
This lab uses multiple routers connected in a simple topology to demonstrate RIP updates, timers, and route propagation.

## Key Configurations
- Enabling RIP and advertising networks
- Observing periodic updates
- Testing route learning and hop count limits
- Configuring version 2 for subnet support

## Verification Commands
show ip rip database  
show ip protocols  
show ip route rip  

## Troubleshooting Notes
I validated that all routers used the same RIP version, checked for missing network statements, and confirmed that routes were not filtered by split horizon.
