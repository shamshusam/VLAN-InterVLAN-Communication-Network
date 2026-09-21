# IP Addressing

## Overview

IP addressing is used to provide Layer-3 communication between network devices.

Each PC in the network is assigned an IPv4 address, subnet mask, and default gateway.

## Addressing Table

| Device | VLAN | IP Address | Subnet Mask | Default Gateway |
|---|---:|---|---|---|
| PC0 | 10 | 192.168.10.11 | 255.255.255.0 | 192.168.10.1 |
| PC1 | 10 | 192.168.10.12 | 255.255.255.0 | 192.168.10.1 |
| PC2 | 10 | 192.168.10.13 | 255.255.255.0 | 192.168.10.1 |
| PC3 | 10 | 192.168.10.14 | 255.255.255.0 | 192.168.10.1 |
| PC4 | 10 | 192.168.10.15 | 255.255.255.0 | 192.168.10.1 |
| PC5 | 20 | 192.168.20.11 | 255.255.255.0 | 192.168.20.1 |
| PC6 | 20 | 192.168.20.12 | 255.255.255.0 | 192.168.20.1 |
| PC7 | 20 | 192.168.20.13 | 255.255.255.0 | 192.168.20.1 |
| PC8 | 20 | 192.168.20.14 | 255.255.255.0 | 192.168.20.1 |
| PC9 | 20 | 192.168.20.15 | 255.255.255.0 | 192.168.20.1 |
| PC10 | 30 | 192.168.30.11 | 255.255.255.0 | 192.168.30.1 |
| PC11 | 30 | 192.168.30.12 | 255.255.255.0 | 192.168.30.1 |
| PC12 | 30 | 192.168.30.13 | 255.255.255.0 | 192.168.30.1 |
| PC13 | 30 | 192.168.30.14 | 255.255.255.0 | 192.168.30.1 |
| PC14 | 30 | 192.168.30.15 | 255.255.255.0 | 192.168.30.1 |
| PC15 | 40 | 192.168.40.11 | 255.255.255.0 | 192.168.40.1 |
| PC16 | 40 | 192.168.40.12 | 255.255.255.0 | 192.168.40.1 |
| PC17 | 40 | 192.168.40.13 | 255.255.255.0 | 192.168.40.1 |
| PC18 | 40 | 192.168.40.14 | 255.255.255.0 | 192.168.40.1 |
| PC19 | 40 | 192.168.40.15 | 255.255.255.0 | 192.168.40.1 |

## VLAN Networks

| VLAN | Network Address | Usable IP Range | Default Gateway |
|---|---|---|---|
| VLAN 10 | 192.168.10.0/24 | 192.168.10.1 – 192.168.10.254 | 192.168.10.1 |
| VLAN 20 | 192.168.20.0/24 | 192.168.20.1 – 192.168.20.254 | 192.168.20.1 |
| VLAN 30 | 192.168.30.0/24 | 192.168.30.1 – 192.168.30.254 | 192.168.30.1 |
| VLAN 40 | 192.168.40.0/24 | 192.168.40.1 – 192.168.40.254 | 192.168.40.1 |

## Default Gateway

The default gateway is used by a PC when it needs to communicate with a device outside its local IP network.

In this project, each VLAN has its own default gateway configured on the Layer-3 routing device. This allows communication between different VLANs through inter-VLAN routing.

In this project, the router provides the Layer-3 routing function required for communication between VLANs.

> The exact IP addresses and gateway configuration will be added after verifying the actual Packet Tracer configuration.
