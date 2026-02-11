# Basic Router Security Labs

## Purpose
In this set of labs, I focused on foundational router hardening. My goal was to apply baseline security controls that protect device access, enforce authentication, and reduce exposure to common misconfigurations.

## Topology Overview
These labs use simple router and switch topologies designed to highlight secure management access, password protection, and remote access configuration.

## Key Configurations
- Securing console and VTY lines
- Enforcing encrypted passwords
- Configuring service password‑encryption
- Setting up login banners
- Restricting remote access methods

## Verification Commands
- show running-config
- show line vty 0 4
- show users
- show ip interface brief

## Troubleshooting Notes
I validated that insecure access methods were disabled, verified password protection on all management lines, and confirmed that remote sessions were authenticated correctly.
