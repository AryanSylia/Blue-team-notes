# 03 — Network Fundamentals 🌐  
**Date:** 2025-11-07  
**Source:** TryHackMe — *LAN Topologies*  
*(Personal learning notes — not containing protected answers)*  

---

## 🧭 Overview
Understanding how devices connect and communicate in a **Local Area Network (LAN)** is essential.  
A network’s **topology** describes its physical or logical layout — how devices (nodes) are linked together.  
Different topologies affect performance, reliability, and cost.

---

## 🌟 Star Topology
**Definition:**  
All devices connect individually to a central network device (switch or hub).

**Advantages:**
- Easy to add or remove devices.  
- Failure of one cable does not affect others.  
- Easier troubleshooting.  
- Scalable and commonly used today.

**Disadvantages:**
- Requires more cabling → higher cost.  
- If the central switch/hub fails → entire network goes down.  
- Maintenance becomes harder as the network grows.

**Common Use:** Offices, schools, home networks.

---

## 🚏 Bus Topology
**Definition:**  
All devices share one main communication cable called the *backbone*.  
Data travels in both directions along this single line.

**Advantages:**
- Simple and cheap to set up.  
- Requires less cabling.

**Disadvantages:**
- Network performance slows with more devices.  
- Troubleshooting is difficult (single cable).  
- One break in the backbone stops communication for all devices.

**Common Use:** Older or small temporary networks.

---

## 🔄 Ring Topology
**Definition:**  
Each device connects to exactly two others, forming a closed loop (ring).  
Data travels in one direction through each device until reaching the target.

**Advantages:**
- Less prone to collisions.  
- Easier fault isolation in small networks.  
- Requires less cabling than a star.

**Disadvantages:**
- If one link fails, the entire ring breaks (unless redundant).  
- Not efficient for large networks (higher latency).  

**Common Use:** Older LANs, token-based networks.

---

## 🧩 Hybrid / Extended Topologies
**Definition:**  
Combination of two or more topologies (e.g., several star networks linked together).  
Provides balance between scalability, performance, and redundancy.

**Common Use:**  
Enterprise environments (core–distribution–access network design).

---

## ⚙️ Switch — What It Does
- Operates at **Layer 2 (Data Link)**.  
- Uses **MAC addresses** to send data only to the correct destination port.  
- Reduces traffic compared to a hub.  
- Builds a *MAC Address Table* dynamically.  
- Connects devices **within** the same LAN.

**Key Point:** Efficient internal communication inside one network segment.

---

## 🚦 Router — What It Does
- Operates at **Layer 3 (Network)**.  
- Uses **IP addresses** to route data **between networks** (LAN ↔ Internet).  
- Decides the best path for packets (routing tables).  
- Can perform NAT, firewalling, or VLAN inter-routing.  

**Key Point:** Connects different networks together (e.g., local network to the Internet).

---

## 🧠 Key Concepts
| Concept | Meaning |
|----------|----------|
| **Single Point of Failure** | A component whose failure stops the entire network (e.g., central switch in star topology). |
| **Collision Domain** | Network area where data packets can collide; reduced by using switches. |
| **Broadcast Domain** | All devices that receive broadcast packets; routers separate these domains. |
| **Scalability** | How easily the network can grow while maintaining performance. |
| **Redundancy** | Having backup paths or devices to increase reliability. |

---

## 🧱 Best Practices
- Use **Star or Hierarchical** topologies for modern LANs.  
- Implement **redundant links** or backup switches to avoid downtime.  
- Separate traffic with **VLANs** for security and organization.  
- Use **Spanning Tree Protocol (STP)** to prevent switching loops.  
- Monitor network traffic via **SNMP / NetFlow / IDS** tools.

---

## 🧾 Summary
| Topology | Pros | Cons | Typical Use |
|-----------|------|------|--------------|
| **Star** | Reliable, scalable, easy to manage | Central device failure affects all | Offices, homes |
| **Bus** | Cheap, simple | Collisions, single failure point | Legacy/small setups |
| **Ring** | Less collisions, predictable path | Break = full outage | Old token networks |
| **Hybrid** | Scalable, flexible | Complex setup | Enterprises |

---

**Tags:** `networking` `topologies` `switch` `router` `tryhackme` `lan`


Star:      Bus:         Ring:
   *         *-*         *-*-*
  /|\         |             |
 * * *       * *           * *
