# 01 — Identifying Devices on a Network
**Date:** 2025-11-06
**Source:** TryHackMe — "Identifying devices on a network" (Personal observations, no secure solutions included)

---

## Overview

Objective: To understand how devices are identified within a network — what identifiers are used (device name, IP address, MAC address), the difference between private and public addresses, and why this is important for network security.

---

## Key Concepts

### IP Address (Internet Protocol)
- A numerical address that identifies a device at the network level (Layer 3).

- **IPv4** Example: `192.168.1.77` (consists of 4 groups, each 0-255).

- **IPv6** is longer and offers more addresses: `2a00:22c4:...`

**Private vs. Public**
- **Private IP**: Used within a local network (e.g., `192.168.x.x`, `10.x.x.x`).

- **Public IP**: The address the internet sees (assigned by your ISP).

### MAC (Media Access Control) Address
- A unique address for a network interface (such as a Wi-Fi or Ethernet card) at the link level (Layer 2).

- Format: `a4:c3:f0:85:ac:2d` (6 hexadecimal groups).

- Usually stored on the device itself (from the factory) — sometimes found on the device label, sometimes not.

- Each interface has a separate MAC: One device may have a MAC for Wi-Fi and another for Ethernet.

### Practical Difference
- **ARP**: When a device wants to send a packet within a local network to a specific IP address, the device translates the IP address to the MAC address using ARP and then sends the packet to that MAC address.

---

## Useful Commands (Displaying MAC/IP)

### Windows
```PowerShell
ipconfig /all
