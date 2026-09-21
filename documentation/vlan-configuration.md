# VLAN Configuration

## Overview

VLANs (Virtual Local Area Networks) are used to logically divide the physical network into separate broadcast domains.

In this project, 20 PCs are connected through four Cisco 2960 switches. Four VLANs are configured to organize the PCs into separate logical network groups.

Inter-VLAN communication is enabled through the Cisco 2811 router.

## Network Devices

- SW0 - Cisco 2960
- SW1 - Cisco 2960
- SW2 - Cisco 2960
- SW3 - Cisco 2960
- R1 - Cisco 2811 Router
- 20 PCs

## VLAN Assignment

| VLAN | Purpose | Network | Default Gateway |
|------|---------|---------|-----------------|
| VLAN 10 | Network Group 1 | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 20 | Network Group 2 | 192.168.20.0/24 | 192.168.20.1 |
| VLAN 30 | Network Group 3 | 192.168.30.0/24 | 192.168.30.1 |
| VLAN 40 | Network Group 4 | 192.168.40.0/24 | 192.168.40.1 |

## PC VLAN Assignment

| VLAN | Connected PCs |
|------|---------------|
| VLAN 10 | PC0, PC1, PC2, PC3, PC4 |
| VLAN 20 | PC5, PC6, PC7, PC8, PC9 |
| VLAN 30 | PC10, PC11, PC12, PC13, PC14 |
| VLAN 40 | PC15, PC16, PC17, PC18, PC19 |

## Access Ports

PC-facing switch ports are configured as access ports.

Each access port is assigned to the appropriate VLAN based on the connected PC.

Example:

```text
interface fastEthernet 0/1
switchport mode access
switchport access vlan 10
