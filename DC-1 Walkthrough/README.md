# 🛡️ Dc-1 Walkthrough

This repository provides a comprehensive walkthrough of the **Dc-1** Capture the Flag (CTF) challenge. It covers techniques for network reconnaissance, vulnerability exploitation, and privilege escalation to successfully complete the challenge.

## 📋 Table of Contents
- [🔍 Introduction](#-introduction)
- [🛠️ Tools Used](#️-tools-used)
- [🗺️ Walkthrough Steps](#-walkthrough-steps)
- [⚠️ Disclaimer](#️-disclaimer)

## 🔍 Introduction

The **Dc-1** CTF is designed for beginners and intermediate penetration testers. This guide will teach you how to:
1. Perform network discovery.
2. Identify and exploit vulnerabilities.
3. Gain shell access and escalate privileges to root.

This walkthrough is for educational purposes, helping you enhance your cybersecurity skills.

## 🛠️ Tools Used

- 🕵️‍♂️ **Netdiscover**: Identifies active hosts in the network using ARP requests.
- 🌐 **Nmap**: Scans for open ports, services, and vulnerabilities on the target system.
- 📚 **SearchSploit**: Finds publicly available exploits in the Exploit Database.
- 💉 **Metasploit Framework (msfconsole)**: Executes exploits and manages payloads for penetration testing.

## 🗺️ Walkthrough Steps

### Step 1: Network Discovery with Netdiscover
Use **Netdiscover** to identify live systems in the subnet by sending ARP requests.

### Step 2: Port Scanning with Nmap
Run **Nmap** to scan for open ports, services, and vulnerabilities on the target system.

### Step 3: Finding Exploits with SearchSploit
Leverage **SearchSploit** to locate publicly available exploits for the identified vulnerabilities.

### Step 4: Setting Up Exploits with Metasploit
1. Open **msfconsole** and load the desired exploit.
2. Configure the following options:
   - `RHOSTS`: Target IP address.
   - `LHOST`: Attacker IP address.

### Step 5: Execute the Exploit
Run the exploit to gain initial access to the target system.

### Step 6: Gaining Shell Access
Use a Python script to spawn a shell. Employ commands like:
- `find` to check file permissions (`2>/dev/null` to suppress errors).
- `touch` to create files or directories for testing.

### Step 7: Privilege Escalation
1. Create and execute a file for privilege escalation.
2. Use `/bin/bash` to execute commands as root.
3. Successfully gain root access and retrieve the flag.

## ⚠️ Disclaimer

This walkthrough is strictly for **educational purposes only**. Unauthorized use of these techniques is illegal and unethical. Always obtain proper authorization before conducting penetration tests.

---

🌟 **Pro Tip**: If you find this helpful, consider starring this repository and contributing to the cybersecurity community!
