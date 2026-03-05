# Secure OpenClaw Deployment on Azure

This project demonstrates how to securely deploy OpenClaw AI agents on Microsoft Azure using hardened infrastructure and security best practices.

The goal of this lab is to simulate how organizations can deploy AI agents while maintaining strong security controls and limiting attack surface exposure.

---

## Architecture Overview

Internet
   │
Azure Network Security Group (NSG)
   │
Restricted Admin Access (IP Allowlist)
   │
Windows Server 2025 VM
   │
Docker Runtime
   │
OpenClaw AI Agent Platform

---

## Security Controls Implemented

• IP restricted RDP access  
• Network Security Group firewall rules  
• Default deny inbound policy  
• Windows firewall enabled  
• Containerized runtime using Docker  

---

## Azure Infrastructure

The environment is deployed using Microsoft Azure Virtual Machines.

Configuration:

VM Size: Standard B2ms  
OS: Windows Server 2025  
Network: Azure Virtual Network  
Firewall: Network Security Group  

---

## Network Security Rules

| Priority | Rule | Purpose |
|--------|--------|--------|
|300|Allow RDP|Admin access|
|310|Allow HTTPS|Secure web access|
|320|Allow HTTP|Web testing|
|330|Allow ICMP|Ping troubleshooting|
|65500|Deny All|Block all other inbound|

Only the administrator IP address is allowed to connect.

---

## Installation Steps

1. Create Azure Virtual Machine
2. Configure Network Security Group rules
3. Restrict admin access to specific IP
4. Connect via RDP
5. Install Docker
6. Deploy OpenClaw containers
7. Verify service availability

---

## Security Considerations

Potential threats considered during deployment:

• Brute force RDP attacks  
• Unauthorized internet scanning  
• Container breakout attempts  
• Misconfigured firewall rules  

Mitigations:

• IP allowlist access
• Default deny inbound traffic
• Layered firewall protection

---

## Project Purpose

This project was created to demonstrate secure AI infrastructure deployment and serve as a reference for installing OpenClaw in cloud environments.

It also serves as a practical lab for learning AI platform security and cloud infrastructure hardening.

---
