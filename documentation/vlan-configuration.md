# VLAN Configuration

## Overview

VLANs (Virtual Local Area Networks) are used to logically divide the physical network into separate broadcast domains.

In this project, multiple PCs are connected through four Cisco 2960 switches. VLANs are used to organize the network into separate logical groups.

## Network Devices

- SW0 - Cisco 2960
- SW1 - Cisco 2960
- SW2 - Cisco 2960
- SW3 - Cisco 2960
- R1 - Cisco 2811 Router

## VLAN Assignment

The exact VLAN IDs and port assignments used in the Packet Tracer topology will be documented here.

| VLAN | Purpose | Switch | Connected Devices |
|------|---------|--------|-------------------|
| VLAN 10 | Network Group 1 | SW0/SW1/SW2/SW3 | To be documented |
| VLAN 20 | Network Group 2 | SW0/SW1/SW2/SW3 | To be documented |
| VLAN 30 | Network Group 3 | SW0/SW1/SW2/SW3 | To be documented |
| VLAN 40 | Network Group 4 | SW0/SW1/SW2/SW3 | To be documented |

> The VLAN IDs above are placeholders for documentation structure. They should be replaced with the actual VLAN IDs configured in the Packet Tracer project.

## Access Ports

PC-facing switch ports are configured as access ports and assigned to their respective VLANs.

## Trunk Links

Links carrying traffic for multiple VLANs are configured as trunk links where required by the network design.

The trunk configuration allows VLAN traffic to travel between switches and toward the router.

## Verification

VLAN configuration can be verified using commands such as:

```text
show vlan brief
