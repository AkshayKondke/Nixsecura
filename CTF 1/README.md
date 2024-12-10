# CTF1 Walkthrough

This repository provides a detailed walkthrough of the **CTF1** challenge. It includes the tools and steps required to identify vulnerabilities, exploit services, and retrieve critical information. The walkthrough is aimed at beginners and intermediate penetration testers.

## Table of Contents
- [Introduction](#introduction)
- [Tools Used](#tools-used)
- [Step-by-Step Instructions](#step-by-step-instructions)
- [Features](#features)
- [Disclaimer](#disclaimer)

## Introduction

The **CTF1** challenge is designed to test and enhance your penetration testing skills. It involves:
1. Network reconnaissance.
2. Vulnerability identification.
3. Exploitation of services.
4. Gathering key information for challenge completion.

This guide provides a step-by-step approach to solving the challenge while using industry-standard tools.

## Tools Used

- **Nmap**: For network scanning and vulnerability assessment.
- **Netdiscover**: For identifying live hosts on the network.
- **Nikto**: For scanning web servers for vulnerabilities.
- **Gobuster**: For brute-forcing directories and files.
- **Hydra**: For password cracking and brute-forcing login credentials.
- **SSH (Secure Shell)**: For securely accessing remote servers.

## Step-by-Step Instructions

### Step 1: Network Scanning with Nmap
Run **Nmap** to discover live hosts, open ports, and services. Analyze the results to identify potential vulnerabilities.

### Step 2: Host Discovery with Netdiscover
Use **Netdiscover** to map out the network and find live hosts.

### Step 3: Web Server Scanning with Nikto
Scan the target's web server using **Nikto** to identify vulnerabilities and configurations.

### Step 4: Analyze robots.txt
1. Open the target in Firefox.
2. Check the `robots.txt` file for sensitive information.
3. Copy the text for further analysis.

### Step 5: Directory Brute-Forcing with Gobuster
Run **Gobuster** to find hidden directories or files on the web server. For example, locate `sudo.html`.

### Step 6: Source Code Analysis
1. Open the identified HTML file in a browser.
2. Inspect the page source to find sensitive information (e.g., credentials or usernames).

### Step 7: Brute-Force Login with Hydra
Use **Hydra** to perform a brute-force attack on login credentials.

### Step 8: Secure Access via SSH
Log in to the target system using the discovered credentials with **SSH**.

## Features

- **Network Reconnaissance**: Tools for discovering hosts and mapping services.
- **Web Vulnerability Scanning**: Identify misconfigurations and security flaws in web servers.
- **Brute-Forcing Capabilities**: Access restricted areas using powerful tools.
- **Hands-On Learning**: Practical exposure to penetration testing techniques.

## Disclaimer

This walkthrough is intended for educational purposes and ethical hacking only. Unauthorized access or testing without explicit permission is illegal and unethical. Always adhere to applicable laws and obtain authorization before conducting any penetration tests.

---

Feel free to fork this repository, contribute improvements, or raise issues!
