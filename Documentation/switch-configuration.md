# Switch Configuration

## Overview

This document describes the configuration of the Cisco 2960 switch used in the Small Office Network Design project.

The switch provides Layer 2 connectivity for all devices and includes a management IP address for administrative access.

---

## Device Information

| Parameter | Value |
|-----------|-------|
| Device | Cisco Catalyst 2960 |
| Hostname | Office-Switch |
| Management VLAN | VLAN 1 |
| Management IP | 192.168.10.2 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.10.1 |

---

## Configuration Commands

```bash
enable
configure terminal

hostname Office-Switch

interface vlan 1
ip address 192.168.10.2 255.255.255.0
no shutdown
exit

ip default-gateway 192.168.10.1

enable secret Cisco123!

service password-encryption

banner motd #Unauthorized access is prohibited#

end
write memory
```

---

## Verification

Verify the management interface:

```bash
show ip interface brief
```

Verify the running configuration:

```bash
show running-config
```

---

## Purpose

The switch provides:

- Layer 2 network connectivity
- Management access using VLAN 1
- Basic security configuration
- Default gateway for remote management

---

## Notes

- VLAN 1 is used as the management interface.
- The switch does not perform routing.
- Password encryption is enabled for improved security.