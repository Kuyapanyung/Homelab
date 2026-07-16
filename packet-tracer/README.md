# Packet Tracer Homelab

## Objective

This Packet Tracer project represents the logical design of my homelab before implementing it in Proxmox and pfSense.

## Network Topology

![Homelab Topology](topology.png)

## Devices

- Internet (PT-Cloud)
- Home Router
- pfSense Firewall (simulated using Cisco 2911)
- Cisco 2960 LAN Switch
- Ubuntu Desktop
- Alpine Desktop
- Lubuntu Desktop

## IP Addressing

| Device | IP Address |
|---------|------------|
| Home Router | 192.168.1.1/24 |
| pfSense WAN | 192.168.1.2/24 |
| pfSense LAN | 192.168.99.1/24 |
| Ubuntu Desktop | 192.168.99.10/24 |
| Alpine Desktop | 192.168.99.11/24 |
| Lubuntu Desktop | 192.168.99.12/24 |

## Purpose

This simulation is used to:

- Plan the homelab network before implementation.
- Practice routing and IP addressing.
- Understand network topology and device connectivity.
- Compare the simulated design with the actual Proxmox-based homelab.