# dns-lab-secure
A hands-on project to build a secure DNS server in a virtual lab. Explore DNS fundamentals, simulate real-world attacks like spoofing and cache poisoning, and apply security hardening techniques. Learn TCP/IP, OSI layer communication, and gain practical cybersecurity skills.


# Secure DNS Lab 🔐🌐

## Overview

The **Domain Name System (DNS)** is a foundational component of the internet — translating human-readable domain names (like `google.com`) into machine-understandable IP addresses (like `93.184.216.34`). However, DNS is also a major attack surface in cybersecurity.

This project explores:
- Building a **small-scale DNS server** inside a virtual environment.
- Analyzing and simulating **DNS-based attacks**.
- **Hardening** the DNS server against such attacks.
- Along with the project, we will also be Learning the **TCP/IP model**, **OSI layers**, and **communication between hosts** in real-world networking environments.

---

## 🧠 Objectives

- Build a functioning DNS server in a virtual lab setup.
- Research and simulate known DNS attacks (e.g., spoofing, cache poisoning, amplification).
- Explore and implement security best practices and hardening techniques.
- Visualize and explain communication across **TCP/IP and OSI models**.
---

## 🔧 Technologies & Tools

| Category         | Tools / Technologies          |
|------------------|-------------------------------|
| Virtualization   | VirtualBox / VMware    |
| DNS Server       | CoreDNS    |
| OS               | Kali Linux   |
| Packet Analysis  | Wireshark / tcpdump           |
| Attack Simulation| Scapy / Ettercap / custom scripts |
| Firewall / Hardening | iptables, ufw, fail2ban   |
| Programming      | Python, Bash                  |



## 📦 Project Structure

```bash
dns-lab-secure/
│
├── virtual-lab/              # VMs setup, networking topology, NAT/Bridged configs
│   ├── attacker-vm/
│   ├── dns-server-vm/
│   └── client-vm/
│
├── dns-server/               # Custom DNS setup (BIND9 or dnsmasq config files)
│   └── zone-files/
│
├── attacks/                  # Simulated DNS attacks (spoofing, poisoning, etc.)
│   └── spoofing/
│   └── amplification/
│
├── hardening/                # Firewall rules, DNSSEC, logging configs
│   └── best-practices.md
│
├── tcp-ip-communication/     # Educational diagrams, layer-by-layer analysis
│   └── layer-analysis.md
│
├── scripts/                  # Automation scripts, monitoring, logs
│   └── dns-monitor.py
│
├── docs/                     # Research reports, reading materials, papers
│   └── dns-security-survey.pdf
│
└── README.md                 # Project intro
```


# 🧪 DNS Lab Topology

## Network Topology
- **[Client VM]** ---> **[DNS Server VM]** ---> **[Internet (optional)]**
- **[Attacker VM]** ---> (same network)

All VMs are placed in an **isolated virtual network**, allowing:
- DNS requests from Client to Server
- Attacker to intercept/modify packets
- Secure testing with no impact on real network

## 📚 Learning Modules(Good to Know)
| Module | Description |
|--------|-------------|
| 1. Basics of DNS | A records, MX, CNAME, zone files |
| 2. TCP/IP & OSI Layers | Layer-by-layer packet flow |
| 3. DNS Server Setup | Using BIND9 or dnsmasq |
| 4. DNS Query Simulation | Using dig, nslookup |
| 5. Attack Simulation | DNS spoofing, amplification |
| 6. DNS Security Mechanisms | DNSSEC, rate limiting |
| 7. Hardening the DNS Server | Firewalls, chroot, logging |
| 8. Monitoring & Logs | Real-time DNS traffic monitoring |
| 9. Final Project Report | Summarize research + implementation |



## 🛡️ Attacks You’ll Simulate
| Attack Type | Description |
|-------------|-------------|
| DNS Spoofing | Trick user into visiting a fake site |
| Cache Poisoning | Inject malicious IPs into DNS cache |
| Amplification Attacks | DDoS via recursive queries |
| NXDOMAIN Attack | Flood server with non-existent domains |
| DNS Tunneling (Advanced) | Data exfiltration through DNS queries |

## 🔐 Security Hardening
- DNSSEC implementation
- Recursion restriction
- Source IP rate limiting
- Logging & monitoring
- Firewall rules (iptables/ufw)
- Restrict zone transfers
- Chrooted DNS service

## 🎯 Target Audience
- Students and learners interested in networking, cybersecurity, and systems engineering
- Professionals looking to understand DNS attacks & mitigations
- Educators seeking a hands-on DNS security lab

## 🧩 Prerequisites
- Familiarity with TCP/IP & OSI models
- Basic Linux commands & configuration
- Comfort with virtualization software (VirtualBox, VMware, QEMU, etc.)
- Curiosity and drive to dig deep into how systems communicate

## 📈 Roadmap
1. Setup VM lab environment
2. Configure DNS server (basic)
3. Create and test custom DNS zones
4. Simulate DNS attacks
5. Analyze packet flow (tcpdump/Wireshark)
6. Implement DNSSEC and hardening steps
7. Document everything with diagrams and demos

## 📌 Contribution & License
This is an open project for learning and experimentation. Pull requests are welcome if you wish to contribute examples or better hardening strategies.

## 📣 Final Note
DNS is everywhere — and it’s silently powerful. This project helps you see the invisible, understand the fundamentals, and protect this core layer of the Internet. 🛡️🌍

