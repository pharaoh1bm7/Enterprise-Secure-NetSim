# Enterprise-Secure-NetSim
<img width="1882" height="829" alt="Screenshot 2026-04-03 083230" src="https://github.com/user-attachments/assets/70ecc79e-990f-4fc7-8093-6aed26bed5ab" />

# Enterprise-Secure-NetSim 🌐🛡️

A comprehensive network simulation project designed in **Cisco Packet Tracer**, featuring a multi-region architecture with advanced routing protocols and security implementations.

## 🚀 Project Overview
This project simulates a corporate network connecting four distinct subnets across multiple routers. It demonstrates the integration of security appliances (Cisco ASA 5506-X) within a routed environment, ensuring secure inter-VLAN communication and external connectivity.

## 🏗️ Topology Architecture
- **Routers:** 4x Cisco 2911/2901 Routers.
- **Security:** Cisco ASA 5506-X Firewall for traffic inspection and access control.
- **End Devices:** Heterogeneous mix of PCs, Laptops, and Servers.
- **Connectivity:** Serial and Gigabit Ethernet links with sub-interface configurations.

## 🛠️ Key Configurations
### 1. Routing Strategy
- **Static Routing:** Implemented across all routers for precise traffic flow control.
- **Default Routes:** Configured on edge routers (Router 2 & Router 4) to ensure return-path connectivity for all subnets.

### 2. Security (ASA 5506-X)
- **ICMP Inspection:** Enabled via global policy to allow bidirectional diagnostic traffic (Ping) across security levels.
- **Interface Security Levels:** Segmented into 'Inside' and 'Outside' zones for traffic prioritization.

### 3. IP Addressing Schema
- **Subnet 1 (Admin):** 192.168.1.0/24
- **Subnet 2 (Sales):** 192.168.2.0/24
- **Subnet 3 (HR):** 192.168.3.0/24
- **Subnet 4 (Server Farm):** 192.168.5.0/24
- **Point-to-Point Links:** 10.0.0.x/30 infrastructure.

## 📝 Troubleshooting Log
One of the core challenges addressed in this version was the **asymmetric routing and return-path issues** on the 4th subnet. This was resolved by:
- Correcting Next-Hop IP mismatch on Router 3.
- Implementing a recursive static route on Router 4 to handle return packets for remote subnets.

## 📁 How to Use
1. Download the `.pkt` file.
2. Open it using **Cisco Packet Tracer v8.2** or higher.
3. Test connectivity by pinging between Subnet 1 (PC11) and Subnet 4 (Server0).

---
