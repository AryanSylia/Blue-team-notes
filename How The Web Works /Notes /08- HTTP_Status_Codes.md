
# HTTP Status Codes
📅 Date: 24/12/2025

---

## Overview

When a client (such as a web browser) sends an HTTP request to a web server, the server responds with an **HTTP Status Code**.  
This status code is always found in the **first line of the HTTP response** and informs the client about the outcome of its request.

HTTP Status Codes are a fundamental part of how browsers, servers, developers, and security professionals understand and handle web communication.

---

## Why HTTP Status Codes Matter

- They tell the browser how to handle the response
- They help developers debug applications
- They reveal application behavior during security testing
- They can expose misconfigurations or vulnerabilities

---

## Status Code Categories

HTTP Status Codes are divided into **five main ranges**, based on the first digit.

---

## 1xx – Informational Responses (100–199)

These codes indicate that the server has received part of the request and the client should continue sending the remainder.

- Rarely used in modern web browsing
- Mostly internal protocol-level communication

Example meaning:
> “I’ve received your request so far, continue.”

---

## 2xx – Success Responses (200–299)

These codes indicate that the request was successfully received, understood, and processed.

### Common Examples

- **200 OK**  
  The request completed successfully and the requested resource was returned.

- **201 Created**  
  A new resource has been successfully created (e.g., a new user, post, or record).

These are the most desirable responses during normal operation.

---

## 3xx – Redirection Responses (300–399)

These codes tell the client that the requested resource has moved and that another request should be made to a different location.

### Common Examples

- **301 Moved Permanently**  
  The resource has been permanently moved to a new URL.

- **302 Found**  
  The resource is temporarily located elsewhere.

Browsers automatically follow these redirects in most cases.

---

## 4xx – Client Error Responses (400–499)

These codes indicate that the problem lies with the **client’s request**.

### Common Examples

- **400 Bad Request**  
  The request is malformed or missing required parameters.

- **401 Not Authorised**  
  Authentication is required to access the resource.

- **403 Forbidden**  
  Access is denied, even if authentication is provided.

- **404 Not Found**  
  The requested resource does not exist.

- **405 Method Not Allowed**  
  The HTTP method used (GET, POST, etc.) is not permitted for this resource.

Client error codes are extremely important in security testing and application analysis.

---

## 5xx – Server Error Responses (500–599)

These codes indicate that the server failed to process a valid request.

### Common Examples

- **500 Internal Server Error**  
  A generic server-side error occurred.

- **503 Service Unavailable**  
  The server is currently unavailable due to overload or maintenance.

Server error codes often point to misconfigurations, crashes, or backend failures.

---

## Quick Mental Map

| Range | Meaning |
|------|--------|
| 1xx  | Information |
| 2xx  | Success |
| 3xx  | Redirection |
| 4xx  | Client Error |
| 5xx  | Server Error |

---

## Security Perspective

From a cybersecurity standpoint, HTTP Status Codes can:
- Reveal hidden endpoints
- Expose authorization issues
- Indicate backend errors
- Assist in vulnerability discovery

Understanding these codes is essential for both defensive and offensive security analysis.

---

## Conclusion

HTTP Status Codes are the **language of communication** between clients and servers.  
Mastering them is a critical step toward understanding web applications, debugging issues, and performing effective security assessments.
