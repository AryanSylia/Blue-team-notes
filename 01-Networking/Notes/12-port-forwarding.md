
---
date: 2025-11-18
---

# 🌐 Port Forwarding — Extending Your Network

Port forwarding is an essential technique that allows devices and services inside a private network to be accessed from the public Internet. Without port forwarding, internal servers (such as a web server, game server, or FTP server) remain accessible **only** to devices inside the same LAN.

---

## 🔎 What Problem Does Port Forwarding Solve?

Private networks use internal IP address ranges such as:

- 192.168.x.x  
- 10.x.x.x  
- 172.16.x.x – 172.31.x.x  

These addresses are *not routable on the Internet*.  
Only the router has a **public IP address**, which is exposed to the outside world.

If a server inside the network (e.g., 192.168.1.10 on port 80) hosts a website, users from the Internet cannot reach it directly because:

> The server has no public IP.  
> The router receives all external traffic first.

This is where port forwarding is used.

---

## 🚀 How Port Forwarding Works

Port forwarding tells the router:

> “When you receive external traffic on port X, forward it to internal device Y on port Z.”

Example:

- Public request: `82.62.51.70:80`  
- Router forwards to: `192.168.1.10:80`

Now external users can reach the internal web server.

---

## 🖥️ Example Scenario (from the diagrams)

### Inside Network #1:
- Web server: **192.168.1.10**
- Running on: **Port 80**

Only computers inside Network #1 can access it.

### Network #2:
- Users in this network want to access the web server.

### With Port Forwarding:
The router in Network #1 is configured like this:

---
title: Port Forwarding — Extending Your Network
date: 2025-03-18
---

# 🌐 Port Forwarding — Extending Your Network

Port forwarding is an essential technique that allows devices and services inside a private network to be accessed from the public Internet. Without port forwarding, internal servers (such as a web server, game server, or FTP server) remain accessible **only** to devices inside the same LAN.

---

## 🔎 What Problem Does Port Forwarding Solve?

Private networks use internal IP address ranges such as:

- 192.168.x.x  
- 10.x.x.x  
- 172.16.x.x – 172.31.x.x  

These addresses are *not routable on the Internet*.  
Only the router has a **public IP address**, which is exposed to the outside world.

If a server inside the network (e.g., 192.168.1.10 on port 80) hosts a website, users from the Internet cannot reach it directly because:

> The server has no public IP.  
> The router receives all external traffic first.

This is where port forwarding is used.

---

## 🚀 How Port Forwarding Works

Port forwarding tells the router:

> “When you receive external traffic on port X, forward it to internal device Y on port Z.”

Example:

- Public request: `82.62.51.70:80`  
- Router forwards to: `192.168.1.10:80`

Now external users can reach the internal web server.

---

## 🖥️ Example Scenario (from the diagrams)

### Inside Network #1:
- Web server: **192.168.1.10**
- Running on: **Port 80**

Only computers inside Network #1 can access it.

### Network #2:
- Users in this network want to access the web server.

### With Port Forwarding:
The router in Network #1 is configured like this:

Public IP: 82.62.51.70
Forward incoming port 80 → 192.168.1.10:80


Now Network #2 (or any external user) can reach the server by visiting:

http://82.62.51.70


---

## 🔥 Port Forwarding vs. Firewall

These two are often confused but serve different purposes:

### Port Forwarding:
- Opens specific ports and routes traffic inside the network.

### Firewall:
- Controls whether the traffic is allowed or blocked.
- Even if port forwarding is configured, the firewall may still block the connection.

---

## ⚙️ Where Is Port Forwarding Configured?

✔ **Port forwarding is always configured on the router**  
This is the device that handles NAT and manages public-to-private traffic.

---

## 🛡️ Security Considerations

Opening ports exposes internal services to the Internet.  
To stay secure:

- Only forward ports you *absolutely* need.
- Use Firewalls.
- Use encrypted protocols (HTTPS, SSH, SFTP).
- Ensure the internal service is patched and secure.

---

## 📌 Summary

Port forwarding enables:

- Public access → to private network services
- By forwarding traffic → from the router’s public IP  
- To a specific internal device and port

It is a foundational networking skill and widely used in:

- Self-hosting
- Game servers
- Remote access
- Security testing
- Web hosting
- IoT devices

---



