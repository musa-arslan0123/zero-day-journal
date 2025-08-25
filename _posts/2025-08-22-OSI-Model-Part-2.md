---
title: "Networking Notes: OSI Model (Part 2)"
date: 2025-08-20 12:30:00 +0800
tags: [Networks, Try-Hack-Me]
categories: [journal, OSI-Model]
---

# Networking Notes: OSI Model (Layers 6 & 7)

Continuing with the OSI model, these are the top two layers where **user interaction** and **data translation** happen.

---

## Presentation Layer (Layer 6)

- **Purpose:**  
  Standardises how data is presented across different systems.  
- **Translation:**  
  Converts data into a common format so that the receiving system understands it, even if it uses different software.  
- **Example:**  
  When you send an email from one client, the recipient might use a completely different email program — the presentation layer ensures the content still displays correctly.  
- **Security:**  
  Data encryption (e.g., **HTTPS**) and sometimes compression happen here.  
- **Key Role:**  
  Acts as a translator and formatter between the application layer and the lower layers.

---

## Application Layer (Layer 7)

- **Purpose:**  
  Provides the interface between the **end user** and the network.  
- **Protocols & Services:**  
  - **HTTP/HTTPS** → Web browsing  
  - **SMTP/IMAP/POP3** → Email  
  - **DNS** → Resolving domain names to IP addresses  
  - **FTP** → File transfers  
- **User Interaction:**  
  Email clients, browsers, file transfer apps (e.g., FileZilla) all operate here with GUIs for user-friendly access.  
- **Key Role:**  
  Determines how user applications communicate with network services.

---

## Summary of Layers 6 & 7
- **Layer 6 (Presentation):** Data translation, formatting, encryption.  
- **Layer 7 (Application):** End-user applications, protocols, and services.  

With this, all **seven OSI layers** have been covered across your posts.

---