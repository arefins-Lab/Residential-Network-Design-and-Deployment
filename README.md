Residential Network Design and Deployment:

📌 Project Overview:
This project involved designing and implementing a centralised residential network for a multi‑story property. The objectives were:

Seamless Wi‑Fi coverage across all floors

Stable wired connectivity for desktops and printers

Traffic segmentation for family, office, and guest usage

Future‑ready scalability with VLANs, IoT isolation, and QoS

The deployment was based on a single ISP connection and aligned strictly with the client’s requirements — balancing performance, reliability, and cost‑effectiveness.

⚙️ Project Constraints & Requirements:
ISP: Single 210 Mbps broadband connection

Equipment Quality: Moderate‑to‑high grade, reliable but cost‑effective

Scope: Limited to the client’s stated needs (no unnecessary advanced features)

Reliability: Priority on stable, interference‑free coverage

🖥️ Ground Floor Network Architecture:
Primary Internet Connection: ISP → ASUS RT‑AX59U AX4200 Dual Band WiFi Router

Core Switching Layer: Router → TP‑Link TL‑SG2210P JetStream 10‑Port Gigabit Smart Switch

Static IP Assignments: PCs, APs, and printers configured outside the DHCP range → prevents conflicts

Devices & Connections:

2 × Desktop PCs (Windows 11) – Wired

1 × Canon imageCLASS LBP6030B Mono Laser Printer – Wired

1 × Ruijie RG‑RAP2200(E) Access Point – Ceiling‑mounted, dedicated for library/guest Wi‑Fi

Living Room Wi‑Fi: Provided directly by the ASUS Router for family/general use

🏢 First Floor Network Architecture:
Main Uplink: Wired uplink from the Ground Floor managed switch

Wireless Coverage: 1 × Ruijie RG‑RAP2200(E) Access Point (centrally ceiling‑mounted) → seamless coverage across living area + 4 rooms

🔑 Key Equipment:
Router: ASUS RT‑AX59U AX4200 Dual Band WiFi Router

Switch: TP‑Link TL‑SG2210P JetStream 10‑Port Gigabit Smart Switch

Access Points: Ruijie RG‑RAP2200(E) (Wi‑Fi 5, 1267 Mbps, Dual Band, Ceiling Mount)

Cabling: AC‑NET CAT‑6 Full Copper LAN Cable

Desktops: Windows 11 PCs

Printer: Canon imageCLASS LBP6030B Mono Laser Printer

🔒 Security & Best Practices:
Static IPs: For APs, PCs, and printers (outside the  DHCP pool)

Router Security Suite: IPS/IDS enabled

Guest Isolation: Guest Wi‑Fi via dedicated AP

Future VLAN Capability: Supported via managed switch

🚀 Future Enhancements:
VLANs: Full segmentation (Guest, IoT, Family, Office)

QoS Rules: Prioritise video conferencing/work traffic

IoT Integration: Dedicated segment for smart devices

Remote Management: Secure off‑site troubleshooting

✅ Result
A centralised, reliable, and future‑ready residential network delivering:

Full Wi‑Fi coverage

Stable wired connectivity

Scalable security and segmentation

📜 Command Library (Cisco IOS):
bash
! Enter privileged EXEC mode
enable

! Enter global configuration mode
configure terminal

! Set hostname
hostname HomeRouter

! Configure the interface with an IP address
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

! Exclude addresses from the DHCP pool
ip dhcp excluded-address 192.168.1.190 192.168.1.200

! Verify DHCP bindings
show ip dhcp binding

! Verify running configuration
show running-config

! Save configuration
write memory

