# Network Testing

## Overview

This document summarizes the verification tests performed to validate the functionality of the Small Office Network Design project.

All critical network services were tested to ensure proper communication between devices.

---

## Test Environment

| Component | Status |
|----------|--------|
| Router | Operational |
| Switch | Operational |
| Access Point | Operational |
| DHCP | Operational |
| Server | Operational |
| Printer | Operational |
| Wired Clients | Operational |
| Wireless Clients | Operational |

---

## Connectivity Tests

### Router Connectivity

Command:

```cmd
ping 192.168.10.1
```

Result:

- Successful
- 0% Packet Loss

---

### Server Connectivity

Command:

```cmd
ping 192.168.10.10
```

Result:

- Successful
- 0% Packet Loss

---

### Printer Connectivity

Command:

```cmd
ping 192.168.10.20
```

Result:

- Successful
- 0% Packet Loss

---

### PC-to-PC Connectivity

Client devices successfully communicated with each other over the local network.

Result:

- Successful
- 0% Packet Loss

---

### DHCP Verification

All client devices configured for DHCP automatically received valid IPv4 addresses from the router.

Example:

| Device | IP Address |
|---------|------------|
| PC-1 | 192.168.10.100 |
| Laptop | 192.168.10.106 |

---

### Wireless Connectivity

The wireless laptop successfully:

- Connected to Office-WiFi
- Authenticated using WPA2-PSK (AES)
- Received an IP address via DHCP
- Successfully communicated with the router

---

## Test Summary

| Test | Status |
|------|--------|
| Router Ping | Passed |
| Server Ping | Passed |
| Printer Ping | Passed |
| PC-to-PC Communication | Passed |
| DHCP Address Assignment | Passed |
| Wireless Connectivity | Passed |

---

## Conclusion

All network components were successfully configured and verified.

The Small Office Network Design project provides reliable wired and wireless connectivity, automatic IP address assignment through DHCP, and communication with network services including the office server and network printer.