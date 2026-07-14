# Ubuntu Server Installation

## Objective

Deploy an Ubuntu Server virtual machine on Proxmox to serve as a Linux client for networking practice, Linux administration, and future homelab services.

---

## VM Configuration

| Setting | Value |
|---------|-------|
| Hypervisor | Proxmox VE 9.1.1 |
| Guest OS | Ubuntu Server 26.04 LTS |
| CPU | 2 vCPU |
| Memory | 2 GB |
| Disk | 32 GB (VirtIO) |
| Network Adapter | VirtIO |

---

## Storage Configuration

The default LVM storage layout was selected during installation.

- Boot Partition: 2 GB (ext4)
- Root Filesystem: LVM (ext4)

![Storage Configuration](../screenshots/ubuntu/storage-configuration.png)

---

## Profile Configuration

Created the initial administrator account during installation.

> **Note:** The password is intentionally omitted for security purposes.

![Profile Configuration](../screenshots/ubuntu/profile-configuration.png)

---

## Network Connectivity Verification

After completing the installation, I verified the VM's network connectivity.

### Initial Test

```bash
ping 8.8.8.8
```

Result:

```text
ping: connect: Network is unreachable
```

Next, I tested DNS resolution:

```bash
ping google.com
```

Result:

```text
ping: google.com: Temporary failure in name resolution
```

### After Network Configuration

After resolving the network configuration, I tested again:

```bash
ping google.com
```

Result:

```text
64 bytes from google.com ...
0% packet loss
```

This confirmed that:

- Internet connectivity was working.
- DNS name resolution was functioning correctly.

![Network Connectivity Verification](../screenshots/ubuntu/ping-google-ubuntu.png)

---

## Lessons Learned

- Verified network connectivity using ICMP (`ping`).
- Distinguished between a routing problem (`Network is unreachable`) and a DNS resolution problem (`Temporary failure in name resolution`).
- Confirmed successful Internet connectivity after correcting the network configuration.