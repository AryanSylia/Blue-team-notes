#03 — Network Subnetting 🌐
**Date:** 2025-11-07
**Source:** TryHackMe — *A Primer on Subnetting*
*(Personal learning notes — not containing protected answers)*

---

## 🧭 Overview
**Subnetting** is the process of dividing a large network into smaller, independent networks.

The idea is simple: just like cutting a cake for several people, you divide the IP addresses into smaller groups.

Each group represents a specific department or purpose within the same organization — such as accounting, human resources, or customer service.

---

## 🧩 Subnet Mask

A subnet mask is not a device, but a number written in the same format as an IP address, such as:

255.255.255.0

🔹 Its role is to determine which part of an IP address belongs to the **network** and which part belongs to the **hosts**.

### 🧠 Illustrative Example
IP Address → `192.168.1.10`
Subnet Mask → `255.255.255.0`

| Part | Explanation |

|--------|----------|

| Parts with the value `255` | Belong to the network (static) |

| Parts with the value `0` | Belong to the hosts (variable) |


📘 Therefore:
- Network Address → `192.168.1.0`
- First Device → `192.168.1.1`
- Last Device → `192.168.1.254`
- Broadcast → `192.168.1.255`

The mask tells the system where the network begins and ends, and therefore how many devices can be connected to it.

---

## 🚦 Default Gateway

The **Default Gateway** is usually the **Router** that connects your local network to the internet or other networks.

🔹 Think of it as the **main door** of the network — any device that wants to send data out of the network goes through it.

Example:
- Network: `192.168.1.0/24`
- Your Device: `192.168.1.10`
- Gateway: `192.168.1.1` or `192.168.1.254`

📦 When you try to open a website:

1. Your device sends data to the Gateway.

2. The Router (Gateway) forwards it to the internet.

3. When a response arrives, it returns it to your device.

---

## 🧱 Subnetting — Concept and Purpose
Subnetting = Dividing the network into subnets.

It can be applied to **large or small** networks as needed.

### ⚙️ Practical Example:

In a small cafe:
- Staff Network: `192.168.10.0/24`

- Customer Network (Wi-Fi): `192.168.20.0/24`

📌 Benefits:
- 🔒 **Security:** Customers cannot access the cash register or management equipment.

- ⚡ **Efficiency:** Reduced data congestion.

- 🧠 **Control:** Easier management of each network segment.

---

## 🧾 Network Address Types
| Type | Function | Example |

|-------|----------|---------|

| **Network Address** | Identifies the network start and scope | `192.168.1.0` |

| **Host Address** | Identifies a device within the network | 192.168.1.100 |

| **Default Gateway** | Device that sends data outwards | 192.168.1.254 |

---

## 🔍 Benefits of Subnetting
- **Efficiency:** Better address allocation and reduced congestion.

- **Security:** Isolating partitions and protecting internal networks.

- **Control:** Flexibility in managing each part of the network.

---

## 🧠 Quick Recap
| Concept | What is it? | Function | Example |

|----------|---------|---------|--------|

| **Subnet Mask** | A number that identifies network segments and devices | Determines network size and number of hosts | 255.255.255.0 |

| **Default Gateway** | Device (Router) | Sends data outside the network | 192.168.1.1 |

| **Subnetting** | Dividing the network into smaller networks | Security, efficiency, control | Staff network + Customer network |

---

## 🖥️ ASCII Visualization

