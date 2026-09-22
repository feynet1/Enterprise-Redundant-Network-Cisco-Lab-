# 🏗️ Enterprise Redundant Network Design (Cisco Packet Tracer)

## 📌 Overview
This project demonstrates a **highly available enterprise network topology** built in Cisco Packet Tracer.  
It implements redundancy, scalability, and dynamic routing using real-world networking technologies.

---

## 🎯 Objectives

- Design a **redundant hierarchical network**
- Implement **inter-VLAN routing**
- Ensure **high availability (no single point of failure)**
- Use **dynamic routing (OSPF)**
- Provide **automatic IP assignment (DHCP)**

---

## 🧠 Network Architecture

This project follows a **3-tier architecture**:

- **Access Layer** → 2960 switches (end devices)
- **Distribution Layer** → 3560 multilayer switches (routing + redundancy)
- **Edge Layer** → ISR routers (WAN connectivity)

---

## 🧩 Technologies Used

- **VLANs** — Network segmentation  
- **Trunking (802.1Q)** — VLAN transport  
- **STP (Rapid-PVST)** — Loop prevention  
- **EtherChannel (LACP)** — Link aggregation  
- **Inter-VLAN Routing (SVI)** — Layer 3 switching  
- **HSRP** — Gateway redundancy  
- **OSPF** — Dynamic routing  
- **DHCP** — Automatic IP assignment  

---

## 🌐 VLAN & IP Scheme

| VLAN | Name  | Network            | Gateway (HSRP) |
|------|------|------------------|----------------|
| 10   | SALES | 192.168.10.0/24 | 192.168.10.254 |
| 20   | HR    | 192.168.20.0/24 | 192.168.20.254 |
| 30   | IT    | 192.168.30.0/24 | 192.168.30.254 |
| 40   | MGMT  | 192.168.40.0/24 | 192.168.40.254 |

---

## 🔁 Redundancy Features

- Dual-homed access switches  
- HSRP for default gateway failover  
- EtherChannel between core switches  
- STP root load balancing  
- OSPF dynamic failover  
