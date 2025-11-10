# 06 — OSI Model (Open Systems Interconnection) 🧱  
**Date:** 2025-11-10  
**Source:** TryHackMe — *OSI Model Task*  
*(Personal learning note — no protected answers included)*  

---

## 🧩 What is the OSI Model?

The **OSI Model** (Open Systems Interconnection) is a **conceptual framework** used in networking to describe how data travels from one device to another.  
It defines **seven layers**, each with a specific role, ensuring that devices and software from different vendors can communicate properly.

Think of it as a **blueprint** or **map** showing how information moves through a network — from your app all the way to the physical wire or Wi-Fi signal.

---

## 🎯 Why It Exists

The OSI Model allows different types of hardware and software to **work together** by following common rules.  
This means a router from Cisco can communicate with a computer running Windows or Linux without any problem, because all of them follow the same 7-layer standard.

---

## 🧱 The 7 Layers of the OSI Model

| # | Layer | Function |
|---|--------|-----------|
| **7️⃣** | **Application** | The layer that interacts directly with the user — apps like browsers or email clients live here. |
| **6️⃣** | **Presentation** | Translates data into a readable format (text, images, encryption, compression). |
| **5️⃣** | **Session** | Manages communication sessions (start, maintain, and end connections). |
| **4️⃣** | **Transport** | Responsible for reliable data transfer using protocols like **TCP** or **UDP**. |
| **3️⃣** | **Network** | Determines the best path for data and handles **IP addressing**. |
| **2️⃣** | **Data Link** | Manages **MAC addresses** and moves data between devices on the same network. |
| **1️⃣** | **Physical** | The actual hardware — cables, Wi-Fi signals, network cards, and electricity. |

---

## 🧭 Simple Example — Sending a WhatsApp Message

When you send a message to a friend:

1. You type the message → **Application Layer**  
2. The message is formatted and encoded → **Presentation Layer**  
3. A connection is established between both phones → **Session Layer**  
4. The message is divided into packets → **Transport Layer**  
5. The network finds the best route → **Network Layer**  
6. The packets are directed using MAC addresses → **Data Link Layer**  
7. The message is transmitted physically (Wi-Fi/electric signals) → **Physical Layer**

When the message arrives, your friend’s phone reverses the process from Layer 1 → Layer 7.

---

## 📦 What Is "Encapsulation"?

As data moves down through the layers, **each layer adds its own header** (extra info like port numbers, IPs, or MAC addresses).  
This wrapping process is called **Encapsulation**.  
When the data reaches its destination, the layers remove the headers one by one — called **De-encapsulation** — to reveal the original content.

---

## 🧠 Key Facts

| Question | Answer |
|-----------|--------|
| What does “OSI” stand for? | **Open Systems Interconnection** |
| How many layers are there? | **7 layers** |
| What is the process of adding headers called? | **Encapsulation** |

---

## 💡 Memory Trick

To remember the 7 layers from top to bottom:

> **All People Seem To Need Data Processing**  
> *(Application – Presentation – Session – Transport – Network – Data Link – Physical)*

Or, from bottom to top:

> **Please Do Not Throw Sausage Pizza Away 🍕**

---

## 🧾 Summary

The OSI Model helps us **organize and understand** how data travels in a network.  
Each layer has its own job — from the physical transmission (Layer 1) to the user-facing app (Layer 7).  
This structure makes it possible for any device, regardless of brand or design, to communicate seamlessly.

---

**Tags:** `networking` `osi-model` `tcp-ip` `encapsulation` `tryhackme`

---

