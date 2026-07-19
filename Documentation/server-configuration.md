# Server Configuration

## Overview

This document describes the server configuration for the Small Office Network Design project.

The server provides basic network services and is configured with a static IP address to ensure consistent availability on the local network.

---

## Server Information

| Parameter | Value |
|-----------|-------|
| Device | Server-PT |
| Hostname | Office-Server |
| IP Address | 192.168.10.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.10.1 |
| DNS Server | 8.8.8.8 |

---

## Network Configuration

The server is connected directly to the office switch using a Copper Straight-Through cable.

A static IP address is assigned to ensure that clients can reliably access server services.

---

## HTTP Service

The HTTP service is enabled to provide basic web services within the local network.

Clients can access the server using:

```text
http://192.168.10.10
```

---

## Verification

The server configuration was verified using a client computer on the local network.

### Test Results

- Static IP address configured successfully.
- Server is reachable from client devices.
- Successful ping response from clients.
- HTTP service is configured and available for local network access.

---

## Expected Result

The server should remain accessible using its static IP address and provide web services to authorized devices connected to the office network.