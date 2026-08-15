---
title: "Building My Offensive Linux Lab: Setting Up from Scratch for Bug Bounty"
date: 2026-08-15
draft: false
tags: ["Bug Bounty", "Linux", "VirtualBox", "Cybersecurity", "Recon"]
---

Welcome back to the journey. In my previous update, I laid out the foundation. Now, it's time to get hands-on and build the actual ecosystem where all the hacking, enumeration, and bug hunting will take place. 

If you are starting from absolute zero like I am, you don’t need an expensive rig or complex cloud setups to start learning offensive security. All you need is a hypervisor, a solid Linux distribution, and the right mindset.

Here is how I set up my first local Linux lab using **VirtualBox** and the essential tools I am deploying to kick off my Bug Bounty journey.

---

## 1. The Hypervisor & OS Choice

For this lab, I went with **VirtualBox** running **Kali Linux**. While you can use Parrot OS or even a minimal Ubuntu/Debian setup and install tools manually, Kali provides a robust, pre-configured environment tailored for penetration testing and bug hunting.

* **RAM Allocated:** 4 GB
* **CPU Cores:** 2
* **Network Mode:** Bridged Adapter (to simulate a real external interaction with target networks when needed).

---

## 2. Essential Tools Deployed in the Lab

A hacker is only as good as their toolset—and more importantly, knowing *how* and *when* to use them. Here are the core tools I am deploying right out of the box:

### 🌐 Interception & Web Testing
* **Burp Suite Community Edition:** The absolute standard for web application security testing. It allows me to intercept, inspect, modify, and replay HTTP/HTTPS requests heading to target applications. Essential for finding logic flaws, XSS, and IDORs.

### 🔍 Network Reconnaissance
* **Nmap:** The king of network mapping. Used for host discovery, port scanning, and service version detection to spot potential entry points or misconfigured services.

### 📂 Content Discovery & Fuzzing
* **ffuf (Fuzz Faster U Fool):** A blazing-fast tool written in Go used for discovering hidden directories, files, and virtual hosts on web servers. 
* **Gobuster:** Another fantastic alternative for brute-forcing URIs and DNS subdomains.

### 🕵️ Subdomain Enumeration (Recon Phase)
* **Sublist3r / Amass:** Critical for gathering as many subdomains as possible during the initial reconnaissance phase of a Bug Bounty target, expanding the attack surface.

---

## What's Next?

With the lab up and running and the toolchain locked in, the next step is putting theory into practice. I will be diving into my very first target environments—testing out web vulnerabilities on lab platforms and mapping out a repeatable workflow for live bug hunting.

Stay tuned, and happy hacking!