# 05 — DHCP (Dynamic Host Configuration Protocol) 📡  
**Date:** 2025-11-07  
**Source:** TryHackMe — *DHCP Task*  
*(Personal learning note — no protected answers included)*  

---

## 🧩 What is DHCP?

**DHCP** stands for **Dynamic Host Configuration Protocol**.  
It is the protocol responsible for **automatically assigning IP addresses** to devices on a network.  

Instead of manually configuring IPs for every device, a **DHCP server** automatically handles this process when a device connects to the network.

---

## ⚙️ How DHCP Works

When a device connects to a network, it doesn’t yet have an IP address.  
So, it communicates with the DHCP server through a process called **DORA**, which consists of four steps:

| Step | Name | Description |
|------|------|--------------|
| **D** | **DHCP Discover** | The device broadcasts a message: “Hey, I’m new here! Is there any DHCP server that can give me an IP address?” |
| **O** | **DHCP Offer** | The DHCP server replies: “Sure! You can use IP address **192.168.1.10**.” |
| **R** | **DHCP Request** | The device confirms: “Yes, I’d like to use **192.168.1.10**.” |
| **A** | **DHCP Acknowledgment (ACK)** | The server confirms: “Done! You can use that IP for the next 24 hours.” |

After these four steps, the device can use the assigned IP and join the network.

---

## 💻 Example (Based on the Diagram)

1️⃣ **DHCP Discover**  
> Device → “Hey, I’m new here, who can give me an IP address?”

2️⃣ **DHCP Offer**  
> Server → “You can use **192.168.1.10**.”

3️⃣ **DHCP Request**  
> Device → “Yes please, I’ll take that IP.”

4️⃣ **DHCP ACK**  
> Server → “Perfect. You can use it for 24 hours.”

---

## 🧠 Why DHCP is Important

| Benefit | Description |
|----------|-------------|
| ⚡ **Automatic** | No need to manually assign IPs to each device. |
| 🧩 **Organized** | Prevents IP conflicts between devices. |
| 🧱 **Scalable** | Works efficiently even in large networks. |
| ⏰ **Temporary (Leased)** | Each IP is assigned for a limited time before renewal. |

---

## 🧾 Summary — DORA Steps

| Step | DHCP Message | Sent By | Received By | Purpose |
|------|----------------|----------|-------------|----------|
| **D** | DHCP Discover | Device | Broadcast | Search for DHCP server |
| **O** | DHCP Offer | DHCP Server | Device | Offer an IP address |
| **R** | DHCP Request | Device | DHCP Server | Confirm acceptance of the offered IP |
| **A** | DHCP ACK | DHCP Server | Device | Confirm assignment (final step) |

---

## ⚙️ Additional Notes

- DHCP servers are often built into **home routers**.  
- If no DHCP server is available, the device assigns itself an **APIPA address** (e.g., `169.254.x.x`).  
- DHCP can also distribute other network information such as:
  - **Default Gateway**
  - **DNS Server**
  - **Subnet Mask**

---

## 🧭 Simple Analogy

Imagine you arrive at a hotel (the network).  
You go to reception (the DHCP server) and say, “I need a room.” (**Discover**)  
The receptionist offers you Room 10. (**Offer**)  
You agree to take it. (**Request**)  
The receptionist gives you the key and confirms. (**ACK**)  
You now have a room number (IP) and can stay connected.

---

## 🧩 Quick Recap

| Term | Meaning | Function |
|------|----------|-----------|
| **DHCP** | Dynamic Host Configuration Protocol | Automatically assigns IPs |
| **DORA** | Discover, Offer, Request, Acknowledge | The four steps of DHCP |
| **Lease Time** | Duration of IP validity | Can be renewed or changed |
| **DHCP Server** | Device that assigns IPs | Often the router |
| **APIPA** | Automatic Private IP Addressing | Used when DHCP is unavailable |

---

**Tags:** `networking` `dhcp` `ip` `addressing` `tryhackme`

---

## ▶️ Next Topic Preview

**Next:** *The OSI Model — Understanding the 7 Layers of Networking.*
