# IP Addressing Plan

## Overview

This document defines the IPv4 addressing scheme used in the Small Office Network Design project.

The addressing plan separates infrastructure devices from client devices and reserves additional space for future expansion.

---

## Network Information

| Parameter | Value |
|-----------|-------|
| Network Address | 192.168.10.0/24 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.10.1 |
| DNS Server | 8.8.8.8 |

---

## Static IP Address Allocation

| Device | IP Address |
|---------|------------|
| Router | 192.168.10.1 |
| Switch | 192.168.10.2 |
| Wireless Access Point | 192.168.10.3 |
| Server | 192.168.10.10 |
| Network Printer | 192.168.10.20 |

---

## DHCP Address Pool

Client devices receive IP addresses automatically.

| Parameter | Value |
|-----------|-------|
| Start Address | 192.168.10.100 |
| End Address | 192.168.10.199 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.10.1 |
| DNS Server | 8.8.8.8 |

---

## Client Devices

| Device | Address Type |
|---------|--------------|
| PC1 | DHCP |
| PC2 | DHCP |
| PC3 | DHCP |
| PC4 | DHCP |
| PC5 | DHCP |
| PC6 | DHCP |

---

## Address Allocation Summary

| Address Range | Purpose |
|---------------|---------|
| 192.168.10.1 – 192.168.10.20 | Infrastructure Devices |
| 192.168.10.21 – 192.168.10.99 | Reserved for Future Devices |
| 192.168.10.100 – 192.168.10.199 | DHCP Clients |
| 192.168.10.200 – 192.168.10.254 | Reserved |

---

## Benefits

This addressing scheme provides:

- Easy network management
- Simplified troubleshooting
- Support for future expansion
- Clear separation between infrastructure and client devices
- Consistent IP allocation