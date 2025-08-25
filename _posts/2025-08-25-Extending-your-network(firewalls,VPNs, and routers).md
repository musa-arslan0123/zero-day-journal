---
title: "Extending Your Network: Firewalls, VPNs, and Routers Oh My!"
date: 2025-08-22 14:00:00 +0800
tags: [Networks, vpn, firewall, port-forwarding, switches, routers]
categories: [journal, Networking]
---

Building a network isn’t just about cables and blinking lights — it’s about letting the *right* data in, keeping the *wrong* stuff out, and sometimes creating secret tunnels worthy of a spy movie. Let’s talk **port forwarding, firewalls, VPNs, routers, and switches** — the unsung heroes keeping your cat memes flowing safely.

---

## Port Forwarding: Opening the Door (But Only a Crack)

By default, your home network is like a fortress with all the doors shut.  
**Port forwarding** says:  
> “Okay, fine — you can come in, *but only through this door*, and only for this service.”

- **Without port forwarding:** A web server on your laptop is only visible to devices on your home Wi-Fi.  
- **With port forwarding:** Your router forwards traffic from the internet on, say, port **80** (HTTP) straight to your laptop’s web server.

Think of it as telling the mailman:  
> “All pizza deliveries? Left side door. Everything else? Nope.”

But remember: **port forwarding just opens the door**. Whether visitors actually get through depends on the firewall standing right behind it.

---

## Firewalls: The Bouncers of the Internet  

A **firewall** is your network’s bouncer:  
- Checks ID (source address)  
- Checks destination (where you’re headed)  
- Decides if you’re on the guest list (the right port, protocol, or network)  

Firewalls can be:  
- **Hardware** → Dedicated appliances in big networks.  
- **Software** → On your PC, router, or cloud server.  
- **Combo units** → Your home router likely does both.

### Stateful vs Stateless  
| Type        | How It Works                                                   | Pros & Cons                                 |
|-------------|---------------------------------------------------------------|--------------------------------------------|
| **Stateful**| Looks at the *entire connection*, not just one packet.         | Smarter but uses more resources.            |
| **Stateless**| Judges each packet individually against static rules.         | Faster, simpler, but dumber.                |

If stateful firewalls are detectives solving whole crimes, stateless firewalls are mall cops checking one shopper at a time.

---

## VPNs: Building Secret Tunnels 🕵️‍♂️  

A **Virtual Private Network (VPN)** creates an encrypted “tunnel” over the public internet. Everything inside is private, like whispering secrets in a crowded room.

**Benefits:**  
- **Connect offices** across cities as if they were one network.  
- **Encrypt traffic** on sketchy coffee shop Wi-Fi.  
- **Add anonymity** (though VPN providers can still log traffic).  
- **Security bonus:** Services like TryHackMe use VPNs so their vulnerable labs aren’t exposed to the whole internet.

**Technologies:**  
- **PPTP:** Easy but weak encryption.  
- **IPSec:** Strong encryption, harder setup.  
- **PPP:** The authentication & encryption base for others.

---

## Routers: The Air Traffic Controllers  

Routers decide **where** your data goes. Multiple paths? They’ll pick:  
- The **shortest** route.  
- The **fastest** route.  
- The **most reliable** route.  

Routers live at **Layer 3** of the OSI model (the Network Layer) and handle:  
- Port forwarding  
- Firewall rules  
- Network address translation (NAT)

Think of them as air traffic control for your network’s data planes.

---

## Switches: The Matchmakers of Local Networks  

A **switch** connects multiple devices inside the same network. They come in two flavours:  

| Switch Type    | What It Does                                              |
|----------------|-----------------------------------------------------------|
| **Layer 2**     | Moves data based on MAC addresses (local traffic).        |
| **Layer 3**     | Adds IP routing — like a router and switch had a baby.    |

Modern switches can use **VLANs (Virtual LANs)** to segment traffic — like VIP areas in a club sharing the same dance floor but with velvet ropes between them.

> **Do switches need Ethernet cables?**  
Mostly, yes — traditional switches use Ethernet. But there are **wireless access points** that handle switching duties for Wi-Fi networks, so it doesn’t always mean cables everywhere.

---

## Putting It All Together  

- **Port Forwarding:** Opens the door.  
- **Firewall:** Decides who walks in or out.  
- **VPN:** Builds a private, encrypted tunnel.  
- **Router:** Finds the best path between networks.  
- **Switch:** Connects local devices and keeps them organised.

Extending your network isn’t just about more cables — it’s about using the right tools so your data knows *where to go*, *who to trust*, and *how to stay safe* along the way.