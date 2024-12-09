# Matrix1 Walkthrough

This repository contains a step-by-step guide for completing the **Matrix1** challenge. The walkthrough covers network reconnaissance, password cracking, and exploiting services to retrieve the flag.

## Table of Contents
- [Introduction](#introduction)
- [Tools Used](#tools-used)
- [Step-by-Step Instructions](#step-by-step-instructions)
- [Features](#features)
- [Disclaimer](#disclaimer)

## Introduction

The **Matrix1** challenge is a practical exercise designed to enhance penetration testing skills. It involves:
1. Network discovery.
2. Service enumeration.
3. Password cracking and brute-forcing.
4. Retrieving the final flag.

This guide provides detailed steps to help users navigate through the challenge.

## Tools Used

- **Netdiscover**: Scans and discovers live hosts on a network using ARP requests.
- **Nmap**: Maps networks, scans for open ports, and identifies vulnerabilities.
- **Crunch**: Generates custom wordlists for password cracking.
- **Hydra**: Performs brute-force attacks on various protocols and services.
- **SSH (Secure Shell)**: Securely connects to remote systems.
- **Vi/Vim**: A powerful terminal-based text editor.

## Step-by-Step Instructions

### Step 1: Network Discovery
Use **Netdiscover** to identify live hosts within the network. It sends ARP requests and collects responses to identify devices.

### Step 2: Port Scanning
Run **Nmap** with the `-p-` option to scan all ports on the target IP address. Identify open ports and active services.

### Step 3: Accessing Services
1. Identify port `80` (HTTP).
2. Visit the target's IP address in Firefox.

### Step 4: Analyzing Web Pages
1. Inspect the page source code using "Inspect Element."
2. Extract the relevant information.

### Step 5: Decode Hidden Information
1. Use the `echo` command to manipulate and display text.
2. Navigate to [decode.fr](https://www.decode.fr/brainfuck-language) to decode the extracted text and retrieve the password.

### Step 6: Wordlist Generation
Use **Crunch** to generate a wordlist tailored for brute-forcing login credentials.

### Step 7: Brute-Force Login
Use **Hydra** to perform brute-force attacks on services like SSH and obtain valid credentials.

### Step 8: Access via SSH
Log in to the target system using SSH and the discovered credentials.

### Step 9: File Editing with Vi/Vim
Utilize Vi/Vim for:
- Editing configuration files.
- Executing shell commands directly within the editor.

### Step 10: Retrieve the Flag
1. Export the shell and path variables.
2. Navigate to the `/root` directory.
3. Retrieve the flag.

## Features

- **Comprehensive Reconnaissance**: Tools for discovering hosts and services.
- **Advanced Exploitation**: Decoding, brute-forcing, and accessing secure systems.
- **Custom Wordlist Generation**: Tailored password cracking.
- **Practical Learning**: Hands-on exposure to penetration testing techniques.

## Disclaimer

This guide is intended for educational purposes and ethical hacking only. Unauthorized use of these techniques is illegal and unethical. Always perform penetration testing with proper authorization.

---

Feel free to fork, contribute, or raise issues to enhance this repository!
