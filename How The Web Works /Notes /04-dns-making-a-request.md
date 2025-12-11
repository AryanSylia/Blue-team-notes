
# 🌐 DNS – Making a Request  
### 📅 Updated: 2025-12-11  

This note explains, step-by-step, what happens when a DNS request is made.  
A DNS request involves multiple servers working together to convert a human-friendly domain name into a machine-friendly IP address.

---

## 🧠 Introduction  
Computers do not understand domain names like `www.tryhackme.com`.  
They communicate using IP addresses such as `104.26.10.229`.  

DNS (Domain Name System) acts as the internet’s phonebook.  
Whenever you request a domain, your device starts a multi-step resolution journey.

---

# 🟩 1. Local DNS Cache – (Your Computer)  
When a domain name is requested, your computer first checks its **local DNS cache**.

- ✔ If the address is found locally → it immediately returns the IP.  
- ❌ If not → the request is forwarded to the **Recursive DNS Server**.

Caching speeds up browsing by avoiding repeated lookups.

---

# 🟦 2. Recursive DNS Server – (Usually Your ISP or Public DNS)  
If the IP is not found locally, the query is sent to a **Recursive DNS Server**, commonly from:

- Your ISP  
- Google DNS (`8.8.8.8`)  
- Cloudflare DNS (`1.1.1.1`)  

This server also maintains its own DNS cache.

- ✔ If found → the IP is returned to your device.  
- ❌ If not → the recursive server starts a full DNS lookup on your behalf.

---

# 🟥 3. Root DNS Server  
The recursive DNS server queries a **Root DNS Server**, the highest authority in the DNS hierarchy.

The root server does **not** return the final IP.  
Instead, it directs the recursive server to the appropriate **Top-Level Domain (TLD) server**, based on the domain extension.

Example:  
Request for `tryhackme.com` → Root server points to `.com` TLD servers.

---

# 🟨 4. TLD DNS Server – (Top Level Domain Server)  
TLD servers manage domain extensions such as:

| TLD | Purpose |
|-----|---------|
| .com | Commercial |
| .net | Network |
| .org | Organizations |
| .edu | Education |
| .gov | Government |
| .mil | Military |

The recursive server asks the `.com` TLD server:  
> “Who is the authoritative DNS server for tryhackme.com?”

The TLD server replies with the **nameservers**, e.g.:

- `kip.ns.cloudflare.com`  
- `uma.ns.cloudflare.com`

---

# 🟧 5. Authoritative DNS Server – (Final Answer Source)  
This server stores all DNS records for the domain, including:

- A / AAAA  
- CNAME  
- MX  
- TXT  
- NS  

The recursive DNS server asks:  
> “What is the IP address for tryhackme.com?”

The authoritative server responds with the official IP, such as:  
`104.26.10.229`.

---

# 🔁 6. Response, Caching & TTL  
After the recursive server receives the answer:

1. It **caches** the record based on TTL (Time To Live).  
2. It sends the final answer back to your device.  
3. Your device then **caches** the answer locally.  
4. Your browser uses the IP to connect to the correct web server.

**TTL** defines how long the answer remains cached (in seconds).

---

# 🔍 Full DNS Resolution Flow  

User Device
↓
Local DNS Cache
↓
Recursive DNS Server
↓
Root DNS Server
↓
TLD DNS Server (.com, .net, .org...)
↓
Authoritative DNS Server
↓
Final Answer (IP Address)


---

# 🧩 Key Concepts Summary  

### ✔ Recursive DNS  
Performs the entire lookup process on behalf of the user.

### ✔ Authoritative DNS  
Stores the official DNS records for a domain.

### ✔ TTL (Time To Live)  
Defines how long a DNS record is allowed to stay cached.

### ✔ DNS Caching  
Improves browsing speed and reduces global DNS traffic.

---

# 🏁 Final Notes  
Understanding DNS is essential for:

- Cybersecurity  
- Networking  
- Pentesting  
- System administration  
- Blue & Red team operations  

This knowledge prepares you for advanced topics like DNS poisoning, enumeration, and secure DNS practices.

---
