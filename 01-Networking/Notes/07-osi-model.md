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

---

## 🌐 Layer 3 — Network Layer 

### ⚙️ Overview

The **Network Layer** is the **third layer** of the OSI Model.  
This is where **routing** and **path selection** happen — the process that decides how packets travel from one network to another.

While the **Data Link Layer** only handles communication inside the same local network (LAN),  
the **Network Layer** connects **different networks** together using logical addressing (IP addresses).

---

### 🧭 Main Responsibilities

1. **Routing (تحديد المسار):**  
   The Network Layer determines the **best path** for data to reach its destination.  
   It uses routing protocols such as:
   - **OSPF (Open Shortest Path First)** — finds the shortest and most efficient path.
   - **RIP (Routing Information Protocol)** — chooses routes based on hop count (number of devices between source and destination).

2. **Forwarding (التوجيه):**  
   Once the route is known, this layer forwards packets through routers and switches that operate at Layer 3.

3. **Logical Addressing (العناوين المنطقية):**  
   Every device is assigned an **IP address** like `192.168.1.100`,  
   which identifies the device’s location within a network or subnet.

---

### ⚙️ How It Works

When your computer (Computer A) sends data to another computer (Computer B) in a **different network**:

1. The **Transport Layer** adds the data segment.  
2. The **Network Layer** adds the **source and destination IP addresses**.  
3. Routers analyze these IP addresses and decide the most optimal route.  
4. The data travels through one or more routers until it reaches its destination.

---

### 🔍 Route Decision Factors

Routing protocols decide the path based on:

- **Shortest path:** Fewer intermediate devices (hops).  
- **Most reliable path:** Fewer packet losses in the past.  
- **Fastest path:** Fiber optics (faster) vs copper cables (slower).

---

### 🧩 Key Components

| Component | Description |
|------------|-------------|
| **Router** | The main Layer 3 device — directs data based on IP addresses. |
| **Layer 3 Switch** | An advanced switch that can also perform routing functions. |
| **IP Address** | Logical address used to identify devices across different networks. |
| **Packet** | The data unit used at this layer. |

---

### 💡 Example

Imagine **Computer A** (192.168.1.10) wants to send data to **Computer B** (192.168.2.10).  
Since they belong to different networks, the data must pass through a **Router**,  
which examines its routing table and sends the packet through the **best available path**.

---

### 🧾 Summary

| Key Aspect | Description |
|-------------|-------------|
| **Layer Number** | 3 |
| **Name** | Network Layer |
| **Main Role** | Routing and inter-network communication |
| **Unit of Data** | Packet |
| **Address Type** | IP Address |
| **Devices** | Routers, Layer 3 Switches |
| **Protocols** | OSPF, RIP |

---

---

## 🚚 Layer 4 — Transport Layer 

### ⚙️ Overview

The **Transport Layer** is the **fourth layer** of the OSI Model and plays a critical role in how data is transmitted between devices.  
While the **Network Layer** decides *where* data should go, the **Transport Layer** determines *how* the data should be delivered — reliably, efficiently, or quickly.

This layer breaks large amounts of data into smaller units called **segments**, ensuring that information reaches the correct application in the right order.

---

### 📦 Main Protocols

The Transport Layer primarily uses two protocols:

#### 🔹 1. TCP (Transmission Control Protocol)

**TCP** ensures reliability and accuracy when transferring data between devices.  
It is a **connection-oriented** protocol — meaning it establishes a stable connection between devices before sending data and ensures that every packet arrives safely and in the right order.

##### ✅ Advantages of TCP:
- Guarantees the **accuracy and integrity** of data.  
- Performs **error checking and recovery** if data is lost.  
- Synchronizes devices to ensure correct sequencing.  
- Ideal for tasks where **all data must arrive complete**.

##### ❌ Disadvantages of TCP:
- Requires a **constant connection**, which can slow down performance.  
- **Slower** than UDP due to error-checking overhead.  
- Can cause **network congestion** if multiple sessions are open.

##### 🧩 Common Uses:
- File downloads (FTP)  
- Web browsing (HTTP, HTTPS)  
- Email (SMTP, POP3, IMAP)

---

#### 🔹 2. UDP (User Datagram Protocol)

**UDP** is a **connectionless** protocol — it sends data directly without establishing a connection or verifying delivery.  
It sacrifices reliability for **speed and efficiency**, making it ideal for real-time applications.

##### ✅ Advantages of UDP:
- Much **faster** than TCP.  
- Doesn’t require a constant connection.  
- Allows small data packets to be sent quickly and efficiently.

##### ❌ Disadvantages of UDP:
- Does **not check** if the data arrived.  
- Packets may be **lost or out of order**.  
- No re-transmission or confirmation.

##### 🧩 Common Uses:
- Video and audio streaming (Netflix, YouTube, Spotify)  
- Online gaming  
- Device discovery protocols (ARP, DHCP)

---

### 🖥️ Example Visualization

#### 🔸 TCP Example:
When sending an image from a **webserver** to a **computer**, the image is split into multiple packets:

Packet #1 ➜ Packet #2 ➜ Packet #3 ➜ Final (Full Image)

The receiver reassembles them in the correct order.  
If one packet is missing, TCP requests it again until the entire image is complete.

#### 🔸 UDP Example:
The same image sent via UDP might lose some packets:

The receiver shows what it received — even if it’s incomplete — prioritizing **speed over accuracy**.

---

### 🧾 Summary

