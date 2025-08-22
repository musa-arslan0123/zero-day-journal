---
title: "Networking Notes: OSI Model (Part 1)"
date: 2025-08-20 12:30:00 +0800
tags: [Networks, Try-Hack-Me]
categories: [journal, OSI-Model]
---

# Networking Notes: OSI Model (Part 1)

The **OSI model** (Open Systems Interconnection) is a framework that defines how devices communicate across a network. It provides a universal structure so that hardware and software from different vendors can interoperate.  

Each layer in the OSI model has its own responsibilities, and data is passed through these layers as it moves across a network. For now, we’ll look at the first four layers.

---

## Physical Layer (Layer 1)
- **Description:** Concerned with the physical components of networking.  
- Devices use **electrical signals** (1s and 0s) to transfer data.  
- Examples: Ethernet cables, fiber optics, hubs.  

---

## Data Link Layer (Layer 2)
- **Description:** Handles **physical addressing** using MAC addresses.  
- Receives packets from the network layer and adds the **MAC address** of the receiving endpoint.  
- Every NIC (Network Interface Card) has a unique MAC address burned in by the manufacturer (though it can be spoofed).  
- Also presents the data in a format suitable for transmission.  
- Devices: switches, NICs.  

---

## Network Layer (Layer 3)
- **Description:** Responsible for **routing** and determining the optimal path for data.  
- Works with **IP addresses** (e.g., `192.168.1.100`).  
- Routing decisions can be based on:
  - Shortest path (fewest hops).
  - Reliability (packet loss history).
  - Connection speed (fiber vs copper).  
- Protocols: **OSPF**, **RIP**, **ICMP**.  
- Devices: routers (Layer 3 devices).  

---

## Transport Layer (Layer 4)
- **Description:** Ensures reliable (or fast) delivery of data.  
- Two main protocols: **TCP** and **UDP**.  

### Transmission Control Protocol (TCP)
- **Advantages:**
  - Guarantees accurate, ordered delivery of data.
  - Synchronises devices to avoid overwhelming the receiver.
- **Disadvantages:**
  - Slower due to reliability overhead.
  - Requires a stable connection.  
- **Use cases:** file transfers, email, web browsing.

### User Datagram Protocol (UDP)
- **Advantages:**
  - Faster, lightweight, no connection overhead.
  - Good for real-time data streams.
- **Disadvantages:**
  - No error checking or guarantee of delivery.
  - Data can be lost without notice.  
- **Use cases:** video streaming, VoIP, discovery protocols (e.g., ARP, DHCP).

---

## Summary
- **Layer 1 (Physical):** Hardware and signals.  
- **Layer 2 (Data Link):** MAC addressing and framing.  
- **Layer 3 (Network):** Routing and IP addressing.  
- **Layer 4 (Transport):** TCP vs UDP for delivery.  

Further layers (Session, Presentation, Application) will be covered later.  

---
