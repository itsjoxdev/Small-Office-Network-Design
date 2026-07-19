# Printer Configuration

## Overview

This document describes the printer configuration for the Small Office Network Design project.

The office printer is configured with a static IP address to ensure reliable access from all devices on the local network.

---

## Printer Information

| Parameter | Value |
|-----------|-------|
| Device | Printer-PT |
| IP Address | 192.168.10.20 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.10.1 |

---

## Network Configuration

The printer is connected to the office switch using a Copper Straight-Through cable.

A static IP address is assigned to prevent address changes and simplify printer management.

---

## Verification

The printer configuration was verified using a client computer on the local network.

### Test Results

- Static IP address configured successfully.
- Printer is reachable from client devices.
- Successful ping response with 0% packet loss.

---

## Expected Result

All devices connected to the office network should be able to communicate with the printer using its static IP address.