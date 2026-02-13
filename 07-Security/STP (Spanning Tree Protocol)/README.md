# Spanning Tree Protocol (STP) Lab

## Purpose
In this lab, I focused on understanding how Spanning Tree Protocol prevents Layer 2 loops in redundant switch topologies. My goal was to see how STP selects a root bridge, assigns port roles, and stabilizes the network when multiple paths exist.

## Topology Overview
This lab uses a multi‑switch environment with intentional redundancy to highlight root bridge election, port state transitions, and how STP maintains a loop‑free topology.

## Key Configurations
- Adjusting bridge priority to influence root bridge selection
- Reviewing port roles such as root, designated, and alternate
- Observing STP convergence after link changes
- Validating how redundant links are blocked or forwarded

## Verification Commands
show spanning-tree  
show spanning-tree vlan <id>  
show interfaces status  
show running-config | section spanning-tree  

## Troubleshooting Notes
I confirmed which switch became the root bridge, validated that redundant links were placed into blocking or alternate states, and tested link failures to observe how quickly STP reconverged. I also checked for inconsistent port settings that could delay convergence.
