# Cisco Packet Tracer

Before implementing configurations in my physical homelab, I first design, simulate, and validate the network using Cisco Packet Tracer.

This allows me to understand networking concepts, verify configurations, troubleshoot issues, and reduce deployment errors before applying them to my Proxmox and pfSense homelab.

---

## Topology

This Packet Tracer project simulates an enterprise network consisting of:

- Home Router (ISP Simulation)
- pfSense Router (Router-on-a-Stick)
- Cisco 2960 Switch
- Ubuntu Server
- Alpine Linux Server
- Lubuntu Client
- Multiple VLANs

---

## Features Implemented

- ✅ Network Topology Design
- ✅ Home Router Configuration
- ✅ pfSense Router Simulation
- ✅ Switch Port Configuration
- ✅ VLAN Configuration
- ✅ IEEE 802.1Q Trunking
- ✅ Router-on-a-Stick
- ✅ Inter-VLAN Routing
- ✅ DHCP Configuration
- ✅ DNS Configuration
- ⏳ Access Control Lists (ACL)
- ⏳ SSH Management
- ⏳ Port Security
- ⏳ STP
- ⏳ EtherChannel

---

## Files

| File | Description |
|------|-------------|
| `homelab-network.pkt` | Cisco Packet Tracer project |
| `Homelab-topology-updated.png` | Updated network topology |
| `packet-tracer-guide.md` | Step-by-step Packet Tracer documentation |

---

## Screenshots

Configuration screenshots are located in:

```text
../screenshots/packet-tracer/
```

These include:

- Network topology
- Home Router configuration
- pfSense configuration
- VLAN configuration
- Switch configuration
- Router subinterfaces
- DHCP configuration
- DHCP bindings
- DNS configuration
- Connectivity verification

---

## Purpose

This Packet Tracer project serves as a learning environment before implementing the same concepts in my physical homelab running:

- Proxmox VE
- pfSense
- Ubuntu Server
- Alpine Linux
- Lubuntu Desktop

The goal is to build confidence with Cisco networking concepts before deploying them in a real virtualized environment.