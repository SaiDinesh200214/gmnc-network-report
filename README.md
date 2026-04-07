# 🌐 Enterprise Network Infrastructure Design
### Global Multi-National Company (GMNC) — Network Design Report

<div align="center">

![Network](https://img.shields.io/badge/Network-Enterprise%20Grade-00BCD4?style=for-the-badge&logo=cisco&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-Report-1565C0?style=for-the-badge&logo=latex&logoColor=white)
![Cisco](https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-2E7D32?style=for-the-badge)

**Designed & Documented by [Saidinesh Andekar](https://linkedin.com/in/saidineshandekar)**  
*Networking & Cybersecurity Enthusiast · April 6, 2026*

</div>

---

## 📋 Project Overview

This repository contains the full **Enterprise-Level Network Design Report** for a simulated Global Multi-National Company (GMNC), built and tested in **Cisco Packet Tracer**. The network spans three geographically distributed zones and implements industry-standard protocols mirroring real-world deployments at companies like Amazon AWS, Infosys, and HDFC Bank.

The report is written in **LaTeX** (Overleaf-compatible) with a professional dark-themed cover, embedded topology diagrams, real-world analogies for every protocol, and colour-coded Cisco IOS configuration blocks.

---

## 🗂️ Repository Structure

```
gmnc-network-report/
│
├── network_report.tex       ← Full LaTeX source (Overleaf-ready)
├── network_report.pdf       ← Compiled PDF report (17 pages)
├── topo1.jpg                ← Topology diagram — schematic view
├── topo2.jpg                ← Topology diagram — colour-coded zone view
└── README.md                ← This file
```

---

## 🏗️ Network Architecture

The GMNC network is divided into **3 functional zones**:

| Zone | Colour | Devices | Function |
|------|--------|---------|----------|
| **Access Zone** | 🟢 Green | PCs, Laptops, DHCP Server, L2 Switches | End-user connectivity |
| **Core Operations Zone** | 🔵 Blue | Core Routers, OSPF backbone | High-speed packet forwarding |
| **Distribution Zone** | 🟣 Pink | Distribution Routers, NAT, ACL | Policy control & internet access |

### Topology — Schematic View
![Topology Schematic](topo1.jpg)

### Topology — Colour-Coded Zone Overview
![Zone Overview](topo2.jpg)

---

## ⚙️ Technologies Implemented

| Protocol / Feature | Purpose | Real-World Analogy |
|---|---|---|
| **RIP v2** | Dynamic routing across 30 subnets | Word-of-mouth navigation in a city |
| **DHCP** | Auto IP assignment (254+ devices/pool) | Hotel reception assigning rooms |
| **NAT** | Private to public IP translation | Corporate PO Box address |
| **ACL** | Traffic filtering & server protection | Airport security checkpoint |
| **IPSec VPN** | Encrypted site-to-site tunnel (R1 to R8) | Armoured cash transit van |
| **OSPF** | Core zone routing backbone | Highway GPS system |

---

## 📊 IP Addressing Scheme

```
192.168.1.0/24   →  Access Zone – Area 1  (End-user devices)
192.168.3.0/24   →  Access Zone – Area 1  (Server VLAN)
192.168.5.0/24   →  Access Zone – Area 1  (Wireless segment)
192.168.9.0/24   →  Access Zone – Area 3  (DHCP auto-assigned)
192.168.21.0/24  →  Core Operations Zone  (Backbone links)
192.168.25.0/24  →  Distribution Zone     (Inter-router WAN)
192.168.26.0/24  →  Distribution Zone     (Internet-facing)
```

---

## ✅ Test Results

| Feature | Test Method | Result |
|---|---|---|
| RIP Routing | `show ip route rip` — 30 networks learned | ✅ PASS |
| DHCP Auto-Assign | PC12 received `192.168.9.2` automatically | ✅ PASS |
| NAT Translation | `show ip nat translations` populated | ✅ PASS |
| ACL Enforcement | Server blocked cross-area; PCs permitted | ✅ PASS |
| VPN Tunnel | Traceroute: 2 hops to `192.168.100.2` | ✅ PASS |
| End-to-End Ping | All zones reachable | ✅ PASS |

---

## 🛡️ Security Model

The network follows a **Defense-in-Depth** approach aligned with **NIST CSF** and **ISO 27001**:

```
┌─────────────────────────────────────────────┐
│       PERIMETER — NAT + ACL                 │
│  ┌───────────────────────────────────────┐  │
│  │     NETWORK — Routing Zones + VPN     │  │
│  │  ┌─────────────────────────────────┐  │  │
│  │  │  TRANSPORT — Subnetting + DHCP  │  │  │
│  │  │  ┌───────────────────────────┐  │  │  │
│  │  │  │   HOST — ACL per Server   │  │  │  │
│  │  │  │  ┌─────────────────────┐  │  │  │  │
│  │  │  │  │  DATA — IPSec VPN   │  │  │  │  │
│  │  │  │  └─────────────────────┘  │  │  │  │
│  │  │  └───────────────────────────┘  │  │  │
│  │  └─────────────────────────────────┘  │  │
│  └───────────────────────────────────────┘  │
└─────────────────────────────────────────────┘
```

---

## 📄 How to Use the LaTeX Report

### Option 1 — Overleaf (Recommended)
1. Go to [overleaf.com](https://overleaf.com) → **New Project** → **Upload Project**
2. Upload `network_report.tex`, `topo1.jpg`, and `topo2.jpg` into the same project
3. Click **Recompile** — compile **twice** for the Table of Contents to populate

### Option 2 — Local LaTeX
```bash
# Install dependencies (Ubuntu/Debian)
sudo apt install texlive-full

# Compile (run twice for TOC)
pdflatex network_report.tex
pdflatex network_report.tex
```

---

## 🔧 Tools Used

- **Cisco Packet Tracer** — Network simulation & testing
- **LaTeX / Overleaf** — Report authoring
- **TikZ** — Cover page graphics & defense-in-depth diagram
- **tcolorbox** — Styled info boxes & code frames

---

## 👤 About the Author

**Saidinesh Andekar** — Networking & Cybersecurity Enthusiast

- 🌐 Portfolio: [saidinesh-portfolioweb.netlify.app](https://saidinesh-portfolioweb.netlify.app)
- 💼 LinkedIn: [linkedin.com/in/saidineshandekar](https://linkedin.com/in/saidineshandekar)
- 🐙 GitHub: [github.com/SaiDinesh200214](https://github.com/SaiDinesh200214)

**Certifications:** Practical Ethical Hacking · Linux Fundamentals · Intro to Pentesting · AWS (×3) · UX Design · PowerShell · Vulnerability Management

---

<div align="center">

*Built with ❤️ and Cisco IOS — April 2026*

</div>
