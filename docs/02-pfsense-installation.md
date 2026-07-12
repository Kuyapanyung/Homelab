# pfSense Could Not Reach Netgate Servers

## Problem

During the initial pfSense installation, the installer displayed:

> Cannot reach the Netgate Servers, please verify your network settings!

### Screenshot

![Netgate Installer Warning](../screenshots/pfsense/installer-warning-netgate.png)

---

## Investigation

Upon reviewing the VM hardware configuration in Proxmox:

![pfSense VM Hardware](../screenshots/pfsense/vm-hardware-network-config.png)

Both virtual network adapters were initially connected to the same bridge:

```text
net0 -> vmbr1
net1 -> vmbr1
```
