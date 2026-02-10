# Network and Service Exposure Analysis

This repository documents hands-on analysis of **network services, listening sockets, and real system exposure** on Linux hosts.

The focus is on distinguishing between configuration, catalog information, and actual runtime state.

---

## 🔍 Topics Covered

- Listening services and sockets
- IPv4 vs IPv6 exposure
- Localhost vs external interfaces
- Service-to-process mapping
- Network-based attack surface identification

---

## 📂 Contents

### 🔹 Listening Services Enumeration
Identify services exposed on all interfaces using runtime inspection tools.

### 🔹 Web Content Path Discovery
Extract and count unique paths from web content using CLI-based filtering.

---

## 🧠 Methodology

Analysis is based on:
- runtime validation
- socket-level inspection
- noise reduction and normalization
- defensible counting and correlation
