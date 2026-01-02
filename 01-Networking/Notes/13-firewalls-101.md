
# 🔥 Firewalls 101  
**Date:** 2025-11-19  
**Category:** Networking Notes  
**Topic:** Firewalls (Stateful vs Stateless)

---

## 📌 Introduction

A **firewall** is a device or software inside a network that determines what traffic is allowed to enter or exit.  
Think of a firewall as **border security** for a network.

A network administrator can configure a firewall to **permit** or **deny** traffic based on several factors:

- Where the traffic is coming from (source IP/network)
- Where the traffic is going (destination IP/network)
- What port the traffic is using (e.g., port 80, port 443)
- What protocol is being used (TCP, UDP, or both)

Firewalls use **packet inspection** to analyze incoming and outgoing traffic.

---

## 🔥 Why Firewalls Matter

Firewalls help protect networks from:

- Unauthorized access  
- Malware  
- Traffic from suspicious hosts  
- Attacks such as DDoS, port scanning, or brute force attempts  

They act as the **first line of defense** in network security.

---

## 🧱 Two Main Categories of Firewalls

Firewalls can be categorized into many types, but this lesson focuses on the two major categories:

---

## 1️⃣ **Stateful Firewall**

A **stateful firewall** analyzes the *entire connection*, not just individual packets.

### ✔ Characteristics

- Tracks the **state** of the connection  
- Makes decisions using the full context of the communication  
- Dynamically evaluates traffic  
- Requires more system resources  

### ✔ Example

A stateful firewall may allow the first steps of a TCP handshake, and if the host behaves maliciously, it will block the **entire device**, not just the packet.

### ✔ Pros

- More intelligent  
- More secure  
- Better decision-making  

### ✔ Cons

- Heavier on resources  
- Slower than stateless firewalls  

---

## 2️⃣ **Stateless Firewall**

A **stateless firewall** analyzes individual packets *without* considering any context or previous traffic.

### ✔ Characteristics

- Uses static rules  
- Fast but less intelligent  
- Only effective if strict rules match perfectly  

### ✔ Pros

- Extremely fast  
- Good for handling high-volume attacks (like DDoS)

### ✔ Cons

- Misses context  
- Useless if packet doesn’t match a defined rule exactly  

---

## 🧩 Where Do Firewalls Operate in the OSI Model?

Firewalls operate primarily in:

- **Layer 3 — Network Layer** (IP filtering)  
- **Layer 4 — Transport Layer** (TCP/UDP filtering)

Advanced firewalls (Next-Gen Firewalls, WAFs) may work at:

- Layer 5  
- Layer 7 (Application Layer)

But for this lesson:  
✔ **Layers 3 & 4**

---

## 🔍 Summary

| Firewall Type  | Examines | Pros | Cons |
|----------------|----------|------|------|
| **Stateful**   | Entire connection | Smart, secure | Uses more resources |
| **Stateless**  | Individual packets | Very fast | Less intelligent |

---

## 📝 Key Takeaways

- Firewalls decide what traffic enters or leaves a network.  
- They can allow (permit) or block (deny) traffic.  
- Stateful firewalls = smart, context-aware.  
- Stateless firewalls = fast, but rule-dependent.  
- OSI layers used = **Layer 3 & Layer 4**.  

---

https://youtu.be/kDEX1HXybrU

