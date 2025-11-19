
# 🔐 VPN Basics  
**Date:** 19 November 2025  
**Category:** Networking Fundamentals  
**Topic:** Virtual Private Networks (VPN)

---

## 🛰️ What Is a VPN?

A **Virtual Private Network (VPN)** is a technology that allows devices on separate networks to communicate securely by creating an encrypted tunnel over the Internet. Devices connected through this tunnel form their own private network, even if they are geographically far apart.

A VPN makes two or more networks behave **as if they were a single internal network**.

---

## 🌐 Why Do We Use VPNs?

Under normal conditions, devices can only communicate directly if they are on the **same internal network** (e.g., inside the same office).

A VPN solves this by creating a **secure, encrypted connection** between:

- Office #1 and Office #2  
- A remote worker and the company network  
- Two servers in different geographical locations  
- You and TryHackMe labs

This allows devices to share resources as if they were on the same LAN.

---

## 🧩 Example Scenario

Consider three networks:

1. **Network #1 (Office #1)**
2. **Network #2 (Office #2)**
3. **Network #3 (VPN tunnel connecting both)**

Devices inside Network #3 remain part of their original networks (#1 and #2), but they also gain access to a **private shared environment** where they can securely communicate across both locations.

---

## ⭐ Benefits of Using a VPN

### **1. Connects Geographically Separate Networks**
Businesses with multiple offices rely on VPNs to:
- Share files and servers  
- Access internal tools  
- Allow employees to work remotely

---

### **2. Provides Privacy**
VPN technology encrypts traffic, which means:
- ISPs cannot see your browsing activity  
- Sniffers cannot read your data  
- Public WiFi becomes safer to use

Encryption protects both the **source** and **destination** of the data.

---

### **3. Offers Anonymity**
VPNs hide your real IP address, helping to:
- Bypass censorship  
- Protect user identity  
- Evade tracking by ISPs or intermediaries

However, anonymity depends on:
- The VPN provider  
- Logging policies  
- Encryption strength

---

## 🛡️ Why TryHackMe Uses a VPN

TryHackMe requires a VPN connection so that:

- You can securely interact with vulnerable machines  
- Your ISP does not think you are attacking devices on the open Internet  
- TryHackMe machines remain **isolated** and inaccessible without VPN  
- The lab environment stays controlled and safe

---

## 🔧 VPN Technologies

Below are common VPN technologies and how they work:

### **PPP (Point-to-Point Protocol)**
- Provides **authentication and encryption** using a private key and certificate.  
- The certificate must match the server’s.  
- **Non-routable** — cannot leave its network on its own.  
- Used inside other VPN technologies (e.g., PPTP).

---

### **PPTP (Point-to-Point Tunneling Protocol)**
- Wraps PPP data so it can travel across networks.  
- Extremely easy to configure.  
- Supported by most devices.  
- Weak encryption compared to modern standards.

---

### **IPSec (Internet Protocol Security)**
- Encrypts data using the existing **IP framework**.  
- Difficult to set up but very secure when implemented correctly.  
- Strong encryption and widely supported by modern systems.


---

## 📚 Summary

A VPN:
- Creates a secure tunnel  
- Allows remote networks to communicate  
- Provides privacy and anonymity  
- Uses protocols such as **PPP**, **PPTP**, and **IPSec**

VPNs are essential for both cybersecurity training and real-world enterprise networks.

---
