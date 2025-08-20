---
title: "Networking Notes: ARP and DHCP"
date: 2025-08-20 11:00:00 +0800
tags: [Networks, Try-Hack-Me]
categories: [journal]
---

# Networking Notes: ARP and DHCP

## Address Resolution Protocol (ARP)

Devices have two key identifiers:  
- **MAC address** (hardware/physical identifier)  
- **IP address** (logical identifier on a network)

ARP allows devices to associate their IP addresses with their MAC addresses.

### How ARP Works
- Each device keeps an **ARP cache** (a table mapping IP addresses to MAC addresses).  
- When a device wants to talk to another device in the same subnet but doesn’t know its MAC address:  
  1. **ARP Request** – Broadcast: “Who has IP 192.168.0.5? Tell me your MAC.”  
  2. **ARP Reply** – Device with that IP replies directly: “That’s me, my MAC is `aa:bb:cc:dd:ee:ff`.”  
- The requesting device stores the mapping in its cache for a short time.  
- If the cache expires, ARP requests are sent again as needed.  

**Key Point**:  
ARP does not proactively scan the network. It only asks when needed.  
That’s why running `arp -a` shows only devices your computer recently communicated with.

---

## Dynamic Host Configuration Protocol (DHCP)

DHCP automatically assigns IP addresses to devices, so users don’t need to configure them manually.

### The DHCP Process
1. **Discover** – Device sends a broadcast looking for DHCP servers.  
2. **Offer** – DHCP server replies with an available IP address.  
3. **Request** – Device replies, asking to use that IP.  
4. **ACK** – DHCP server confirms and the device starts using the IP.  

This is known as the **DORA process** (Discover, Offer, Request, ACK).

### Where is the DHCP Server?
- **Home networks:** Usually built into the router, handing out private IPs like `192.168.x.x`.  
- **Corporate networks:** Often a dedicated DHCP server (e.g., Windows Server, Linux). The router forwards DHCP requests to it.

### Static IPs and Conflicts
- If you manually assign a static IP that’s already in use, it creates an **IP address conflict**.  
- Effects:  
  - Both devices may lose connectivity.  
  - ARP tables can’t resolve which MAC owns the IP.  
- **Best practice:**  
  - Assign static IPs **outside the DHCP pool** (e.g., router uses `192.168.0.100–200`, so you use `192.168.0.10` or `192.168.0.250`).  
  - Or configure a **DHCP reservation** so a device always gets the same IP automatically.

---
