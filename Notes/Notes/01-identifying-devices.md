# 01 — Identifying Devices on a Network  
**Date:** 2025-11-06  
**Source:** TryHackMe — "Identifying devices on a network" (Personal notes — does not contain protected answers)

---

## Overview  
**Goal:** Understand how devices are identified on a network — what identities are used (device name, IP address, MAC address), the difference between private and public addresses, and why this matters in cybersecurity.

---

## Core Concepts  

### IP Address (Internet Protocol)  
- A numeric address that identifies a device at the **network layer (Layer 3)**.  
- **IPv4** example: `192.168.1.77` (consists of four octets, each ranging from 0–255).  
- **IPv6** is longer and provides far more unique addresses, e.g. `2a00:22c4:...`.  

**Private vs Public IPs**  
- **Private IP:** Used inside local networks (examples: `192.168.x.x`, `10.x.x.x`).  
- **Public IP:** Visible to the Internet, assigned by the ISP (Internet Service Provider).  

### MAC Address (Media Access Control)  
- A **unique hardware identifier** for each network interface (e.g., Wi-Fi or Ethernet card) at the **data link layer (Layer 2)**.  
- Format: `a4:c3:f0:85:ac:2d` (6 hexadecimal groups).  
- Usually embedded in the hardware by the manufacturer — sometimes printed on a sticker, sometimes only stored in firmware.  
- Each interface has its own MAC: one for Wi-Fi, another for Ethernet, etc.  

### Practical Difference  
- **ARP (Address Resolution Protocol):** When a device wants to send a packet to another IP within the same local network, it uses ARP to translate that IP into its corresponding MAC address, then sends the frame to that MAC.

---

## Useful Commands (Display MAC/IP Information)

### Windows
```powershell
ipconfig /all

