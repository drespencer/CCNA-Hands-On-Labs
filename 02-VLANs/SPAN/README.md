# SPAN (Switched Port Analyzer) Lab

## Purpose
In this lab, I focused on configuring SPAN to mirror traffic from one interface or VLAN to another. My goal was to understand how SPAN supports packet analysis, troubleshooting, and monitoring without disrupting normal switch operations.

## Topology Overview
This lab uses a simple switch topology with a defined source interface and a destination monitoring port. The design highlights how SPAN copies traffic for analysis tools like Wireshark.

## Key Configurations
- Selecting source interfaces or VLANs to monitor
- Assigning a destination port for mirrored traffic
- Ensuring the destination port is dedicated to monitoring only
- Verifying SPAN session status and behavior

## Troubleshooting Notes
I confirmed that the monitoring port was receiving mirrored traffic and verified that it wasn’t configured as an access or trunk port. I also checked for conflicting SPAN sessions and validated that only the intended traffic was being mirrored.
