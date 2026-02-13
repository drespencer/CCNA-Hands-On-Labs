# Syslog Lab

## Purpose
In this lab, I worked on configuring Syslog to centralize device logging. My goal was to understand how logs are generated, stored, and forwarded.

## Topology Overview
This lab uses a router sending logs to a Syslog server for monitoring and analysis.

## Key Configurations
- Setting the Syslog server IP
- Adjusting logging levels
- Enabling timestamps
- Testing log generation

## Verification Commands
show logging  
show running-config  
show clock  

## Troubleshooting Notes
I confirmed that logs were reaching the server, validated severity levels, and checked for connectivity issues between the router and the Syslog host.
