# Wireless Configuration

## Overview

This document describes the wireless network configuration for the Small Office Network Design project.

The wireless network is provided through a dedicated Access Point connected to the office switch.

---

## Wireless Settings

| Setting | Value |
|---------|-------|
| SSID | Office-WiFi |
| Security | WPA2-PSK |
| Encryption | AES |
| Password | Office@2026Secure |
| Channel | 6 |
| Coverage Range | 140 meters |

---

## Access Point Configuration

The Access Point-PT device is configured as a Layer 2 wireless bridge connected to the office switch.

The device provides wireless connectivity for clients through the configured SSID and WPA2-PSK security.

---

## Security

The wireless network uses WPA2-PSK with AES encryption to prevent unauthorized access.

---

## Verification

The wireless network was successfully tested using a Laptop-PT client.

### Test Results

- Connected to SSID: Office-WiFi
- Authentication: WPA2-PSK (AES)
- IP Address Assigned via DHCP: 192.168.10.106
- Default Gateway: 192.168.10.1
- Successfully pinged the router with 0% packet loss.

The wireless configuration is functioning correctly.

---

## Expected Result

Wireless devices should obtain network connectivity through DHCP and communicate with other devices on the local network.

The wireless configuration has been successfully validated.