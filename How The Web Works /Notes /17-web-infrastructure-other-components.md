
# Other Components – Web Infrastructure Overview  
**Date:** 1 January 2026

## Introduction

In addition to the core components that allow a website to function (DNS, HTTP, web servers, and browsers), modern web applications rely on several additional components to improve performance, scalability, reliability, and security.

These components are essential for large-scale or high-traffic websites and play a critical role in modern web infrastructure.

## Load Balancers

When a website begins to receive a large amount of traffic, a single web server may no longer be sufficient to handle all incoming requests. Load balancers solve this problem by distributing incoming traffic across multiple web servers.

The load balancer receives the request first and then forwards it to one of several backend servers. This process is invisible to the user and ensures the website remains responsive.

Load balancers provide two main benefits: handling high traffic volumes and ensuring availability. If one server becomes unresponsive, the load balancer stops sending traffic to it and redirects requests to other healthy servers.

To decide which server should handle a request, load balancers use algorithms such as round-robin, which distributes requests evenly, or weighted and least-busy methods, which send traffic to the server under the lowest load.

Load balancers also perform regular health checks on servers. If a server fails these checks, it is temporarily removed from service until it responds correctly again.

## Content Delivery Networks (CDN)

A Content Delivery Network, or CDN, is designed to reduce load on the main web server and improve website performance. CDNs host static resources such as JavaScript files, CSS files, images, videos, and other static assets across many servers distributed worldwide.

When a user requests one of these resources, the CDN determines the user’s geographic location and serves the content from the nearest available server. This significantly reduces latency and improves loading speed.

By offloading static content to a CDN, the main web server can focus on dynamic content and application logic, resulting in better overall performance and scalability.

https://youtu.be/chyZRNT7eEo?list=PLJ7Xch9LHhFv6qBHlKEzdwuQo417SYQVO

## Databases

Most websites need a way to store and retrieve user data. Web servers communicate with databases to save and access information such as user accounts, messages, settings, and application data.

Databases can range from very simple storage solutions to complex clusters of multiple servers designed for speed, redundancy, and fault tolerance.

Common database technologies include MySQL, Microsoft SQL Server, PostgreSQL, and MongoDB. Each database system has its own strengths and use cases, but they all serve the same fundamental purpose: managing data.

From a security perspective, databases are high-value targets. Improper handling of user input or insecure queries can lead to serious vulnerabilities and data breaches.

## Web Application Firewall (WAF)

A Web Application Firewall, or WAF, acts as a protective barrier between users and the web server. All incoming web requests pass through the WAF before reaching the server.

The primary purpose of a WAF is to protect the application from common attacks such as denial-of-service attempts, automated bot traffic, and known exploitation techniques. It analyzes requests, checks whether they appear to originate from legitimate users, and enforces security rules.

WAFs also implement rate limiting, which restricts the number of requests an IP address can send within a given time frame. Requests that are identified as malicious or excessive are dropped before they ever reach the web server.

While a WAF does not replace secure coding practices, it provides an important additional layer of defense.

https://www.youtube.com/watch?v=kDEX1HXybrU&t=4s

## Putting It All Together

In a modern web architecture, a user’s request may pass through multiple layers: a CDN, a WAF, a load balancer, one of several web servers, and finally a database. Each component plays a specific role in ensuring performance, reliability, and security.

Understanding how these components interact is essential for both web development and cybersecurity.

## Conclusion

Modern web applications rely on more than just a single server. Load balancers, CDNs, databases, and web application firewalls work together to create systems that are fast, scalable, and resilient against attacks.

A clear understanding of these components provides a strong foundation for learning web security and defending complex web infrastructures.
