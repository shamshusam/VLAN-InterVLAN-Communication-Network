# VLAN Segmentation and Inter-VLAN Communication Using Cisco Packet Tracer

## 📌 Project Overview

This project demonstrates the design and implementation of a multi-switch network using **Cisco Packet Tracer**.

The network consists of **20 PCs, 4 Cisco 2960 switches, and 1 Cisco 2811 router**. VLANs are used to logically separate network devices, while the router is used to enable communication between different VLANs.

The project focuses on understanding:

- VLAN configuration
- Switch-to-switch connectivity
- Router connectivity
- IP addressing
- Default gateways
- Inter-VLAN communication
- Network connectivity testing

---

## 🖥️ Network Topology

![Network Topology](topology/network-topology.png)

### Devices Used

| Device | Quantity | Purpose |
|---|---:|---|
| Cisco 2811 Router | 1 | Inter-VLAN routing |
| Cisco 2960 Switch | 4 | VLAN and LAN switching |
| PCs | 20 | End devices |

---

## 🔌 Network Structure

The network contains one central switch (`SW0`) connected to the router and the other switches.

```text
                         ┌──────────────┐
                         │  Cisco 2811  │
                         │      R1      │
                         └───────┬──────┘
                                 │
                                 │
                         ┌───────▼──────┐
                         │     SW0      │
                         │  Cisco 2960  │
                         └──┬────┬────┬─┘
                            │    │    │
                 ┌──────────┘    │    └──────────┐
                 │               │               │
          ┌──────▼──────┐ ┌─────▼──────┐ ┌──────▼──────┐
          │     SW1     │ │    SW3     │ │     SW2     │
          │ Cisco 2960  │ │ Cisco 2960 │ │ Cisco 2960  │
          └──────┬──────┘ └─────┬──────┘ └──────┬──────┘
                 │              │               │
              PC5-PC9       PC15-PC19       PC10-PC14

                         SW0 → PC0-PC4
```

---

## 💻 PC Distribution

The PCs are distributed across the four switches as follows:

| Switch | Connected PCs |
|---|---|
| SW0 | PC0 – PC4 |
| SW1 | PC5 – PC9 |
| SW2 | PC10 – PC14 |
| SW3 | PC15 – PC19 |

---

## 🧩 VLAN Concept

VLANs (Virtual Local Area Networks) are used to divide a physical network into multiple logical networks.

Each VLAN represents a separate broadcast domain.

For example:

```text
VLAN 10 → Network Group 1
VLAN 20 → Network Group 2
VLAN 30 → Network Group 3
VLAN 40 → Network Group 4
```

> The exact VLAN IDs and IP addressing used in this project will be documented according to the actual Packet Tracer configuration.

---

## 🔀 Inter-VLAN Communication

Devices belonging to different VLANs are logically separated at Layer 2.

To allow communication between different VLANs, traffic must pass through a Layer 3 device.

In this project, the **Cisco 2811 router (R1)** provides the routing function.

Conceptually:

```text
PC in VLAN A
      │
      ▼
   Switch
      │
      ▼
    Router
      │
      ▼
   Switch
      │
      ▼
PC in VLAN B
```

The router receives traffic from one VLAN, performs routing, and forwards the traffic toward the destination VLAN.

---

## 🌐 IP Addressing

The IP addresses, subnet masks, and default gateways used in the actual Packet Tracer implementation will be documented here.

| VLAN | Network Address | Subnet Mask | Default Gateway |
|---|---|---|---|
| VLAN 10 | To be added | To be added | To be added |
| VLAN 20 | To be added | To be added | To be added |
| VLAN 30 | To be added | To be added | To be added |
| VLAN 40 | To be added | To be added | To be added |

---

## ⚙️ Configuration

The configuration includes:

1. Creating VLANs
2. Assigning switch ports to VLANs
3. Configuring connections between switches
4. Configuring the router
5. Assigning IP addresses to PCs
6. Configuring default gateways
7. Enabling communication between VLANs

Actual configuration commands will be added to the `configuration` directory.

---

## 🧪 Network Testing

Connectivity can be verified using the following tests:

### 1. Same-VLAN Communication

A PC communicates with another PC belonging to the same VLAN.

```text
PC → PC
```

### 2. Inter-VLAN Communication

A PC belonging to one VLAN communicates with a PC belonging to another VLAN.

```text
VLAN A → Router → VLAN B
```

### 3. Ping Test

The `ping` command can be used to verify connectivity.

Example:

```text
ping <destination-ip-address>
```

Successful replies confirm IP connectivity between the devices.

---

## 📁 Repository Structure

```text
VLAN-InterVLAN-Communication-Network/
│
├── README.md
│
├── topology/
│   └── network-topology.png
│
├── configuration/
│   ├── router-config.txt
│   └── switch-config.txt
│
├── documentation/
│   ├── vlan-configuration.md
│   ├── ip-addressing.md
│   └── inter-vlan-communication.md
│
└── screenshots/
    ├── vlan-verification.png
    ├── ip-configuration.png
    └── ping-test.png
```

---

## 📚 What I Learned

Through this project, I practiced:

- Understanding VLANs
- Creating and managing VLANs on switches
- Assigning switch ports to VLANs
- Understanding broadcast domains
- Connecting multiple switches
- Understanding router-based inter-VLAN communication
- Configuring IP addresses
- Configuring default gateways
- Testing network connectivity using `ping`
- Troubleshooting basic network connectivity

---

## 🚀 Future Improvements

Possible improvements to this network include:

- DHCP server configuration
- Network redundancy
- Spanning Tree Protocol (STP)
- EtherChannel
- Access Control Lists (ACLs)
- Dynamic routing protocols
- Network monitoring
- Improved IP addressing and subnetting
- Adding additional network services

---

## 🛠️ Tools Used

- **Cisco Packet Tracer**
- Cisco 2811 Router
- Cisco 2960 Switch
- Ethernet connections
- IPv4 addressing
- VLANs
- Inter-VLAN routing

---

## 👨‍💻 Project Author

**Shamshuddin Sam**

Electronics Engineer | Network Engineer Trainee

Interested in:

- Networking
- IoT
- Network Infrastructure
- Electronics
- Automation
- Technology

---

⭐ If you found this project useful, feel free to explore the repository.
