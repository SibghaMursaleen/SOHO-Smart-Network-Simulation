# 🌐 SOHO Smart Network Simulation

<div align="center">

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco_Packet_Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)
![IoT](https://img.shields.io/badge/IoT_Integration-FF6F00?style=for-the-badge&logo=internetofthings&logoColor=white)
![Network](https://img.shields.io/badge/SOHO_Network-00897B?style=for-the-badge&logo=networkx&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

**A smart and secure Small Office/Home Office (SOHO) network simulation with IoT integration, built using Cisco Packet Tracer.**

*Guided by **Engr. Irfan Younas***

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Network Topology & IP Addressing](#-network-topology--ip-addressing)
- [Features](#-features)
- [Tools & Technologies](#-tools--technologies)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Objectives](#-objectives)
- [Author](#-author)
- [License](#-license)

---

## 🔍 Overview

This project demonstrates the end-to-end design and simulation of a **Small Office/Home Office (SOHO)** network integrated with **IoT smart devices**, developed in **Cisco Packet Tracer**. The simulation covers wired and wireless connectivity, real-time sensor monitoring, home automation, and basic network security — reflecting the architecture of a modern smart workplace.

The project bridges traditional SOHO networking concepts with emerging IoT technologies, providing a practical understanding of how smart devices communicate securely within a local network environment.

---

## 🗺️ Network Topology & IP Addressing

The network is structured into two primary zones — the **Office Zone** (wired) and the **Home/IoT Zone** (wireless) — connected through a central wireless router.

### Network Overview

| Zone | Subnet | Subnet Mask | Usable Range | Default Gateway |
|------|--------|-------------|--------------|-----------------|
| Office LAN (Wired) | `192.168.1.0` | `255.255.255.0` | `192.168.1.1 – 192.168.1.254` | `192.168.1.1` |
| IoT / Wireless Zone | `192.168.2.0` | `255.255.255.0` | `192.168.2.1 – 192.168.2.254` | `192.168.2.1` |

### Device IP Assignments

| Device | IP Address | Type | Zone |
|--------|-----------|------|------|
| Wireless Router | `192.168.1.1` / `192.168.2.1` | Gateway | Both |
| PC 1 (Admin) | `192.168.1.10` | Wired Client | Office LAN |
| PC 2 | `192.168.1.11` | Wired Client | Office LAN |
| Server (IoT/Home Gateway) | `192.168.1.20` | Server | Office LAN |
| Managed Switch | `192.168.1.2` | Layer 2 Switch | Office LAN |
| Smart Thermostat | `192.168.2.10` | IoT Device | Wireless/IoT |
| Smart Fan | `192.168.2.11` | IoT Device | Wireless/IoT |
| Smart Light | `192.168.2.12` | IoT Device | Wireless/IoT |
| Motion Sensor | `192.168.2.13` | IoT Sensor | Wireless/IoT |
| Temperature Sensor | `192.168.2.14` | IoT Sensor | Wireless/IoT |
| Laptop (Remote Access) | `192.168.2.20` | Wireless Client | Wireless/IoT |

> **Note:** IP addresses above are representative of the simulation configuration. Refer to the `.pkt` file for exact device-level settings.

### Topology Diagram (Logical)

```
         [Internet / Cloud]
                |
         [Wireless Router]
         192.168.1.1 / 192.168.2.1
          /               \
[Office LAN]           [Wireless/IoT Zone]
  (Wired)                   (Wi-Fi)
     |                          |
[Switch]              [Smart Devices & Sensors]
  /   \                 - Smart Thermostat
[PC1] [PC2]            - Smart Fan / Light
       |                - Motion Sensor
    [Server]            - Temperature Sensor
  (IoT Gateway)         - Laptop
```

---

## ✨ Features

- ✅ **Hybrid SOHO Topology** — Combines wired Ethernet (Office LAN) and wireless (IoT Zone) in a unified network
- ✅ **IoT Device Integration** — Smart fans, lights, thermostats, and environmental sensors
- ✅ **Real-Time Sensor Monitoring** — Motion and temperature sensors feed live data to the IoT server
- ✅ **Home Automation Logic** — IoT devices respond automatically to sensor triggers
- ✅ **Wired + Wireless Connectivity** — Managed switch for wired clients; wireless router for mobile/IoT devices
- ✅ **Access Control & Security** — Basic firewall rules and access restrictions configured on the router
- ✅ **Centralized IoT Server** — Acts as the local home automation hub, receiving and processing sensor data
- ✅ **Remote Monitoring** — Wireless laptop simulates remote access to IoT dashboard

---

## 🔧 Tools & Technologies

| Tool / Technology | Purpose |
|-------------------|---------|
| **Cisco Packet Tracer** | Network simulation and design environment |
| **Wireless Router** | Central gateway; bridges LAN and wireless zones |
| **Managed Switch** | Layer 2 switching for office wired clients |
| **PCs & Laptop** | End-user devices for testing and remote access |
| **IoT Server** | Central controller for smart device automation |
| **Smart Fan / Light** | Actuator IoT devices controlled via server |
| **Smart Thermostat** | Temperature-based automation device |
| **Motion Sensor** | Detects movement; triggers lighting/alarms |
| **Temperature Sensor** | Monitors ambient temperature for HVAC control |
| **Packet Tracer Scripting** | Logic blocks for IoT condition/response automation |

---

## 📁 Project Structure

```
SOHO-Smart-Network-Simulation/
│
├── SOHO Network .pkt        # Cisco Packet Tracer simulation file (main project)
└── README.md                # Project documentation (this file)
```

---

## 🚀 Getting Started

### Prerequisites

- **Cisco Packet Tracer** version **8.0 or later** installed  
  *(Download from [Cisco NetAcad](https://www.netacad.com/courses/packet-tracer) — free registration required)*

### Steps to Run the Simulation

1. **Clone or download** this repository:
   ```bash
   git clone https://github.com/SibghaMursaleen/SOHO-Smart-Network-Simulation.git
   ```

2. **Open Cisco Packet Tracer** on your machine.

3. **Load the simulation file:**
   - Go to `File` → `Open`
   - Navigate to the cloned/downloaded folder
   - Select `SOHO Network .pkt` and click **Open**

4. **Explore the topology:**
   - Use the **Logical View** to see device connections and zones
   - Click on any device to inspect its IP configuration and interfaces

5. **Run the simulation:**
   - Switch to **Simulation Mode** (bottom-right clock icon)
   - Generate traffic (e.g., ping between PCs, trigger sensors)
   - Observe IoT responses and packet flow in real time

6. **Inspect IoT automation:**
   - Click on the **IoT Server** → **Services** tab to view registered smart devices
   - Check **Smart Devices** for condition/action rules set up in the simulation

---

## 🎯 Objectives

- Design and implement a fully functional **SOHO network** from scratch
- Integrate **IoT sensors and actuators** into the network infrastructure
- Simulate **real-time communication** between smart devices and a centralized server
- Apply **subnetting** and **IP addressing** best practices in a dual-zone environment
- Implement **access control** and **basic network security** policies
- Demonstrate convergence of **traditional networking** and **modern IoT technologies**

---

## 👤 Author

**Sibgha Mursaleen**  
*Computer Networks | IoT & SOHO Network Design*

- 🔗 GitHub: [@SibghaMursaleen](https://github.com/SibghaMursaleen)

**Supervised by:** *Engr. Irfan Younas*

---

## 📄 License

This project is intended for **educational purposes only**.  
All network designs and simulations are created for academic learning within the Cisco Packet Tracer environment.

---

<div align="center">

*If you found this project helpful, consider giving it a ⭐ on GitHub!*

</div>
