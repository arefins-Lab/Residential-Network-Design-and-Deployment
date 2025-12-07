# Residential Network Design & Deployment

## Project Overview
This project delivers a **centralised, multi‑floor residential network architecture** designed for reliability, seamless coverage, and future scalability.  
The solution balances **performance**, **cost‑efficiency**, and **long‑term flexibility**, built on a single ISP connection and aligned strictly with client requirements.

---

## Core Objectives
- Seamless Wi‑Fi coverage across all floors  
- Stable wired connectivity for desktops and printers  
- Traffic segmentation for family, office, and guest networks  
- Future‑ready design supporting VLANs, IoT isolation, and QoS  

---

## Project Constraints & Requirements
- **ISP:** Single 210 Mbps broadband connection  
- **Equipment:** Mid‑to‑high grade, cost‑efficient hardware  
- **Scope:** Only essential features; no unnecessary complexity  
- **Reliability:** Priority on stable, interference‑free coverage  

---

# Ground Floor Network Architecture

### Primary Internet Path
- ISP → **ASUS RT‑AX59U AX4200 Router**

### Core Switching Layer
- Router → **TP‑Link TL‑SG2210P JetStream 10‑Port Smart Switch**

### Static IP Assignments
- APs, desktops, and printers configured **outside the DHCP pool** to prevent conflicts.

### Connected Devices
- 2 × Windows 11 Desktop PCs (wired)  
- 1 × Canon LBP6030B Laser Printer (wired)  
- 1 × Ruijie RG‑RAP2200(E) AP (ceiling‑mounted for library/guest Wi‑Fi)  
- Living Room Wi‑Fi served directly by the ASUS router  

---

# First Floor Network Architecture

### Main Uplink
- Wired uplink from the Ground Floor managed switch.

### Wireless Coverage
- 1 × Ruijie RG‑RAP2200(E) AP (ceiling‑mounted)  
- Provides seamless coverage across the living area + 4 rooms  

---

# Key Equipment
- **Router:** ASUS RT‑AX59U AX4200  
- **Switch:** TP‑Link TL‑SG2210P JetStream  
- **Access Points:** Ruijie RG‑RAP2200(E) (Wi‑Fi 5, 1267 Mbps)  
- **Cabling:** AC‑NET CAT‑6 Full Copper  
- **Desktops:** Windows 11 PCs  
- **Printer:** Canon LBP6030B  

---

# Security & Best Practices
- Static IPs for APs, PCs, printers  
- Router IPS/IDS enabled  
- Guest Wi‑Fi isolation via dedicated AP  
- VLAN‑ready architecture using a managed switch  

---

# Future Enhancements (Planned Architecture Upgrades)
- Full VLAN segmentation: Guest / IoT / Family / Office  
- QoS policies: Prioritize conferencing & work traffic  
- IoT network: Dedicated isolated segment  
- Remote management: Secure off‑site access  
- Central syslog for APs, router, and switch  
- Zabbix/PRTG monitoring for real‑time visibility  
- UPS integration for power protection  
- Mesh expansion if coverage demands increase  

These additions show that the network is **not just deployed**, but **architected for growth**.

---

# Result
A **centralised, reliable, and scalable residential network** delivering:

- Full‑floor Wi‑Fi coverage  
- Stable wired connectivity  
- Segmentation‑ready architecture  
- Security‑focused design  
- Future‑proof upgrade path  




