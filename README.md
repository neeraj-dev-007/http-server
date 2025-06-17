# http-server

An HTTP server written in Go, built from scratch to understand the internals of how the web works.

---

## 🧠 Learnings So Far

### 1. The Internet vs The Web

The **Internet** is the global network infrastructure that connects computers worldwide.

The **Web** (World Wide Web) is a service built on top of the Internet. It consists of:
- **URLs** (Uniform Resource Locators) — identifiers for web resources
- **HTTP** (HyperText Transfer Protocol) — the protocol for communication
- **HTML** (HyperText Markup Language) — the format for displaying web content

---

### 2. IP Addresses and Domain Names

Every device connected to the Internet has an **IP address** (like `192.168.1.10`) to uniquely identify it.

Since IP addresses are hard to remember, we use **domain names** (like `google.com`). DNS (Domain Name System) maps these domain names to IP addresses.

---

### 3. Transport Layer Protocols

**TCP (Transmission Control Protocol)** and **UDP (User Datagram Protocol)** are the two most commonly used transport layer protocols.

- **TCP** is connection-oriented, reliable, and used for most web traffic.
- **UDP** is connectionless, faster, and used in real-time applications like video calls or games.

---

### 4. Ports

**Ports** are logical endpoints used to differentiate services running on the same machine.

- Each IP + protocol (TCP/UDP) combination can use up to **65,535 ports** (16-bit unsigned integers).
- Ports **0–1023** are well-known ports (e.g., 80 for HTTP, 443 for HTTPS).
- **User applications** usually use ports **1024–49151**, while **49152–65535** are ephemeral (temporary) ports.
- Port management is handled by the OS kernel’s networking stack.

---

### 5. Web Server Basics

A **web server** (e.g., NGINX or Apache) handles requests for websites and serves responses (e.g., HTML pages, images).

A complete modern web stack often includes:
- An **HTTP server**: Listens for and responds to client requests (e.g., NGINX, custom Go server).
- An **Application server**: Contains business logic, usually written by developers.
- A **Database**: Stores and retrieves structured data.
- **Load balancers**: Distribute traffic across multiple servers for performance and reliability (e.g., NGINX, HAProxy).

Together, these components serve **dynamic** and **static** web content to users.
