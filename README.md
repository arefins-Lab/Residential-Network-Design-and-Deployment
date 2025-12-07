Residential Network Design & Deployment —

Project Overview:
This project delivers a centralised, multi‑floor residential network architecture designed for reliability, seamless coverage, and future scalability. The solution balances performance, cost‑efficiency, and long‑term flexibility, built on a single ISP connection and aligned strictly with client requirements.

Core Objectives:
Seamless Wi‑Fi coverage across all floors
Stable wired connectivity for desktops and printers
Traffic segmentation for family, office, and guest networks
Future‑ready design supporting VLANs, IoT isolation, and QoS

Project Constraints & Requirements:
ISP: Single 210 Mbps broadband connection
Equipment: Mid‑to‑high grade, cost‑efficient hardware
Scope: Only essential features; no unnecessary complexity
Reliability: Priority on stable, interference‑free coverage

Ground Floor Network Architecture:
Primary Internet Path -
ISP → ASUS RT‑AX59U AX4200 Router

Core Switching Layer -
Router → TP‑Link TL‑SG2210P JetStream 10‑Port Smart Switch

Static IP Assignments -
APs, desktops, and printers are configured outside the DHCP pool to prevent conflicts.

Connected Devices:
2 × Windows 11 Desktop PCs (wired)
1 × Canon LBP6030B Laser Printer (wired)
1 × Ruijie RG‑RAP2200(E) AP (ceiling‑mounted for library/guest Wi‑Fi)
Living Room Wi‑Fi: Served directly by the ASUS router

First Floor Network Architecture:
Main Uplink -
Wired uplink from the Ground Floor managed switch.

Wireless Coverage -
1 × Ruijie RG‑RAP2200(E) AP (ceiling‑mounted)
Provides seamless coverage across the living area + 4 rooms

Key Equipment:
Router: ASUS RT‑AX59U AX4200
Switch: TP‑Link TL‑SG2210P JetStream
Access Points: Ruijie RG‑RAP2200(E) (Wi‑Fi 5, 1267 Mbps)
Cabling: AC‑NET CAT‑6 Full Copper
Desktops: Windows 11 PCs
Printer: Canon LBP6030B

Security & Best Practices:
Static IPs for APs, PCs, and printers
Router IPS/IDS enabled
Guest Wi‑Fi isolation via dedicated AP
VLAN‑ready architecture using a managed switch

Future Enhancements (Planned Architecture Upgrades):
Full VLAN segmentation: Guest / IoT / Family / Office
QoS policies: Prioritise conferencing & work traffic
IoT network: Dedicated isolated segment
Remote management: Secure off‑site access
Central syslog: Logging for APs, router, and switch
Zabbix/PRTG monitoring: Real‑time health visibility
UPS integration: Power protection for core devices
Mesh expansion: If future coverage demands increase

Result:
A centralised, reliable, and scalable residential network delivering:
Full‑floor Wi‑Fi coverage
Stable wired connectivity
Segmentation‑ready architecture
Security‑focused design
Future‑proof upgrade path

Cisco IOS Command Library (For Lab Simulation):
! Enter privileged EXEC mode
enable
! Enter global configuration mode
configure terminal
! Set hostname
hostname HomeRouter
! Configure interface IP
interface GigabitEthernet0/0
ip address 192.168.1.1 255.255.255.0
no shutdown

! Configure default gateway (for switch)
ip default-gateway 192.168.1.1
! Configure DHCP pool
ip dhcp pool RESIDENTIAL
network 192.168.1.0 255.255.255.0
default-router 192.168.1.1
dns-server 192.168.1.220 192.168.1.215
domain-name home. local

! Exclude static IP range
ip dhcp excluded-address 192.168.1.190 192.168.1.200

! Verification commands
show ip dhcp binding
show running-config

! Save configuration
write memory



