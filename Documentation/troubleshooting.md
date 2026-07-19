# Network Troubleshooting Guide

## Overview

This document describes common network issues that may occur in the Small Office Network Design project and the recommended troubleshooting procedures.

---

# Scenario 1 — DHCP Not Working

## Symptoms

- Client receives no IP address.
- IP address appears as 169.254.x.x.
- No network connectivity.

## Possible Causes

- DHCP service is disabled.
- DHCP pool is incorrectly configured.
- Router interface is down.
- Physical cable disconnected.

## Troubleshooting Steps

1. Verify the router interface is up.

```cmd
show ip interface brief
```

2. Verify the DHCP pool.

```cmd
show ip dhcp pool
```

3. Verify DHCP bindings.

```cmd
show ip dhcp binding
```

4. Renew the client IP address.

```cmd
ipconfig /release
ipconfig /renew
```

## Resolution

- Enable the router interface.
- Correct the DHCP pool configuration.
- Verify network cabling.
- Renew the client's IP address.

---

# Scenario 2 — PC Does Not Receive an IP Address

## Symptoms

- IP Address: 169.254.x.x
- Unable to communicate on the network.

## Possible Causes

- DHCP unavailable.
- Network cable disconnected.
- Network adapter disabled.

## Troubleshooting Steps

1. Check cable connections.
2. Verify the NIC is enabled.
3. Confirm the router DHCP service is running.
4. Renew the IP address.

```cmd
ipconfig /renew
```

## Resolution

The PC successfully obtained an IP address after reconnecting to the network and renewing the DHCP lease.

---

# Scenario 3 — WiFi Client Cannot Connect

## Symptoms

- Wireless network not available.
- Authentication failed.
- Unable to obtain an IP address.

## Possible Causes

- Incorrect SSID.
- Incorrect WPA2 password.
- Access Point unavailable.
- Wireless adapter disabled.

## Troubleshooting Steps

1. Verify the SSID is **Office-WiFi**.
2. Verify the WPA2-PSK password.
3. Check that the Access Point is powered on.
4. Ensure the wireless client is within coverage.
5. Renew the DHCP lease.

## Resolution

After correcting the wireless settings and reconnecting, the laptop successfully joined the wireless network and received an IP address from DHCP.

---

# Scenario 4 — Printer Offline

## Symptoms

- Printer cannot be reached.
- Print requests fail.
- Ping to printer fails.

## Possible Causes

- Incorrect static IP.
- Printer disconnected.
- Switch port down.
- Incorrect default gateway.

## Troubleshooting Steps

1. Verify printer power.
2. Check Ethernet cable.
3. Verify printer IP configuration.

Expected configuration:

| Parameter | Value |
|-----------|-------|
| IP Address | 192.168.10.20 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.10.1 |

4. Test connectivity.

```cmd
ping 192.168.10.20
```

## Resolution

After verifying the network configuration and physical connection, the printer responded successfully to network requests.

---

# Recommended Troubleshooting Workflow

1. Verify physical connections.
2. Check device status.
3. Verify IP configuration.
4. Test connectivity using Ping.
5. Verify DHCP operation.
6. Verify wireless connectivity.
7. Verify server and printer accessibility.
8. Document the issue and applied solution.

---

# Useful Commands

```cmd
ipconfig
```

Display current IP configuration.

```cmd
ipconfig /all
```

Display detailed network configuration.

```cmd
ipconfig /release
```

Release the current IP address.

```cmd
ipconfig /renew
```

Request a new IP address.

```cmd
ping
```

Test network connectivity.

```cmd
show ip interface brief
```

Display router interface status.

```cmd
show ip dhcp pool
```

Display DHCP pool information.

```cmd
show ip dhcp binding
```

Display DHCP client bindings.

---

# Conclusion

The troubleshooting procedures described in this document provide a structured approach for identifying and resolving common issues related to DHCP, IP addressing, wireless connectivity, printers, and general network communication within the Small Office Network Design project.