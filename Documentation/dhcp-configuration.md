# DHCP Configuration

## Overview

This document describes the DHCP configuration for the Small Office Network Design project.

The Cisco 2911 router acts as the DHCP server, automatically assigning IP addresses to client devices on the LAN.

---

## Network Information

| Parameter | Value |
|-----------|-------|
| Network | 192.168.10.0/24 |
| Default Gateway | 192.168.10.1 |
| DNS Server | 8.8.8.8 |
| DHCP Range | 192.168.10.100 – 192.168.10.254 |
| Lease Time | 7 Days |

---

## Excluded Addresses

The following addresses are reserved for network infrastructure and static devices:

- 192.168.10.1 (Router)
- 192.168.10.2 (Switch)
- 192.168.10.10 (Server)
- 192.168.10.20 (Printer)

---

## Router Configuration

```bash
ip dhcp excluded-address 192.168.10.1 192.168.10.99

ip dhcp pool OFFICE-LAN
network 192.168.10.0 255.255.255.0
default-router 192.168.10.1
dns-server 8.8.8.8
lease 7
```

---

## Verification

Verify the DHCP pool:

```bash
show ip dhcp pool
```

Verify assigned addresses:

```bash
show ip dhcp binding
```

---

## Expected Result

Client devices automatically receive:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

without manual configuration.

---

## Notes

Infrastructure devices such as the router, switch, server, and printer use static IP addresses, while client PCs receive dynamic addresses from the DHCP server.