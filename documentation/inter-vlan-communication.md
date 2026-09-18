# Inter-VLAN Communication

## Overview

VLANs separate devices into different Layer-2 broadcast domains.

For a device in one VLAN to communicate with a device in another VLAN, the traffic must pass through a Layer-3 routing device.

In this project, the **Cisco 2811 router (R1)** is used for inter-VLAN communication.

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
Routing
   │
   ▼
Destination VLAN
   │
   ▼
Destination Switch
   │
   ▼
Destination PC
