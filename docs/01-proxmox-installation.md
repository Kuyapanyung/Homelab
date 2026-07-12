# 01 - Proxmox VE Host Documentation

## Overview

This document describes the deployment and current configuration of my Proxmox VE host, which serves as the virtualization platform for my networking homelab.

---

## Objective

- Learn enterprise virtualization using Proxmox VE
- Host multiple virtual machines for networking and Linux administration
- Build a practical environment for Network Engineering and Cloud Infrastructure

---

## Hardware Specifications

| Component | Specification |
|-----------|---------------|
| Device | HP EliteDesk 800 G1 Mini |
| CPU | Intel Core i5-4590T |
| CPU Cores | 4 Cores / 4 Threads |
| RAM | 8 GB DDR3 |
| Storage | 500 GB HGST 7200 RPM HDD |
| Architecture | x86_64 |
| Virtualization | Intel VT-x |

---

## Software

| Item | Value |
|------|-------|
| Hypervisor | Proxmox VE |
| Virtualization | KVM & LXC |
| Boot Mode | UEFI |
| Storage | LVM-Thin |

---

## Storage Layout

| Storage | Purpose |
|---------|---------|
| local | ISO images, backups, templates |
| local-lvm | Virtual machine disks |

---

## Virtual Machines

| VM | Operating System | Purpose |
|----|------------------|---------|
| pfSense | pfSense CE | Router & Firewall |
| Ubuntu | Ubuntu Server | Linux Administration |

---

## Network Configuration

| Interface | Purpose |
|-----------|---------|
| vmbr0 | Management Bridge |

---

## Current Topology

```text
                 Internet
                     │
               ISP Router
                     │
        ┌─────────────────────┐
        │ HP EliteDesk 800 G1 │
        │     Proxmox VE      │
        └──────────┬──────────┘
                   │
                vmbr0
                   │
        ┌──────────┴──────────┐
        │                     │
     pfSense             Ubuntu Server
```

---

## Current Status

- ✅ Proxmox installed
- ✅ Management interface configured
- ✅ Storage configured
- ✅ pfSense deployed
- ✅ Ubuntu Server deployed

---

## Future Improvements

- Deploy Windows Server
- Configure VLANs
- Install Docker
- Configure Grafana Monitoring
- Configure WireGuard VPN
- Create automated backups

---

## Lessons Learned

- Proxmox uses Linux Bridges for virtual networking.
- Intel VT-x provides hardware-assisted virtualization.
- LVM-Thin allows efficient allocation of virtual disks.
- Resource planning is important when running multiple VMs.

---

## References

- https://www.proxmox.com/
- https://pve.proxmox.com/wiki/Main_Page
