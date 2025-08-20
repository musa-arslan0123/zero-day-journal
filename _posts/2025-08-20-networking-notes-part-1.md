---
title: "Networking Notes LAN Topologies and Subnetting"
date: 2025-08-20 10:00:00 +0800
tags: [Networks, Try-Hack-Me]
categories: [journal]
---

# Networking Notes

## Local Area Network (LAN) Topologies
When we talk about "topology" in networking, we are referring to the design or structure of the network. There are several types of topologies, each with its advantages and disadvantages.

### Star Topology
- **Description:** Devices are connected individually via a central networking device such as a switch or hub.
- **Advantages:**
  - Reliable and scalable.
  - Easy to add more devices as demand increases.
- **Disadvantages:**
  - More expensive due to cabling and networking equipment.
  - Requires more maintenance as it scales.
  - If the central device fails, connected devices cannot communicate.

### Bus Topology
- **Description:** Uses a single backbone cable with devices branching off it.
- **Advantages:**
  - Simple and cost-efficient to set up.
- **Disadvantages:**
  - Quickly becomes slow and bottlenecked with more devices.
  - Troubleshooting is difficult since all data travels on the same path.
  - Single point of failure — if the backbone cable fails, the whole network goes down.

### Ring Topology
- **Description:** Devices are connected in a loop, with data passed around until it reaches the destination.
- **Advantages:**
  - Requires less cabling and dedicated hardware.
  - Easy to troubleshoot faults due to the single path.
  - Less prone to bottlenecks compared to bus topology.
- **Disadvantages:**
  - Data can take inefficient routes, travelling through many devices.
  - A single cut or failed device breaks the whole network.

---

## What is a Switch?
- **Definition:** A dedicated device that connects multiple devices (computers, printers, servers) within a network via Ethernet ports.
- **Ports:** Common sizes are 4, 8, 16, 24, 32, and 64 ports.
- **How it works:** 
  - Unlike hubs, switches keep track of which device is connected to each port.
  - When receiving data, a switch forwards it only to the intended target instead of broadcasting to all ports.
  - This reduces unnecessary network traffic and improves efficiency.
- **Use case:** Found in businesses, schools, and larger networks with many devices.
- **Redundancy:** Switches can connect to routers (or other switches), providing multiple paths. If one path fails, traffic can reroute.

---

## What is a Router?
- **Definition:** A device that connects different networks and directs data between them.
- **How it works:**
  - Uses **routing**, the process of finding a path for data to travel across networks.
  - Essential when multiple paths exist, ensuring data reaches the right destination.
- **Example:** Your home router connects your internal network (LAN) to your ISP’s network and the internet.

---

## Subnets and IP Address Roles
Subnets divide a network into smaller, manageable sections. IP addresses within a subnet serve three purposes:

| Type              | Purpose                                                                 | Explanation                                                                                   | Example         |
|-------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------|
| **Network Address** | Identifies the subnet itself.                                          | Shared by all devices in that subnet. Defines the "network’s existence."                      | `192.168.1.0`   |
| **Host Address**    | Identifies a device within the subnet.                                | Each device has a unique host address within the network.                                      | `192.168.1.100` |
| **Default Gateway** | Provides access to other networks outside the subnet (usually a router). | Data leaving the subnet is sent to the gateway. Commonly `.1` or `.254`.                      | `192.168.1.254` |

### Quick Analogy
- **Network address = Street name** (defines the street).
- **Host address = House number** (identifies each house on the street).
- **Default gateway = Street exit** (the way out to other streets/networks).

---
