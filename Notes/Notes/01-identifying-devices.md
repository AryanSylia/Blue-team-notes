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


# 02 — ICMP and Ping  
**Date:** 2025-11-06  
**Source:** TryHackMe — "Ping (ICMP)" (Personal notes — does not contain protected answers)

---

### 🧩 **ICMP (Internet Control Message Protocol)**  
ICMP stands for **Internet Control Message Protocol**.  
It is used within networks to exchange **control and diagnostic messages** between devices.  
ICMP operates at the **Network Layer (Layer 3)** of the OSI model and helps detect and report connection issues.

**Main purposes of ICMP:**  
- Verify if another device is reachable on the network.  
- Notify systems about connection or routing problems (e.g., destination unreachable, timeout).  
- Send control messages such as *Echo Reply*, *Destination Unreachable*, or *Time Exceeded*.

In short:  
> ICMP does not transfer user data — it manages and monitors the health of network communication.

---

### ⚙️ **Ping**  
**Ping** is a utility that uses ICMP to test the connectivity between two network devices.  
When you run the `ping` command, your system sends **ICMP Echo Request** packets to a target host and waits for **ICMP Echo Reply** packets in return.  
This process measures how long it takes for data to travel to the target and back (the **Round Trip Time**, or RTT).

**What Ping provides:**  
- Confirms whether the remote host is online and reachable.  
- Measures network latency (response time).  
- Detects packet loss or instability in the connection.

---

### 📡 **Relationship Between Ping and ICMP**  
- **Ping** is the **tool**.  
- **ICMP** is the **protocol** that makes it work.  

In other words, *Ping* is the practical interface that lets you test a network connection using *ICMP messages*.

---

### 🧠 **Key Terms**

| Term | Meaning |
|------|----------|
| **Echo Request** | The ICMP message sent by the source device to check connectivity. |
| **Echo Reply** | The ICMP message sent by the destination device in response. |
| **RTT (Round Trip Time)** | The total time taken for a packet to go to the target and return. |
| **TTL (Time To Live)** | The number of hops a packet can travel before being discarded. |
| **Packet Loss** | The percentage of packets that never reach their destination or are not acknowledged. |

---

**Tags:** `networking`, `icmp`, `ping`, `tryhackme`, `blue-team`
