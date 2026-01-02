
# HTTP Headers – Request & Response Explained
**Date:** 24/12/2025  
**Category:** Web Fundamentals / HTTP  
**Source:** TryHackMe – Web Fundamentals  

---

## Overview

HTTP Headers are additional pieces of information sent between a **client** (usually a web browser) and a **server** during an HTTP request/response cycle.  
They provide context about the request, describe the client, control caching, manage sessions, and tell the browser how to process the returned data.

Technically, an HTTP request can be sent without headers, but in practice, most modern websites will not function correctly without them.

---

## Request Headers (Client → Server)

Request headers are sent by the client to inform the server **who is making the request**, **what is being requested**, and **how the response should be handled**.

### Host
The most critical request header.

- Identifies which website the client wants to access.
- Required because a single server can host multiple websites (virtual hosting).
- Without it, the server may return a default or incorrect site.

Example:
Host: tryhackme.com


---

### User-Agent
Identifies the client software.

- Browser name and version
- Operating system
- Device type (in some cases)

Used by servers to:
- Adjust content for compatibility
- Enable/disable features for certain browsers

Example:
User-Agent: Mozilla/5.0 (Windows NT 10.0; Firefox/87.0)


---

### Content-Length
Specifies the size of the request body in bytes.

- Used mainly with POST and PUT requests.
- Allows the server to know how much data to expect.
- Prevents incomplete or malformed data submissions.

---

### Accept-Encoding
Tells the server which compression formats the client supports.

Common values:
- gzip
- deflate
- br

Purpose:
- Reduce data size
- Improve loading speed

---

### Cookie
Sends stored data back to the server.

Used for:
- Session management
- Authentication
- User preferences

Example:
Cookie: sessionid=abc123


---

## Response Headers (Server → Client)

Response headers are sent by the server to describe the returned content and instruct the browser on how to handle it.

---

### Set-Cookie
Instructs the browser to store a cookie.

- Sent once by the server
- Automatically included in future requests

Used for:
- Login sessions
- User tracking
- Persistent preferences

Example:
Set-Cookie: sessionid=xyz789


---

### Cache-Control
Controls how long a response can be cached by the browser.

- Improves performance
- Reduces unnecessary requests
- Prevents serving outdated content

---

### Content-Type
Describes the type of data being returned.

Examples:
- text/html
- application/json
- image/png
- application/pdf

This header tells the browser **how to interpret and display the content**.

Example:
Content-Type: text/html


---

### Content-Encoding
Indicates how the response body is compressed.

Common value:
Content-Encoding: gzip


The browser automatically decompresses the data before rendering it.

---

## Conceptual Summary

Think of HTTP Headers as a conversation:

**Client says:**
- I am Firefox
- I want tryhackme.com
- I support gzip compression
- Here is my session cookie

**Server replies:**
- Here is HTML content
- It is compressed
- Cache it for a short time
- Store this new cookie

---

## Why Headers Matter in Cybersecurity

Headers are critical because:

- Manipulating headers can lead to attacks
- Missing headers can expose vulnerabilities
- Cookies are directly tied to session hijacking
- User-Agent spoofing can bypass restrictions
- Cache misconfiguration can leak sensitive data

Understanding headers is essential for:
- Web exploitation
- Bug bounty hunting
- Penetration testing
- Secure web development

---

## Key Takeaway

HTTP Headers are not optional details —  
they are **core components of how the web works** and a **major attack surface** in web security.

https://www.youtube.com/watch?v=4bQeGUzHpOE
