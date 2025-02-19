# 🖧 Networking Commands Cheat Sheet

This cheat sheet provides a **quick reference** for essential networking commands, helping you troubleshoot, analyze, and manage networks efficiently.

## 📌 1. `ping` – Check Network Connectivity
**Purpose:** Tests the reachability of a host on a network.  
**Usage:**  
```sh
ping google.com
```
**Use Case:** Checking if a server or website is reachable.

---

## 📌 2. `traceroute` / `tracert` – Trace Packet Routes
**Purpose:** Displays the path packets take to reach a destination.  
**Usage:**  
```sh
traceroute google.com  # Linux/macOS  
tracert google.com     # Windows  
```
**Use Case:** Diagnosing slow network connections by identifying bottlenecks.

---

## 📌 3. `netstat` – Network Statistics
**Purpose:** Displays active connections and listening ports.  
**Usage:**  
```sh
netstat -tulnp  # Linux/macOS  
netstat -ano    # Windows  
```
**Use Case:** Checking which processes are using network ports.

---

## 📌 4. `curl` – Make HTTP Requests
**Purpose:** Fetches data from URLs (useful for APIs & debugging).  
**Usage:**  
```sh
curl -I https://example.com
```
**Use Case:** Checking website availability and response headers.

---

## 📌 5. `dig` / `nslookup` – DNS Lookup
**Purpose:** Queries DNS records for a domain.  
**Usage:**  
```sh
dig google.com  # Linux/macOS  
nslookup google.com  # Windows  
```
**Use Case:** Troubleshooting domain name resolution issues.

---
