
# How Websites Work — Introduction

📅 Date: 25/12/2025  
📘 Topic: Web Fundamentals — How Websites Work  
🎯 Level: Beginner  
📌 Source: Practical Web Fundamentals (Cybersecurity Path)

---

## Overview

This lesson explains how websites work at a fundamental level by describing the interaction between a user's browser and a web server.  
By the end of this section, you should understand how a web page is requested, processed, and displayed.

---

## What Happens When You Visit a Website?

When you visit a website (for example, by typing a URL into your browser), a communication process begins between your device and a remote server.

1. You enter a website address (URL) into your browser.
2. The browser sends a **request** over the Internet.
3. The request reaches a **web server**.
4. The server processes the request.
5. The server sends back a **response**.
6. The browser renders the response into a visible webpage.

This entire process usually happens in a fraction of a second.

---

## The Role of the Browser

A **browser** (such as Chrome, Safari, or Firefox) is responsible for:

- Sending requests to servers
- Receiving responses
- Interpreting the returned data
- Displaying the webpage to the user

The browser does not store the website itself — it only asks for it when needed.

---

## The Role of the Web Server

A **web server** is a dedicated computer located somewhere in the world. Its job is to:

- Listen for incoming requests
- Process those requests
- Send back responses (HTML, CSS, JavaScript, data, etc.)

The server does not know who you are unless additional mechanisms (like cookies or sessions) are used.

---

## The Internet’s Role

The Internet acts as a **transport layer**:

- It carries requests from the browser to the server
- It carries responses from the server back to the browser

It does not interpret the data — it only transfers it.

---

## Main Components of a Website

A website is made up of two major components:

### 1. Front End (Client-Side)

- Runs in the browser
- Responsible for what the user sees
- Includes HTML, CSS, and JavaScript
- Handles layout, design, and interaction

### 2. Back End (Server-Side)

- Runs on the server
- Processes requests
- Handles logic, authentication, and databases
- Sends responses back to the browser

---

## Key Concept

Every website interaction follows a simple principle:

**Request → Process → Response**

The browser always asks, and the server always answers.

---

## Key Summary

Websites work by allowing browsers to communicate with servers over the Internet.  
The browser requests data, the server responds with data, and the browser renders that data into a webpage visible to the user.

This fundamental concept is the foundation for everything else in web development and web security.
