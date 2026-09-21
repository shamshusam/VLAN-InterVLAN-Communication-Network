# Inter-VLAN Communication

## Overview

VLANs separate devices into different Layer-2 broadcast domains.

For a device in one VLAN to communicate with a device in another VLAN, the traffic must pass through a Layer-3 routing device.

In this project, the **Cisco 2811 router (R1)** is used to provide inter-VLAN communication between VLAN 10, VLAN 20, VLAN 30, and VLAN 40.

---

## VLAN Gateway Configuration

Each VLAN has a dedicated gateway configured on Router R1.

| VLAN | Network | Default Gateway |
|---|---|---|
| VLAN 10 | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 20 | 192.168.20.0/24 | 192.168.20.1 |
| VLAN 30 | 192.168.30.0/24 | 192.168.30.1 |
| VLAN 40 | 192.168.40.0/24 | 192.168.40.1 |

The router receives traffic from one VLAN and forwards it to the appropriate destination VLAN.

---

## Traffic Flow

A typical communication path is:

```text
Source PC
   │
   ▼
Access Switch
   │
   ▼
Trunk / Uplink
   │
   ▼
Router R1
   │
   ▼
Inter-VLAN Routing
   │
   ▼
Destination VLAN
   │
   ▼
Destination Switch
   │
   ▼
Destination PC
