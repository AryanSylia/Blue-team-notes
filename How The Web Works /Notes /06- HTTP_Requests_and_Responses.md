
# 🌐 HTTP Requests and Responses
**Date:** 24/12/2025  
**Category:** Web Fundamentals / Networking  
**Source:** Practical Web Concepts (TryHackMe Style Notes)

---

## 🧠 Overview

The web works on a very simple but powerful concept:  
**a client sends a request, and a server sends back a response.**

Every time you open a website, download an image, or interact with an API, this exact process happens behind the scenes using the **HTTP protocol**.

This document explains:
- What a URL is
- How HTTP requests are made
- How servers respond
- How to read and understand real HTTP traffic

---

## 🔗 What is a URL? (Uniform Resource Locator)

A URL is not just an address — it is a **set of instructions** that tells the browser:
- **Which protocol** to use
- **Which server** to contact
- **Which resource** to request
- **What extra data** to send

### Example URL

# 🌐 HTTP Requests and Responses
**Date:** 24/12/2025  
**Category:** Web Fundamentals / Networking  
**Source:** Practical Web Concepts (TryHackMe Style Notes)

---

## 🧠 Overview

The web works on a very simple but powerful concept:  
**a client sends a request, and a server sends back a response.**

Every time you open a website, download an image, or interact with an API, this exact process happens behind the scenes using the **HTTP protocol**.

This document explains:
- What a URL is
- How HTTP requests are made
- How servers respond
- How to read and understand real HTTP traffic

---

## 🔗 What is a URL? (Uniform Resource Locator)

A URL is not just an address — it is a **set of instructions** that tells the browser:
- **Which protocol** to use
- **Which server** to contact
- **Which resource** to request
- **What extra data** to send

### Example URL

http://user:password@tryhackme.com:80/view-room?id=1#task3


---

## 🧩 URL Components Explained

### 1️⃣ Scheme
http://

Defines the protocol used for communication.

Common schemes:
- HTTP
- HTTPS
- FTP

---

### 2️⃣ User (Optional / Deprecated)
user:password@

Used historically for authentication in URLs.  
⚠️ Rarely used today due to security risks.

---

### 3️⃣ Host / Domain
tryhackme.com

The domain name or IP address of the server.

---

### 4️⃣ Port
:80

Specifies the service port on the server.

Common ports:
- HTTP → 80
- HTTPS → 443

---

### 5️⃣ Path
/view-room

Indicates the specific resource or file requested.

---

### 6️⃣ Query String
?id=1

Extra data sent to the server to modify behavior or results.

---

### 7️⃣ Fragment
#task3

Used **only by the browser**, never sent to the server.  
Points to a specific section inside a page.

---

## 📤 Making an HTTP Request

The simplest HTTP request looks like this:

GET / HTTP/1.1


Meaning:
- `GET` → request method
- `/` → requested path
- `HTTP/1.1` → protocol version

---

## 🧾 Example HTTP Request

GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/


### Request Breakdown

- **Line 1:** Request method, path, and HTTP version  
- **Host:** Specifies which website is being requested  
- **User-Agent:** Identifies the client browser and OS  
- **Referer:** Shows the page that initiated the request  

📌 All HTTP requests end with a **blank line** to indicate completion.

---

## 📥 HTTP Response

After receiving a request, the server processes it and returns a response.

### Example HTTP Response

HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98
<html> <head> <title>TryHackMe</title> </head> <body> Welcome To TryHackMe.com </body> </html> ```


📊 Response Breakdown
Line 1 – Status Line

HTTP/1.1 200 OK

HTTP version
Status code (200 = Success)
Common status codes:
200 → OK
301 → Redirect
403 → Forbidden
404 → Not Found
500 → Server Error

Server
Server: nginx/1.15.8
Web server software and version.

Date: Fri, 09 Apr 2021 13:34:03 GMT
Time the response was generated.

Content-Type: text/html
Defines the type of data returned:
HTML
JSON
Image
PDF

Content-Length: 98
Size of the response body in bytes.

Blank Line
Separates headers from the response body.
Body
The actual content requested by the client (HTML, data, file, etc.).

🔁 Request–Response Flow Summary
Browser
  ↓
HTTP Request
  ↓
Web Server
  ↓
HTTP Response
  ↓
Browser Renders Content


🎯 Why This Matters (Security Perspective)
Understanding HTTP requests and responses is essential for:
Web application security
API testing
Burp Suite & Wireshark analysis
Web exploitation and pentesting
Debugging and performance analysis
Every web vulnerability starts with how requests are formed and how responses are handled.

✅ Key Takeaways
URLs instruct the browser how to access resources
HTTP requests ask for data
HTTP responses deliver data
Headers carry metadata
The body contains actual content
Everything on the web relies on this model







