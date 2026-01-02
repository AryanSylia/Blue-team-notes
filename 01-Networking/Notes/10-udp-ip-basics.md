---
title: "UDP/IP Basics"
date: 2025-11-17
---

# 📡 UDP/IP — User Datagram Protocol

The **User Datagram Protocol (UDP)** is another protocol used to communicate data between devices.  
Unlike its brother **TCP**, **UDP is stateless**, meaning it does **not require a constant connection** between two devices for data to be transmitted.

Because UDP does not establish a connection, **no Three-Way Handshake** occurs and **no synchronisation** exists between the devices.

UDP is used in situations where applications can tolerate data loss — for example:

- Video streaming
- Voice calls
- Online games
- Real-time communication where speed matters more than reliability

---

## ⚖️ Advantages & Disadvantages of UDP

| Advantages of UDP | Disadvantages of UDP |
|-------------------|----------------------|
| 🚀 **Much faster than TCP** | ❌ Does not care if data is received or not |
| 🧩 Leaves the application to decide how quickly packets are sent | ⚠️ Developers must handle reliability manually |
| 🔓 Doesn't reserve a continuous connection like TCP | 😖 Bad experience on unstable connections |

---

## 📦 UDP Packet Structure

UDP packets are simpler than TCP packets. They contain fewer headers and have no mechanisms for reliability like TCP.

| Header | Description |
|--------|-------------|
| **Time to Live (TTL)** | Prevents packets from staying forever on the network by setting an expiry time. |
| **Source Address** | IP address of the sending device. |
| **Destination Address** | IP address of the receiving device. |
| **Source Port** | Random port selected by the sender (0–65535). |
| **Destination Port** | Port on the destination device where the service is running (e.g., port 80). |
| **Data** | The actual bytes of the file or message being transmitted. |

---

## 🔄 How UDP Communication Works

Since UDP is **stateless**, there is **no acknowledgement (ACK)** sent back.

A typical UDP interaction looks like this:




Alice ---- REQUEST ----> Bob
Alice <--- RESPONSE ---- Bob
Alice <--- RESPONSE ---- Bob
Alice <--- RESPONSE ---- Bob




No verification  
No retransmission  
No handshake  

Just **speed**.

---

## 🧠 Comparison: When to Use UDP?

| Task | Recommended Protocol | Why |
|------|-----------------------|-----|
| File transfer | **TCP** | Reliability is required |
| Video call | **UDP** | Speed > Reliability |

---

## ✅ Quick Review Questions

**1. What does "UDP" stand for?**  
✔️ User Datagram Protocol  

**2. What type of connection is UDP?**  
✔️ Stateless  

**3. What protocol would you use to transfer a file?**  
✔️ TCP  

**4. What protocol is used for video calls?**  
✔️ UDP  

---

## ✔️ Summary

UDP is a **fast**, **simple**, and **connectionless** protocol.  
It offers **no guarantee of delivery**, but is perfect for real-time, low-latency applications.

---

https://www.youtube.com/watch?v=WUrVttiThys


https://youtu.be/2G1ueMDgwxw

