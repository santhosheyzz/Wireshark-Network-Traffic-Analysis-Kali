# 🔍 Wireshark Packet Capture and Analysis - Kali Linux

## 📌 Project Summary

**Date**: June 3, 2025  
**Tool**: Wireshark  
**System**: Kali Linux  
**Interface Used**: wlan0 (Wi-Fi)  

**Objective**:  
To capture live network traffic, analyze common protocols, and understand how data flows across a network. The captured `.pcap` file is analyzed using protocol filters, and findings are documented here.
---
![img alt](https://github.com/santhosheyzz/Wireshark-Network-Traffic-Analysis-Kali/blob/8ae6139e48cb62e9e1c125ac0751b9fcad10c878/Images/Task.png)
---

## 🧪 Traffic Generated

- Opened websites: `example.com`, `bing.com`
- Ran terminal commands:
  ```bash
  ping google.com
  curl http://example.com
  ```

---

---

## 🌐 Protocols Identified (Full Forms + Functions)

| Protocol | Full Form                         | Port      | Function |
|----------|-----------------------------------|-----------|----------|
| **DNS**  | Domain Name System                | 53        | Translates domain names (like google.com) to IP addresses |
| **HTTP** | HyperText Transfer Protocol       | 80        | Requests and transfers unencrypted web content |
| **HTTPS**| HyperText Transfer Protocol Secure| 443       | Transfers encrypted web content |
| **ICMP** | Internet Control Message Protocol | -         | Used for diagnostics like ping (no port) |
| **TCP**  | Transmission Control Protocol     | -         | Reliable connection-oriented communication |
| **UDP**  | User Datagram Protocol            | -         | Fast, connectionless communication |
| **TLS**  | Transport Layer Security          | 443       | Encryption protocol used in HTTPS |
| **OCSP** | Online Certificate Status Protocol| -         | Verifies SSL certificate revocation status |
| **ARP**  | Address Resolution Protocol       | -         | Resolves IP addresses to MAC addresses in local networks |
| **DHCP** | Dynamic Host Configuration Protocol| 67/68    | Assigns IP addresses to devices automatically |
| **BSSID**| Basic Service Set Identifier      | -         | MAC address of the access point in Wi-Fi |
| **SSL**  | Secure Sockets Layer (Legacy)     | 443       | Obsolete version of TLS used for encryption |
| **FTP**  | File Transfer Protocol            | 21        | Transfers files between client and server |
| **SMTP** | Simple Mail Transfer Protocol     | 25        | Sends emails |
| **POP3** | Post Office Protocol v3           | 110       | Retrieves emails from the server |
| **IMAP** | Internet Message Access Protocol  | 143       | Access emails on the server in real-time |

---

## 📂 File(s) Included

- `network-capture.pcap` – Raw packet capture file  
- `README.md` – Documentation and analysis

---

## 🔍 Cheat Sheet: Common Wireshark Filters

| Filter | Purpose |
|--------|---------|
| `http` | Show only HTTP traffic |
| `dns`  | Show DNS queries/responses |
| `icmp` | Show ping traffic |
| `tcp`  | Show only TCP packets |
| `udp`  | Show only UDP packets |
| `tls`  | Show encrypted HTTPS packets |
| `ip.addr == 192.168.1.1` | Filter packets to/from specific IP |
| `tcp.port == 80` | Show traffic on HTTP port |
| `frame contains "google"` | Find packets containing specific keyword |

---

## 📈 Observations

### 1. **DNS**
- Domain requests sent to `8.8.8.8` (Google DNS)
- Type: Standard query and response

### 2. **HTTP**
- GET request to example.com
- Headers and content viewable (not encrypted)

### 3. **ICMP**
- Echo requests and replies observed during ping

### 4. **TLS**
- TLS handshakes captured when visiting HTTPS websites

---

## 🎯 Key Skills Practiced

- Live packet capture in Kali Linux  
- Interface monitoring  
- Using display filters in Wireshark  
- Protocol recognition and packet dissection  
- Creating a professional report  

---

## 🎤 Interview Questions & Answers

### 1. **What is Wireshark used for?**
Wireshark is a network protocol analyzer used to capture, inspect, and analyze packets in real-time on a network.

### 2. **What is a packet?**
A packet is a unit of data sent across a network that includes headers and payload (content/data).

### 3. **How to filter packets in Wireshark?**
Use the filter bar with syntax like `http`, `ip.addr == 192.168.1.1`, or `tcp.port == 443` to view specific traffic.

### 4. **What is the difference between TCP and UDP?**
- **TCP**: Reliable, connection-based, slower (used for HTTP, HTTPS)  
- **UDP**: Fast, connectionless, unreliable (used for DNS, video streaming)

### 5. **What is a DNS query packet?**
A DNS query packet is a request sent from a client to a DNS server to resolve a domain name into an IP address.

### 6. **How can packet capture help in troubleshooting?**
Packet capture allows admins to detect errors, performance issues, or malicious activity by inspecting traffic flow and packet contents.

### 7. **What is a protocol?**
A protocol is a set of rules that define how data is transmitted and received over a network (e.g., HTTP, DNS, TCP).

### 8. **Can Wireshark decrypt encrypted traffic?**
Wireshark **cannot decrypt** TLS/HTTPS traffic unless:
- You have the **server’s private key**, or  
- **SSL key logging** is enabled in the browser (for client-side decryption)

---

## ✅ Conclusion

This hands-on session provided practical experience in capturing and analyzing network packets using Wireshark in Kali Linux. Key protocols like DNS, HTTP, ICMP, and TLS were identified, and tools like filters and packet dissection helped deepen protocol-level understanding. This is a foundational skill for networking, cybersecurity, and digital forensics roles.

---
