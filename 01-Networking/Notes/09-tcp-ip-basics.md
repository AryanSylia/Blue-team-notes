# 📡 TCP/IP & The Three-Way Handshake  
**Last updated: 2025-11-17**

---

## ## 📘 What Is TCP/IP?

**TCP/IP (Transmission Control Protocol / Internet Protocol)** is a suite of communication protocols used to connect devices across the internet.  
It operates similarly to the OSI model but uses **four layers instead of seven**:

### **TCP/IP Layers**
1. **Application Layer** – Applications such as browsers, email clients, etc.  
2. **Transport Layer** – TCP and UDP  
3. **Internet Layer** – IP addressing and routing  
4. **Network Interface Layer** – Physical and Data Link operations (MAC, frames, cables)

TCP/IP defines how data is packaged, transmitted, addressed, and received across networks.

---

## ## 🔒 TCP: A Reliable Transport Protocol

**TCP is connection-based**, meaning a connection must be established before data is sent.

### Key Features of TCP:
- Ensures data integrity  
- Guarantees ordered delivery  
- Retransmits lost packets  
- Provides flow control and congestion control  

TCP is used by:  
HTTP/HTTPS, SMTP, FTP, SSH, Telnet, etc.

---

## ## 📦 Encapsulation & Decapsulation

When sending data, each layer of the TCP/IP model adds its own **header**.  
This process is called **encapsulation**.

When the data reaches the destination, the headers are removed layer by layer — this is **decapsulation**.

---

## ## 🧱 Structure of a TCP Segment (TCP Header)

TCP packets include several important fields:

| Header | Description |
|--------|-------------|
| **Source Port** | The port number used by the sender to initiate the TCP connection. |
| **Destination Port** | The port where the receiving service is listening (e.g., port 80 for HTTP). |
| **Source IP** | Sender’s IP address. |
| **Destination IP** | Receiver’s IP address. |
| **Sequence Number** | Identifies the starting byte of data sent. Ensures correct ordering. |
| **Acknowledgement Number** | Tells the sender which bytes have been successfully received. |
| **Flags** | Control bits like SYN, ACK, FIN, RST. |
| **Checksum** | Ensures data integrity (detects corruption). |
| **Data** | The actual payload being transmitted. |

---

## ## 🤝 The Three-Way Handshake (Connection Establishment)

To establish a connection, TCP uses **three steps**:

### **1️⃣ SYN — Client → Server**
The client requests to start a connection.  
Includes an **Initial Sequence Number (ISN)**.

### **2️⃣ SYN/ACK — Server → Client**
The server acknowledges the SYN and sends its own ISN.

### **3️⃣ ACK — Client → Server**
The client confirms receipt of the server's SYN.

✔ **Connection is now established** and data transmission can begin.

---

## ## 🔢 Sequence & Acknowledgement Numbers

TCP uses sequence numbers to keep data ordered.

Example:

| Data Sent | Sequence Number | ACK Returned |
|-----------|-----------------|--------------|
| Chunk 1 | 0 | 1 |
| Chunk 2 | 1 | 2 |
| Chunk 3 | 2 | 3 |

ACK = Sequence + 1

This ensures that:
- No data is lost  
- No data is duplicated  
- Data arrives in the correct order  

---

## ## 🔚 Closing a TCP Connection (Four-Way Termination)

TCP uses **four steps** to cleanly close a connection:

### **1️⃣ FIN — Client → Server**
Client requests to end the connection.

### **2️⃣ ACK — Server → Client**
Server acknowledges the FIN.

### **3️⃣ FIN — Server → Client**
Server also signals that it wants to close.

### **4️⃣ ACK — Client → Server**
Client acknowledges: connection is now closed.

This prevents data loss and ensures a clean shutdown.

---

## ## 🟥 RST: Reset Connection

**RST (Reset)** is used to abruptly terminate a connection when something goes wrong.

Examples:
- Application is not listening on that port  
- Connection attempt is invalid  
- System resources are low  

RST is an emergency exit.

---

## ## ✅ Advantages of TCP

- Ensures data integrity  
- Guarantees ordered delivery  
- Retransmits lost packets  
- Synchronizes devices  
- Highly reliable  

---

## ## ❌ Disadvantages of TCP

- Slower than UDP  
- Requires more processing  
- Needs a full connection before sending data  
- Can cause bottlenecks on slow links  

---

## ## 📌 Summary

TCP is the backbone of reliable communication on the internet.  
It ensures:
- connections are established correctly,  
- data arrives in order and without corruption,  
- connections are closed cleanly.

---
 
