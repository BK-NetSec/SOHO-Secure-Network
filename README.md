Secure SOHO Network Implementation
Author: BK-NetSec
Field: Information Technology / Network Engineering

Project Overview
This project demonstrates the design and deployment of a secured Small Office/Home Office (SOHO) network using Cisco Packet Tracer. The infrastructure utilizes a Layer 2 Switch to manage wired distribution, ensuring efficient data frame delivery and collision domain separation.

Key Technical Features

Layer 2 Switching: Used a Cisco 2960 switch to provide dedicated bandwidth to wired endpoints.

WPA2-AES Encryption: Secured wireless communication for mobile devices.

Administrative Hardening: Changed default router credentials and disabled unauthorized remote management.

DHCP Address Reservation: Guaranteed IP stability for critical resources like the Network Printer.

Firewall and Policy Enforcement: Implemented SPI Firewall and URL filtering to mitigate external threats.

ICMP Verification: Validated end-to-end connectivity across wired and wireless segments.

Hardware Components and Roles

Wireless Router (Gateway)
The brain of the network. It handles DHCP address assignment, provides the WPA2-secured Wi-Fi signal, and acts as the first line of defense with its built-in firewall.

Cisco Catalyst Switch (Distribution Layer)
The central hub for wired devices. It ensures high-speed, dedicated bandwidth for the Desktop PC and Printer, managing data frames efficiently to prevent network congestion.

Desktop PC (Wired Endpoint)
Connected via Copper Straight-Through cable to the switch. It represents a high-performance workstation that requires a stable, low-latency connection for office tasks.

Smartphone (Wireless Endpoint)
Connected to the Bole_Office SSID. It is used to verify the wireless security (WPA2-AES) and test end-to-end connectivity via the router's wireless radio.

Network Printer (Shared Resource)
A critical office asset with a reserved Static IP. This ensures all devices on the network can consistently communicate with the printer without address conflicts.

Implementation and Verification

Network Topology
The design includes a centralized Wireless-N Router connected to a Cisco Catalyst Switch, which distributes the connection to a high-performance PC and a shared Network Printer.
![Network Topology](topology.png/Screenshot%202026-04-06%20231138.png)

Administrative Security
Web Utility access is protected by a custom authorization layer. Default admin access is strictly controlled to prevent unauthorized configuration changes.

![Security Challenge](Newrouter_security.png%20folder/Screenshot%202026-04-06%20230039.png)

Connectivity Test (Ping)
Successful ICMP echo requests from the Smartphone (192.168.10.17) to the Desktop (192.168.10.10) with 0% packet loss.
![Ping Verification](ping_test.png/Screenshot%202026-04-06%20231621.png)
How to View the Lab

Ensure you have Cisco Packet Tracer 8.0 or higher installed.

Clone this repository or download the .pkt file.

Open the file to explore the detailed configurations and security policies.

Developed as part of my professional network engineering portfolio.
