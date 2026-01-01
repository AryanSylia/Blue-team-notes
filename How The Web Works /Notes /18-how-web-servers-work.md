
# How Web Servers Work  
**Date:** 1 January 2026

## Introduction

This section explains how web servers work internally once a request reaches them. While previous lessons focused on how a request travels from the browser to the server, this part focuses on what happens inside the server itself and how content is delivered back to the user.

Understanding this process is essential for web development and cybersecurity, as many vulnerabilities originate from how servers handle requests and generate responses.

## What Is a Web Server?

A web server is not necessarily a physical machine, but rather a software application that runs on a machine connected to the internet. Its main role is to listen for incoming connections, interpret requests using the HTTP protocol, and respond with the appropriate content.

Common web server software includes Apache, Nginx, IIS (used on Windows systems), and Node.js when used as a server-side runtime. These programs are responsible for deciding how requests are handled and what data is returned to the client.

## Root Directory

Every web server is configured with a root directory. This directory is the location on the server’s hard drive where website files are stored. When a client requests a resource, the web server looks for it inside this directory.

On Linux systems using Apache or Nginx, the default root directory is usually `/var/www/html`. On Windows systems using IIS, the default location is `C:\inetpub\wwwroot`.

When a client requests a file such as `/picture.jpg`, the web server retrieves the corresponding file from its root directory and sends it to the browser. At its core, the web is built on real files stored on a server’s filesystem.

## Virtual Hosts

A single web server can host multiple websites at the same time using a feature called virtual hosts. Virtual hosts allow the server to serve different websites based on the domain name requested by the client.

When an HTTP request arrives, it includes a host header specifying the domain name. The web server checks this value against its virtual host configuration files. If a match is found, the server serves the content associated with that domain. If no match is found, the default website is served instead.

Each virtual host can map to a different directory on the hard drive. For example, one domain may point to `/var/www/website_one`, while another points to `/var/www/website_two`. This allows many independent websites to run on a single server.

## Static vs Dynamic Content

Static content refers to files that do not change. These files are served exactly as they are stored on the server and are identical for every user. Examples include images, CSS files, JavaScript files, and static HTML pages.

Dynamic content, on the other hand, changes depending on the request, user input, or stored data. Examples include blog homepages that display the latest posts, search result pages, and personalized user dashboards.

For dynamic content, the server executes backend code to generate HTML dynamically before sending it to the client.

## Backend and Frontend

All processing that generates dynamic content happens on the backend. This includes application logic, database queries, and server-side programming. The backend is hidden from the user and cannot be viewed in the browser.

The frontend is everything the user sees in their browser. It consists of the final HTML, CSS, and JavaScript delivered by the server. The browser never sees the backend code, only the result of its execution.

## Backend Scripting and Programming Languages

Backend languages give websites their interactivity and intelligence. Common backend languages include PHP, Python, Ruby, Node.js, and Perl.

These languages can process user input, communicate with databases, call external services, and generate custom HTML responses for each request. When a backend script runs, it produces HTML that is sent to the browser, while the backend code itself remains hidden.

The increased interactivity enabled by backend processing also introduces additional security risks if input is not handled safely.

## Security Implications

Because backend logic is responsible for processing user input and generating responses, it is a common target for attacks. Improper input handling, insecure configurations, or poor isolation between virtual hosts can lead to serious vulnerabilities.

Understanding how web servers work is a critical foundation for learning about web application attacks such as injections, cross-site scripting, and file inclusion vulnerabilities.

## Conclusion

Web servers are the core of how websites function. They receive requests, locate files, execute backend logic when necessary, and deliver content to users. Concepts such as root directories, virtual hosts, static and dynamic content, and backend processing form the foundation of modern web applications.

A solid understanding of these mechanisms is essential for both building secure web applications and identifying potential security weaknesses.
