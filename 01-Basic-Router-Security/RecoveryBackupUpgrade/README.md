# Login Recovery, Backup, and Upgrade Lab

## Purpose
In this lab, I focused on recovering router access when passwords are lost, as well as performing basic backup and upgrade tasks. My goal was to understand how to regain control of a device and maintain its software and configuration safely.

## Topology Overview
This lab uses a single router connected through a console session to demonstrate password recovery, configuration backup, and IOS image management.

## Key Configurations
- Entering ROMMON mode for password recovery
- Resetting the configuration register
- Backing up the running configuration
- Managing IOS images and verifying file integrity
- Restoring normal boot behavior

## Verification Commands
show version  
show flash:  
show startup-config  
show running-config  

## Troubleshooting Notes
I confirmed that the router successfully bypassed the startup configuration during recovery, validated that the new passwords worked, and ensured that the device booted from the correct IOS image after upgrades.
