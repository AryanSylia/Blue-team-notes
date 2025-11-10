# 05 — ARP (Address Resolution Protocol) 🔁  
**Date:** 2025-11-07  
**Source:** TryHackMe — *ARP Task*  
*(Personal learning note — no protected answers included)*  

---

## 🧩 What is ARP?

**ARP** stands for **Address Resolution Protocol**,  
and it is the technology that allows a device to find out **the physical (MAC) address** that corresponds to an **IP address** within a local network.

Each device on a network has two main identifiers:
- **IP Address** → The logical address (like your home address)
- **MAC Address** → The physical address (like your ID card)

When one device wants to communicate with another, it cannot send packets using only the IP address.  
It needs to know the **MAC address** of the target device — and that’s exactly what ARP provides.

---

## ⚙️ How ARP Works

Every device keeps a small table called the **ARP Cache**,  
which stores a list of known IP addresses and their corresponding MAC addresses.

When a device doesn’t know the MAC address of another host, it performs the following steps:

### 1. **ARP Request**
A broadcast message is sent to all devices in the network asking:
> “Who has the IP address 192.168.1.10?”

Only the device that owns this IP address will respond.

### 2. **ARP Reply**
The device that has the requested IP address responds:
> “I have that IP — my MAC address is 18:AC:33:12:88:29.”

The requester then stores this mapping in its **ARP Cache** for future use.

---

## 🧠 Example (from the diagram)

1️⃣ **Step 1:**  
Computer A (MAC: `01:00:AB:78:99:33`) sends an **ARP Request** asking who owns IP `192.168.1.10`.

2️⃣ **Step 2:**  
Computer B, which has IP `192.168.1.10`, replies with its MAC: `18:AC:33:12:88:29`.

3️⃣ **Result:**  
Computer A stores the mapping:  
> `192.168.1.10 → 18:AC:33:12:88:29`  
and can now communicate directly without broadcasting again.

---

## 🧾 ARP Summary Table

| Concept | Description | Example |
|----------|--------------|----------|
| **ARP Goal** | Link IP address to MAC address | `192.168.1.10 → 18:AC:33:12:88:29` |
| **Messages** | ARP Request / ARP Reply | “Who has IP 192.168.1.10?” → “I do!” |
| **ARP Cache** | Stores learned IP-MAC mappings | `arp -a` (to view on Windows/Linux) |
| **Scope** | Works only within the local network (LAN) | Not used across routers |
| **Purpose** | Enables local communication between devices | PCs, printers, routers, etc. |

---

## 🧩 Simple Analogy

Imagine you know someone’s **name** (IP) but not their **face** (MAC).  
You ask aloud: “Who is John?” (**ARP Request**)  
John answers: “I’m John, and this is me.” (**ARP Reply**)  
Now you remember his face for next time (**ARP Cache**).  

---

## 🧠 Quick Recap

| Term | Definition | Function |
|------|-------------|-----------|
| **ARP** | Address Resolution Protocol | Links IPs to MACs |
| **ARP Request** | Broadcast message asking for MAC | “Who has this IP?” |
| **ARP Reply** | Response containing the MAC address | “This is my MAC.” |
| **ARP Cache** | Temporary table storing known IP–MAC pairs | Speeds up future communication |

---

**Tags:** `networking` `arp` `ip` `mac` `protocol` `tryhackme`
