# ACLs Lab

## Purpose
In this lab, I worked on configuring standard and extended ACLs to control traffic flow. My goal was to understand how ACLs filter packets, where to place them, and how they impact network behavior.

## Topology Overview
This lab uses routers and switches connected across multiple subnets to demonstrate ACL placement, direction, and filtering logic.

## Key Configurations
- Creating standard and extended ACLs
- Applying ACLs to interfaces in the correct direction
- Filtering traffic based on source, destination, and protocol
- Testing permitted and denied traffic flows

## Verification Commands
show access-lists  
show ip interface  
show running-config  
ping and traceroute tests  

## Troubleshooting Notes
I confirmed that ACLs were applied to the correct interfaces and directions, validated that legitimate traffic was allowed, and ensured that unwanted traffic was successfully blocked.
