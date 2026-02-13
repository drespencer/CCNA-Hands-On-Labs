# OSPF Lab

## Purpose
In this lab, I focused on building OSPF adjacencies and understanding how link‑state routing forms a complete view of the network. My goal was to practice area design, neighbor formation, and route verification.

## Topology Overview
This lab uses multiple routers connected through point‑to‑point and broadcast networks to demonstrate OSPF areas, DR/BDR behavior, and LSA propagation.

## Key Configurations
- Enabling OSPF and assigning networks to areas
- Adjusting interface priorities for DR/BDR elections
- Verifying neighbor adjacency states
- Observing OSPF routes and LSAs

## Verification Commands
show ip ospf neighbor  
show ip ospf interface  
show ip route ospf  
show ip protocols  

## Troubleshooting Notes
I validated that all routers shared the same area settings, checked for mismatched network statements, and confirmed that OSPF adjacencies reached the FULL state.