| Aspect | TCP | UDP |
|--------|-----|-----|
| **Connection Type** | Connection-oriented | Connectionless |
| **Reliability** | High (guaranteed delivery) | Low (no delivery check) |
| **Speed** | Slower | Faster |
| **Error Checking** | Yes | No |
| **Best For** | File transfers, web browsing, emails | Streaming, gaming, voice/video calls |
| **Data Unit** | Segment | Datagram |

---

---

## 🟦 Layer 5 — Session Layer 

**Date:** 2025-11-17  

### 🧭 Overview

The **Session Layer** is the **fifth layer** of the OSI Model.  
This layer is responsible for **creating, maintaining, and terminating sessions** between two devices communicating over a network.

A *session* represents the logical connection between two systems while they exchange data.

Whenever an application on one device needs to communicate with another device, the Session Layer establishes a session and manages all communication within it.

---

### 🔗 What the Session Layer Does

#### 1️⃣ Session Establishment  
When communication begins, Layer 5 creates a session to allow data exchange.  
Examples: opening a website, starting a video call, connecting to a remote server (SSH).

#### 2️⃣ Session Maintenance   
While the connection is active, the Session Layer:
- Keeps the session alive  
- Resets the connection if necessary  
- Uses **Checkpoints** to resume data transfer without restarting  
- Ensures only *new* data is resent if something is interrupted

#### 3️⃣ Session Termination 
When communication ends, the session is closed properly to free up resources and prevent errors.

---

### 🧱 Key Features

| Feature | Description |
|--------|-------------|
| **Session Creation** | Establishes communication between devices |
| **Session Maintenance** | Keeps the connection alive and stable |
| **Checkpoints** | Allows resuming transfers after interruptions |
| **Session Uniqueness** | Each session is independent and isolated |
| **Efficient Bandwidth** | Only new/resumed data is transmitted |

---

### 🧪 Examples of Where Session Layer Is Used
- Video calls (Zoom, WhatsApp, Teams)  
- Remote access sessions (SSH, RDP)  
- File transfers that support resume  
- Website login sessions (Session IDs)  

---

### 📌 Summary

| Element | Value |
|--------|--------|
| **Layer Number** | 5 |
| **Name** | Session Layer |
| **Main Function** | Create, maintain, terminate sessions |
| **Key Feature** | Checkpointing and session control |
| **Responsible For** | Logical communication between applications |

---

---

## 🟩 Layer 6 — Presentation Layer 

### 🧭 Overview

The **Presentation Layer** is the **sixth layer** of the OSI Model.  
Its main purpose is to ensure that data can be **understood**, **formatted**, and **used correctly** by the receiving system — no matter what software or hardware is being used.

This layer acts as a **translator** for data moving between the Application Layer (Layer 7) and the lower layers of the OSI model.  
It ensures that data sent from one device in a certain format can be received and displayed correctly on another device that may use a different format.

Security-related features such as **data encryption** (e.g., HTTPS) also occur in this layer.

---

### 🔑 Key Responsibilities

#### 1️⃣ Translation
- Converts data between different formats  
- Ensures different applications can understand each other  
- Example: Opening an email in Gmail vs Outlook

#### 2️⃣ Compression 
- Reduces the size of data to improve speed  
- Used for images, video streams, and file transfers

#### 3️⃣ Encryption
- Protects data during transmission  
- HTTPS encryption is performed here  
- Ensures confidentiality and integrity

#### 4️⃣ Standardisation 
- Makes sure all data uses a unified structure  
- Allows different systems to exchange information without issues

---

### 🧪 Examples of Presentation Layer Functions
- Encrypting communication on secure websites (HTTPS)  
- Compressing video/audio for streaming  
- Converting character sets (ASCII ↔ Unicode)  
- Ensuring emails display correctly on any client  

---

### 📌 Summary

| Element | Value |
|--------|--------|
| **Layer Number** | 6 |
| **Name** | Presentation Layer |
| **Main Functions** | Translation, Encryption, Compression |
| **Purpose** | Ensuring data is readable and secure |
| **Related to** | HTTPS, encoding, file formats |

---

---

## 🟣 Layer 7 — Application Layer (طبقة التطبيقات)

### ⚙️ Overview  
The **Application Layer** is the **seventh and highest layer** of the OSI Model.  
It is the layer that users interact with directly through applications such as web browsers, email clients, or file transfer tools.  

This layer does **not** refer to the applications themselves, but rather to the **protocols and rules** that those applications use to communicate across the network.

Its main job is to ensure that applications can correctly **send, receive, and interpret** data using standardized protocols.

---

### 🧩 Key Responsibilities  
- Provides a **user interface** (GUI or CLI) for interacting with network services.  
- Defines the **protocols** that applications use to communicate.  
- Manages **application-specific data formats**.  
- Ensures that data displayed to the user is **understandable and consistent**.  
- Handles services like emailing, browsing, file transfers, remote access, and more.

---

### 📡 Common Protocols in the Application Layer

| Protocol | Purpose |
|---------|---------|
| **HTTP / HTTPS** | Browsing websites |
| **DNS** | Translating domain names into IP addresses |
| **FTP / SFTP** | Transferring files between devices |
| **SMTP** | Sending email |
| **IMAP / POP3** | Receiving email |
| **SSH / Telnet** | Remote device access |
| **LDAP** | Directory services |
| **SNMP** | Network device monitoring |

---

### 🖥️ User Interaction  
The Application Layer is the closest to the user:

- **GUI applications**:  
  Web browsers (Chrome, Firefox), email clients (Outlook, Thunderbird), FTP tools (FileZilla).

- **CLI tools**


