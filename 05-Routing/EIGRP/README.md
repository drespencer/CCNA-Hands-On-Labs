# EIGRP Lab

## Purpose
In this lab, I worked on configuring EIGRP and understanding how it uses metrics and the DUAL algorithm to select loop‑free paths. My goal was to practice neighbor formation, metric tuning, and route verification.

## Topology Overview
This lab uses a multi‑router setup to highlight EIGRP neighbor relationships, feasible successors, and metric calculations.

## Key Configurations
- Enabling EIGRP and advertising networks
- Verifying neighbor adjacency
- Observing feasible successors and topology entries
- Adjusting metrics to influence path selection

## Verification Commands
show ip eigrp neighbors  
show ip eigrp topology  
show ip route eigrp  
show ip protocols  

## Troubleshooting Notes
I checked for mismatched AS numbers, confirmed that interfaces were included in the EIGRP process, and validated that routes appeared correctly in the topology table.
