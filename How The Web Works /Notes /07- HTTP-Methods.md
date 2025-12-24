
# HTTP Methods  
📅 Date: 24/12/2025  

---

## Overview

HTTP Methods define the **action** that the client (browser, application, script) wants to perform when communicating with a web server.  
While the URL specifies **where** the request is sent, the HTTP method specifies **what should be done**.

These methods are a fundamental part of how the web works and are critical to understand in networking, web development, and cybersecurity.

---

## Common HTTP Methods

Although many HTTP methods exist, the most commonly used ones are **GET**, **POST**, **PUT**, and **DELETE**.

---

## GET Method

### Description
The **GET** method is used to retrieve information from a web server.  
It does **not** modify any data on the server.

### Common Uses
- Loading web pages
- Fetching images, CSS, JavaScript files
- Reading data from an API

### Characteristics
- Data can be sent via the URL (query string)
- Requests can be cached
- Requests appear in browser history
- Not suitable for sensitive data

### Conceptual Meaning
> "Give me this resource."

---

## POST Method

### Description
The **POST** method is used to send data to a web server, usually to create a new resource or submit information.

### Common Uses
- User registration
- Login forms
- Submitting contact forms
- Creating new records in a database

### Characteristics
- Data is sent in the request body
- Not stored in browser history
- Not cached by default
- More secure than GET for sensitive data

### Conceptual Meaning
> "Here is some data, process it and store it."

---

## PUT Method

### Description
The **PUT** method is used to update or replace existing data on the server.

### Common Uses
- Updating a user profile
- Changing account details
- Modifying existing records

### Characteristics
- Requires the resource to already exist
- Sends complete updated data
- Often used in RESTful APIs

### Conceptual Meaning
> "Update this existing resource with new data."

---

## DELETE Method

### Description
The **DELETE** method is used to remove a resource from the server.

### Common Uses
- Deleting user accounts
- Removing posts or comments
- Cleaning database entries

### Characteristics
- Can permanently remove data
- Usually protected by authentication and authorization
- Dangerous if misconfigured

### Conceptual Meaning
> "Remove this resource completely."

---

## Summary Table

| Method  | Purpose                     |
|--------|-----------------------------|
| GET    | Retrieve data               |
| POST   | Create or submit data       |
| PUT    | Update existing data        |
| DELETE | Remove data                 |

---

## Security Perspective

Understanding HTTP methods is essential in cybersecurity because:
- Misconfigured methods can lead to vulnerabilities
- Unauthorized PUT or DELETE requests can cause data loss
- APIs may expose sensitive functionality without proper controls
- Many web attacks rely on abusing HTTP methods

---

## Final Notes

HTTP methods define **intent**.  
Correct usage ensures functionality, while incorrect or insecure usage can expose serious security risks.

Mastering these concepts is essential for:
- Web security testing
- API analysis
- Penetration testing
- Defensive security engineering
