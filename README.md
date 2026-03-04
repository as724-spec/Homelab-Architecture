# Homelab STIG and RHEL Compliance Setup

## Overview
This repository documents the architecture, configuration, and security hardening of a distributed homelab environment. The infrastructure is designed to emulate an enterprise Red Hat Enterprise Linux (RHEL) deployment, adhering to DISA STIG guidelines to facilitate RHCSA preparation.

## Hardware Inventory

| Hostname / Node | Hardware Model | CPU | RAM | Storage | Primary Role |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `mgt-thinkpad` | Thinkpad T14 Gen2i | i7-1185G7 | 32GB 3200MHz | 1TB NVMe, 1TB SSD | Admin Workstation / Ansible Control |
| `pve-node-01` | Dell Precision 3561 | i5-11500H | 64GB 3200MHz | 512GB NVMe, 256GB NVMe | Proxmox Hypervisor (Compute) |
| `pve-node-02` | Dell Precision 3551 | i7-10850H | 64GB 2933MHz | 512GB NVMe | Proxmox Hypervisor (Compute) |
| `svc-z240` | HP Z240 | i7-6700 | 16GB 2400MHz | 512GB NVMe, 1TB 2.5" SSD | AlmaLinux Services / Storage |
| `dev-asus` | Asus x712ja | i5-1035G1 | 20GB 3200MHz | 1TB NVMe, 1TB HDD | Fedora Development Environment |
| `test-hp17z` | HP Laptop 17z-ca000 | AMD A9-9425 | 32GB 2400MHz | 256GB 2.5" SSD | Isolated Testing / Break-Fix |

## Network Infrastructure
* **Core Router:** TP-Link AX5400 Pro
* **Distribution Switch:** Netgear 8-port unmanaged 2.5GbE
* **Interfaces:** 2x 2.5GbE USB adapters, 2x 1GbE adapters utilized for Proxmox cluster networking and management separation.
