# Router Configuration

## Overview

This document describes the configuration of the Cisco router used in the Small Office Network Design project.

The router serves as the default gateway for all devices on the local network.

---

## Device Information

| Parameter | Value |
|-----------|-------|
| Device | Cisco 2911 |
| Hostname | Office-Router |
| Interface | GigabitEthernet0/0 |
| IP Address | 192.168.10.1 |
| Subnet Mask | 255.255.255.0 |

---

## Configuration Commands

```bash
enable
configure terminal

hostname Office-Router

interface GigabitEthernet0/0
ip address 192.168.10.1 255.255.255.0
no shutdown

end
write memory
```

---

## Verification

Use the following command to verify the configuration:

```bash
show ip interface brief
```

Expected result:

- GigabitEthernet0/0 is **up**
- IP Address is **192.168.10.1**

---

## Purpose

The router provides:

- Default Gateway
- Communication between the LAN and external networks
- Foundation for DHCP and future Internet connectivity

---

## Notes

- The interface must be enabled using `no shutdown`.
- Save the configuration using `write memory` to preserve changes after reboot.