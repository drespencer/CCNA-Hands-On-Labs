# Port Security Lab

## Purpose
In this lab, I focused on securing switchports using port security. My goal was to understand how to limit access, prevent unauthorized devices from connecting, and enforce violation actions that protect the network edge.

## Topology Overview
This lab uses a switch with end‑user devices connected to access ports. The setup highlights how port security restricts MAC addresses and responds to violations.

## Key Configurations
- Setting switchports to access mode
- Enabling port security on specific interfaces
- Limiting the number of allowed MAC addresses
- Configuring sticky MAC learning
- Choosing violation actions such as protect, restrict, or shutdown

## Verification Commands
show port-security  
show port-security interface  
show running-config interface <id>  

## Troubleshooting Notes
I validated that the correct MAC addresses were learned, confirmed that violation actions triggered as expected, and ensured that unauthorized devices were blocked from gaining access.
