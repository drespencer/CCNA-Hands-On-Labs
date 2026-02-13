# PPP Lab

## Purpose
In this lab, I focused on configuring PPP on serial links and understanding how authentication works between routers. My goal was to get comfortable with PAP and CHAP, verify encapsulation, and see how PPP behaves on point‑to‑point WAN connections.

## Topology Overview
This lab uses two routers connected through a serial interface to demonstrate PPP encapsulation, authentication, and link negotiation.

## Key Configurations
- Setting PPP encapsulation on serial interfaces
- Configuring PAP or CHAP authentication
- Assigning IP addresses to serial links
- Verifying link negotiation and authentication success

## Verification Commands
show interfaces serial  
show ppp all  
show pppoe session  
show running-config  

## Troubleshooting Notes
I confirmed which router acted as the authenticator, validated that usernames and passwords matched correctly, and checked that the serial link reached an up/up state with PPP encapsulation.
