# 07 — OSI Model (Open Systems Interconnection) 🧱  
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

---

## 🧱 Layer 1 — Physical Layer 

### ⚙️ Overview

The **Physical Layer** is the **lowest layer** in the OSI Model.  
It deals with the **physical components** of networking — the actual hardware that sends and receives data.  
This layer is responsible for **transmitting raw bits (1s and 0s)** over a physical medium like cables or wireless signals.

---

### 🔌 Function

At this level, data isn’t “packets” or “frames” yet — it’s just **electrical, optical, or radio signals**.  
The devices here don’t understand what the data means; they only handle the **transmission** and **reception** of the signal.

- The bit **1** may be represented by an **electrical pulse** (or light in fiber optics).  
- The bit **0** may be represented by the **absence** of that pulse.

In other words, this layer converts digital data into physical signals that can travel through wires or the air.

---

### 🧩 Examples of Physical Layer Components

| Component | Description |
|------------|--------------|
| **Ethernet Cables** | Transfer data through electrical signals between devices. |
| **Fiber Optic Cables** | Use light pulses to carry information over long distances. |
| **Connectors** | Physical interfaces that link cables and devices (e.g., RJ45). |
| **Hubs / Repeaters** | Devices that boost or extend the physical signal. |
| **Network Interface Cards (NICs)** | Allow computers to send/receive signals. |
| **Wi-Fi Antennas** | Transmit and receive radio waves wirelessly. |

---

### 💡 Example

When you plug an Ethernet cable between your computer and a router,  
the **Physical Layer** is the one actually carrying the electrical pulses back and forth —  
representing binary data (`1`s and `0`s) that higher layers will later interpret as meaningful information.

---

### 🧠 Summary

| Key Aspect | Description |
|-------------|-------------|
| **Layer Number** | 1 |
| **Name** | Physical Layer |
| **Type of Data** | Bits (`1` and `0`) |
| **Main Role** | Transmitting data signals physically |
| **Mediums Used** | Cables, wireless waves, fiber optics |
| **Real Examples** | Ethernet cable, Wi-Fi antenna, router port |

---

---

## 🔗 Layer 2 — Data Link Layer 

### ⚙️ Overview

The **Data Link Layer** is the **second layer** in the OSI Model.  
It focuses on how data is **physically addressed** and **transferred** between devices that are directly connected in the same local network.

It takes the raw bits from the **Physical Layer** and organizes them into **frames** — a structure that includes addressing and error-checking information — making communication more reliable and structured.

---

### 🧠 Main Responsibilities

1. **Physical Addressing:**  
   Each device in a local network has a **MAC address** (Media Access Control).  
   This address is **burned into the Network Interface Card (NIC)** by the manufacturer and is unique to that device.  
   - Example: `A4:C3:F0:85:AC:2D`  
   - It tells the network exactly *which device* should receive the data.

2. **Framing:**  
   The Data Link Layer packages data from the **Network Layer** (which contains IP addresses) into **frames** that include:
   - Source MAC address  
   - Destination MAC address  
   - Data payload  
   - Error detection bits (CRC)

3. **Error Detection:**  
   It checks whether the frames were transmitted correctly using techniques like **CRC (Cyclic Redundancy Check)**.

4. **Media Access Control:**  
   This layer also determines *who can use the network medium at a given time* — avoiding data collisions (important in shared networks).

---

### 🧩 Key Concepts

| Term | Description |
|------|--------------|
| **MAC Address** | A unique hardware address used to identify a device on the local network. |
| **NIC (Network Interface Card)** | The hardware component inside every device that connects it to a network and holds its MAC address. |
| **Frame** | The “data packet” format used at the Data Link Layer — includes addressing and error-checking info. |
| **Switch** | A Layer 2 device that uses MAC addresses to forward data to the correct destination within the LAN. |

---

### 💡 Example

When your computer sends a message to another device on the same Wi-Fi or LAN:
1. The **Network Layer** decides the destination IP.  
2. The **Data Link Layer** adds the **MAC address** of that device.  
3. The **Physical Layer** then sends the signal through the cable or wireless channel.

If the data is going outside the local network, it’s sent first to the router’s MAC address (gateway).

---

### 🧾 Summary

| Key Aspect | Description |
|-------------|-------------|
| **Layer Number** | 2 |
| **Name** | Data Link Layer |
| **Main Role** | Physical addressing, framing, and error detection |
| **Unit of Data** | Frame |
| **Key Address** | MAC Address |
| **Hardware Example** | Network Interface Card (NIC), Switch |

---



