
# 📦 Ports 101 (Practical)
**Date:** 17 November 2025  

---

## 🌐 Overview

Ports are essential logical points through which data is exchanged between devices on a network.  
Think of a harbour: ships (applications) must dock at the correct port number to exchange cargo (data).  
If the port isn’t compatible, the connection cannot be made.

When a connection is established, all data sent or received by a device **must pass through a port number**.  
Ports are represented by a numerical value ranging from:

0 – 65535


To avoid chaos with thousands of possible ports, networking standards have assigned **common and well-known ports** to specific protocols so applications behave uniformly.

---

## 🔢 Why Do We Need Ports?

- A single device can run many applications at the same time.  
- Ports allow the system to distinguish **which application** should receive the incoming data.  
- Example:  
  - Web browser → Port **80** (HTTP) or **443** (HTTPS)  
  - SSH connection → Port **22**  
  - File transfer → Port **21**

Ports below **1024** are known as **Well-Known Ports** and are reserved for standard protocols.

---

## 📚 Common Ports & Their Protocols

### 🔐 Well-Known Ports Table

| Protocol | Port Number | Description |
|---------|-------------|-------------|
| **FTP** (File Transfer Protocol) | 21 | Used for downloading or uploading files between a client and a file server. |
| **SSH** (Secure Shell) | 22 | Secure login to remote systems using encrypted text-based sessions. |
| **HTTP** (HyperText Transfer Protocol) | 80 | Powers the World Wide Web (WWW). Used by browsers to load web pages. |
| **HTTPS** (HyperText Transfer Protocol Secure) | 443 | Secure version of HTTP using encryption (TLS/SSL). |
| **SMB** (Server Message Block) | 445 | File and device sharing (printers, folders) across a network. |
| **RDP** (Remote Desktop Protocol) | 3389 | Secure remote desktop access using a visual GUI interface. |

---

## ⚙️ How Ports Work

Ports **are not physical**.  
They are **logical entry points** inside the Operating System.

A device may have:

- **One IP address**,  
- but **thousands of ports** available for various applications.

Example:

| Application | Port Used |
|------------|-----------|
| Chrome Tab 1 | Random port (e.g., 51234) |
| Chrome Tab 2 | Random port (e.g., 51235) |
| SSH Client | 22 |
| Web Server | 80 |

Each port is like an apartment inside one building — the IP is the building address, and the port is the apartment number.

---

## 🧠 Important Notes

- Ports **do not guarantee security** — attackers can scan ports.  
- Applications **can run on non-standard ports**, but clients must specify the port manually.  
  Example:  
  Running a web server on port 8080 →  


---

## ✅ Summary

- Ports are logical pathways for data inside a device.
- Range: **0 → 65535**
- Ports < **1024** = Well-known ports.
- Used to direct traffic to the correct application.
- Different protocols follow standard port rules.

---
