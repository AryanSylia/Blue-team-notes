
# HTTP vs HTTPS (Web Basics)

**Date:** 2025-12-24  

---

## Overview

When you browse a website, your browser (client) must communicate with a web server to request and receive web content such as HTML pages, images, videos, CSS, and JavaScript. This communication follows a set of rules called a **protocol**. The protocol used for the web is **HTTP**, and its secure version is **HTTPS**.

---

## What is HTTP? (HyperText Transfer Protocol)

**HTTP** stands for **HyperText Transfer Protocol**.  
It is the standard protocol that defines how a browser and a web server exchange information on the web.

### What HTTP does

When you type a URL into your browser and press Enter, your browser sends an **HTTP request** to a server. The server replies with an **HTTP response** containing the content you asked for.

A simplified flow looks like this:

1. Browser requests a page (HTTP request)
2. Server replies with the page content (HTTP response)
3. Browser renders the content for you

### Why HTTP is not safe

HTTP **does not encrypt** the data being transferred. That means:

- Anyone who can intercept the traffic on the network path (for example, on public Wi-Fi) may be able to **read** the data.
- If the data contains sensitive information (like logins, passwords, session cookies), that information could be exposed.
- Attackers can attempt **Man-in-the-Middle (MITM)** attacks, where they intercept or modify traffic.

In short: **HTTP is plain-text communication**.

---

## What is HTTPS? (HyperText Transfer Protocol Secure)

**HTTPS** stands for **HyperText Transfer Protocol Secure**.  
It is the secure version of HTTP, meaning it adds encryption and trust mechanisms on top of HTTP.

HTTPS works using **TLS** (Transport Layer Security) (historically also known as SSL).

### What HTTPS adds

HTTPS provides three major security benefits:

#### 1) Encryption (Confidentiality)

The data between your browser and the website is **encrypted**.  
Even if someone captures the traffic, they cannot read it easily because it is encrypted.

This protects sensitive information such as:

- Login credentials
- Personal information
- Payment information
- Session cookies (important for authenticated sessions)

#### 2) Authentication (Identity verification)

HTTPS helps ensure your browser is talking to the **real** website/server and not a fake one impersonating it.

This is done using **digital certificates** issued by trusted Certificate Authorities (CAs).  
When a site uses HTTPS properly, the server presents a certificate that proves it owns the domain.

This reduces the risk of:

- Impersonation
- Fake login pages delivered through MITM attacks

#### 3) Integrity (No tampering)

HTTPS helps ensure the data is not modified while travelling between the browser and the server.  
Without integrity protection, an attacker could inject malicious content (like scripts) into a web page while it is being downloaded.

---

## What does the “S” in HTTPS stand for?

The **S** in **HTTPS** stands for:

**Secure**

It indicates the connection is protected using TLS encryption.

---

## Practical example (easy mental model)

### HTTP (not secure)

Think of HTTP like sending a postcard through the mail:

- Anyone handling it can read the message
- The message could be altered

### HTTPS (secure)

Think of HTTPS like sending a locked package:

- People can see you sent a package, but not what is inside
- Tampering is much harder and likely to be detected

---

## Why this matters in Cybersecurity

From a security perspective, HTTP traffic is valuable to attackers because it can expose:

- Credentials (username/password)
- Session tokens/cookies
- Sensitive data transferred by web apps
- Internal information leaked by plain-text requests

Common attacks related to insecure web traffic include:

- **Sniffing** (capturing network traffic)
- **MITM** (intercepting/modifying traffic)
- **Credential theft** on public networks

HTTPS helps reduce these risks, and today it is the standard for modern websites.

---

## Quick comparison table

| Feature | HTTP | HTTPS |
|--------|------|-------|
| Encryption | ❌ No | ✅ Yes (TLS) |
| Safe on public Wi-Fi | ❌ Risky | ✅ Much safer |
| Server identity verification | ❌ No | ✅ Yes (certificates) |
| Data integrity protection | ❌ No | ✅ Yes |
| Recommended today | ❌ No | ✅ Yes |

---

## Key takeaways

- **HTTP** is the basic web communication protocol, but it is **not encrypted**.
- **HTTPS** is HTTP with **TLS security**, providing encryption, authentication, and integrity.
- The **S** in HTTPS means **Secure**.
- In cybersecurity, HTTPS is essential to protect users from interception, impersonation, and data manipulation.

- https://youtu.be/wW2A5SZ3GkI?list=PLJ7Xch9LHhFv6qBHlKEzdwuQo417SYQVO

- https://youtu.be/hExRDVZHhig?list=PLJ7Xch9LHhFv6qBHlKEzdwuQo417SYQVO

---
