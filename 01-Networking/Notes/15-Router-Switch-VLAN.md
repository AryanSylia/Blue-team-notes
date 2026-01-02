
# LAN Networking Devices (Routers, Switches, VLANs)
### Date: **19 November 2025**

---

## 🧭 1. What is a Router?

A **router** is a networking device responsible for connecting different networks and forwarding data between them. It determines the best possible path for the data to travel from one network to another.

Routers operate at **Layer 3** of the OSI model and make decisions using **IP addresses**.

### **Router Responsibilities**
- Connect multiple networks together  
- Forward packets based on IP addresses  
- Choose the most optimal path based on metrics such as:  
  - Shortest path  
  - Most reliable route  
  - Fastest medium (copper vs. fiber)  
  - Network congestion  
- Handle routing features such as port forwarding and firewalling

- https://youtu.be/ELCPzcOTkYg

---

## 🧩 2. What is a Switch?

A **switch** is a dedicated networking device used to connect multiple devices inside the same network. It forwards traffic to the correct device using its **MAC address**.

Switches can operate at:
- **Layer 2** (standard switch using MAC addresses)  
- **Layer 3** (advanced switch capable of routing using IP)
- 
- https://youtu.be/WJ_UD3R7s2I

---

## 🔵 3. Layer 2 Switch

A Layer 2 switch:
- Operates at the **Data Link layer (Layer 2)**
- Uses **MAC addresses** to forward frames  
- Cannot route packets  
- Connects multiple devices inside the same LAN  

Layer 2 switches are ideal for:
- Home networks  
- Office departments  
- Simple LAN environments  

---

## 🟣 4. Layer 3 Switch

A Layer 3 switch:
- Operates at **both Layer 2 and Layer 3**  
- Can perform routing functions similar to a router  
- Uses both **MAC addresses** (Layer 2) and **IP addresses** (Layer 3)

These switches are common in large organizations that require high-speed internal routing.

---

## 🟡 5. VLAN (Virtual Local Area Network)

A **VLAN** divides a physical network into multiple logical networks.  
Even though devices are connected to the same switch, VLANs separate them logically.

### **Benefits of VLANs**
- Improves security by isolating departments  
- Reduces broadcast traffic  
- Organizes the network efficiently  
- Allows multiple virtual networks on one physical switch  

### **Example**
- **VLAN 1:** Sales Department  
- **VLAN 2:** Accounting Department  

These departments **cannot communicate** with each other unless routing rules allow it.


https://youtu.be/jC6MJTh9fRE

---

## 🧾 Summary Table

| Device | OSI Layer | Purpose |
|--------|-----------|---------|
| **Router** | Layer 3 | Connects different networks using IP |
| **Layer 2 Switch** | Layer 2 | Connects devices within the same LAN using MAC |
| **Layer 3 Switch** | Layer 2 & 3 | Performs switching + routing |
| **VLAN** | Layer 2 | Logical network separation for better security & organization |

---

## 📌 Key Terms

Router → Forwards packets between networks using IP
Switch → Forwards frames inside the same network using MAC
VLAN → Logical segmentation inside a switch
Layer 3 Switch → Hybrid of switch + router

