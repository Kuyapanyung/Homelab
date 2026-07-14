# Homelab Infrastructure Overview

## Project Overview

This homelab is a personal learning environment built to gain hands-on experience with enterprise networking, virtualization, Linux administration, and firewall management.

The goal of this project is to simulate a small enterprise network while developing practical skills required for Network Engineer, Network Operations Center (NOC), and Cloud Infrastructure roles.

---

# Objectives

- Learn Proxmox VE virtualization
- Deploy and manage multiple virtual machines
- Configure pfSense as a virtual firewall and router
- Practice Linux server administration
- Build virtual network topologies
- Document every deployment and troubleshooting process
- Develop a professional GitHub portfolio

---

# Physical Hardware

| Component | Specification |
|-----------|---------------|
| Host Machine | HP EliteDesk 800 G1 Mini |
| CPU | Intel Core i5-4590T @ 2.00 GHz |
| RAM | 16 GB DDR3 |
| Storage | 500 GB HGST HDD |
| Hypervisor | Proxmox VE 9.1.1 |

---

# Virtual Infrastructure

| VM | Purpose | Status |
|----|---------|--------|
| pfSense | Firewall, Router, NAT | ✅ Running |
| Ubuntu Server | Linux administration and networking | ✅ Running |
| Alpine Linux | Lightweight Linux and package management | ✅ Running |

More virtual machines will be added as the homelab expands.

---

# Network Architecture

## vmbr0

Purpose:

- Physical network bridge
- Connected to the home router
- Provides WAN connectivity
- Used for Proxmox management

## vmbr1

Purpose:

- Internal virtual switch
- Connected to the pfSense LAN interface
- Used for communication between virtual machines

---

# Current Topology

```text
                    Internet
                        │
                        │
                 Home Router
                        │
                  192.168.1.0/24
                        │
                    vmbr0 (WAN)
                        │
                 +----------------+
                 |    Proxmox VE  |
                 +----------------+
                        │
            ┌───────────┴───────────┐
            │                       │
         pfSense WAN             vmbr1 (LAN)
                                    │
                    ┌───────────────┴──────────────┐
                    │                              │
             Ubuntu Server                  Alpine Linux
```

---

# Repository Structure

```
Homelab/
│
├── docs/
│   ├── 00-homelab-overview.md
│   ├── 01-proxmox-installation.md
│   ├── 02-pfsense-installation.md
│   ├── 03-ubuntu-server.md
│   ├── 04-vlan-configuration.md
│   ├── 05-firewall-rules.md
│   ├── 06-dhcp-dns.md
│   ├── 07-wireguard-vpn.md
│   ├── 08-monitoring.md
│   ├── 09-troubleshooting.md
│   └── 10-alpine-linux.md
│
├── screenshots/
│
├── diagrams/
│
└── scripts/
```

---

# Skills Practiced

## Virtualization

- Proxmox VE
- Virtual Machines
- Virtual Networking
- Linux Bridges

## Networking

- TCP/IP
- Routing
- NAT
- DHCP
- DNS
- Firewall Rules
- VLANs (Upcoming)

## Linux

- Ubuntu Server
- Alpine Linux
- SSH
- Package Management
- Network Troubleshooting

## Documentation

- Markdown
- Git
- GitHub
- Infrastructure Documentation

---

# Lessons Learned

Throughout this project, every deployment is documented together with the problems encountered and the solutions used to resolve them.

Examples include:

- Incorrect pfSense WAN/LAN bridge assignment
- Initial Ubuntu network connectivity verification
- Alpine Linux package management
- Linux networking fundamentals

The objective is not only to build the infrastructure but also to document the troubleshooting process, reflecting real-world operational practices.

---

# Future Roadmap

The homelab will continue to expand with additional technologies, including:

- VLAN segmentation
- pfSense Firewall Rules
- DHCP & DNS Services
- WireGuard VPN
- Docker
- Monitoring (Grafana / Prometheus)
- Active Directory
- Windows Server
- Reverse Proxy
- Kubernetes (Long-term Goal)

---

# About This Project

This homelab serves as a practical learning platform for developing skills in networking, Linux administration, virtualization, and cloud infrastructure.

Every configuration, deployment, and troubleshooting step is documented to create a professional portfolio while continuously improving hands-on technical experience.