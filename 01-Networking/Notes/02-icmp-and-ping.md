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

