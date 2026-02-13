# HSRP Lab

## Purpose
In this lab, I focused on configuring HSRP to provide gateway redundancy. My goal was to understand active/standby roles, priority settings, and failover behavior.

## Topology Overview
This lab uses two routers acting as redundant gateways for a VLAN, demonstrating HSRP group configuration and failover testing.

## Key Configurations
- Setting HSRP group numbers and virtual IPs
- Adjusting priorities and enabling preemption
- Testing failover by shutting down interfaces
- Verifying active and standby roles

## Verification Commands
show standby  
show standby brief  
show ip interface  

## Troubleshooting Notes
I validated that both routers participated in the same HSRP group, confirmed priority behavior, and ensured that clients used the virtual IP as their default gateway.
