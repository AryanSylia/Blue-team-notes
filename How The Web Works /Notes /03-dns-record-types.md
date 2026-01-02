
# 📘 DNS Record Types  
**Updated: 2025-12-08**

This document explains the most common DNS record types used on the internet. Each DNS record type serves a specific purpose in translating domain names into information required for communication across networks.

---

## 🅰️ A Record
**Purpose:** Maps a domain name to an IPv4 address.

**Example:**
tryhackme.com → 104.26.10.229

Used when a domain needs to point to a server using an IPv4 address.

---

## 🅰️🅰️🅰️🅰️ AAAA Record
**Purpose:** Maps a domain name to an IPv6 address.

**Example:**
example.com → 2606:4700:20::681a:be5

Used for modern networks that support IPv6 addressing.

---

## 🔁 CNAME Record (Canonical Name)
**Purpose:** Points one domain name to another domain name instead of an IP address.

**Example:**
store.tryhackme.com → shops.shopify.com


When a user visits **store.tryhackme.com**, the DNS server follows the CNAME and then resolves **shops.shopify.com** to its IP address.

**Why it's used:**
- Easier domain management  
- Avoids repeating the same IP in many places  
- If the destination IP changes, only the main domain needs updating  

---

## 📧 MX Record (Mail Exchange)
**Purpose:** Specifies the mail servers responsible for receiving emails for a domain.

**Example response for tryhackme.com:**
alt1.aspmx.l.google.com (priority 10


**Priority value:**  
- Lower number = higher priority  
- Email clients try servers in order of priority  

**Use case:**
If the primary mail server is down, email delivery automatically switches to the backup server.

---

## 📝 TXT Record
**Purpose:** Stores arbitrary human-readable text.  
TXT records have multiple use cases, especially for **security and verification**.

### Common uses:
- **SPF** (Sender Policy Framework): Prevents email spoofing  
- **DKIM**: Secures email using cryptographic signatures  
- **Domain ownership verification:** Required by Google, Microsoft, Cloudflare, etc.  
- **Service configuration:** Like proving domain ownership for APIs or SaaS platforms  

**Example:**
"v=spf1 include:_spf.google.com ~all"


---

## 📚 Summary Table

| Record Type | Purpose | Example |
|-------------|---------|---------|
| **A** | Maps domain → IPv4 | 104.26.10.229 |
| **AAAA** | Maps domain → IPv6 | 2606:4700:20::681a:be5 |
| **CNAME** | Points domain → another domain | store.tryhackme.com → shops.shopify.com |
| **MX** | Email handling servers | alt1.aspmx.l.google.com |
| **TXT** | Text data (SPF, DKIM, verification) | "v=spf1 include:_spf.google.com ~all" |

---

## 🗒️ Notes  
This file is part of the DNS learning series inside the *Notes / Network* directory.

Related files:
- `dns-basics.md`  
- `dns-domains-hierarchy.md`  
- `dns-record-types.md` *(this file)*

---

https://youtu.be/HnUDtycXSNE
