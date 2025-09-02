# Residential-Network-Design-and-DeploymentProject Overview

This project involved designing and implementing a centralised residential network for a multi-story property. The objective was to provide:

Seamless Wi-Fi coverage across all floors.

Stable wired connectivity for desktops and printers.

Traffic segmentation for different usage scenarios (family, office, and guests).

Future-ready scalability with options for VLANs, IoT isolation, and QoS.

The deployment was based on a single ISP connection and aligned strictly with the client’s requirements—balancing performance, reliability, and cost-effectiveness.

Project Constraints & Requirements:

ISP: Single 210 Mbps broadband connection.

Equipment Quality: Moderate-to-high grade, reliable but not excessively costly.

Scope: Limited to the client’s stated needs. No unnecessary advanced features.

Reliability: Priority on stable, interference-free coverage.

Ground Floor Network Architecture:

The ground floor functions as the core distribution hub.

Primary Internet Connection:

ISP → ASUS RT-AX59U AX4200 Dual Band WiFi Router

Core Switching Layer:

Router → TP-Link TL-SG2210P JetStream 10-Port Gigabit Smart Switch

All wired and wireless connections originate from this managed switch.

Static IP Assignments:

Desktop PCs, Access Points, and Printer configured with static IPs outside DHCP range.

Prevents IP conflicts and ensures reliability.

Devices & Connections:

2 × Desktop PCs (Windows 11) – Wired

1 × Canon imageCLASS LBP6030B Mono Laser Printer – Wired

1 × Ruijie RG-RAP2200(E) Access Point – Ceiling-mounted, dedicated for library/guest Wi-Fi

Living Room Wi-Fi:

Provided directly by the ASUS Router for family & general use.

First Floor Network Architecture:

The first floor extends coverage from the ground floor’s central switch.

Main Uplink:

Wired uplink from Managed Switch (Ground Floor) to the first floor.

Wireless Coverage:

1 × Ruijie RG-RAP2200(E) Access Point centrally ceiling-mounted.

Provides seamless Wi-Fi across the entire floor (living area + 4 rooms).

Key Equipment:

Router: ASUS RT-AX59U AX4200 Dual Band WiFi Router

Switch: TP-Link TL-SG2210P JetStream 10-Port Gigabit Smart Switch

Access Points: Ruijie RG-RAP2200(E) (Wi-Fi 5, 1267 Mbps, Dual Band, Ceiling Mount)

Cabling: AC-NET CAT-6 Full Copper LAN Cable

Desktops: Windows 11 PCs

Printer: Canon imageCLASS LBP6030B Mono Laser Printer

Security & Best Practices:

Static IPs: For APs, PCs, and printer (outside DHCP pool).

Router Security Suite: IPS/IDS enabled.

Guest Isolation: Guest Wi-Fi via dedicated AP.

Future VLAN Capability: Supported via managed switch.

Future Enhancements:

The design is flexible and can scale with client needs:

VLANs: Full network segmentation (Guest, IoT, Family, Office).

QoS Rules: Prioritize video conferencing or work-related traffic.

IoT Integration: Dedicated segment for smart devices.

Remote Management: Secure access for off-site troubleshooting.

Result:
A centralized, reliable, and future-ready residential network with full coverage, wired stability, and scalable security.
