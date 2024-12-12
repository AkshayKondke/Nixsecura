# 🛡️ Hackaton Walkthrough

This repository contains a comprehensive walkthrough for solving the **Hackaton** Capture the Flag (CTF) challenge. It includes network reconnaissance, vulnerability exploitation, and privilege escalation techniques to successfully complete the challenge.

## 📋 Table of Contents
- [🔍 Introduction](#-introduction)
- [🛠️ Tools Used](#️-tools-used)
- [🗺️ Walkthrough Steps](#-walkthrough-steps)
- [⚠️ Disclaimer](#️-disclaimer)

## 🔍 Introduction

The **Hackaton** CTF challenge tests your penetration testing skills in discovering vulnerabilities, accessing systems, and escalating privileges to achieve root access. This guide covers:
1. Network reconnaissance.
2. Vulnerability exploitation.
3. Secure shell access.
4. Privilege escalation to root.

This walkthrough is designed for educational purposes to enhance practical cybersecurity knowledge.

## 🛠️ Tools Used

- 🕵️‍♂️ **Netdiscover**: Identifies live hosts on a network using ARP requests.
- 🌐 **Nmap**: Performs full port scans, service detection, and vulnerability assessments.
- 🛡️ **Gobuster**: Brute-forces URLs, directories, and DNS subdomains to discover hidden resources.
- 🔐 **Hydra**: Performs password brute-forcing on various protocols and services.
- 🖥️ **Vi/Vim**: A terminal-based text editor used for creating and editing files, as well as executing shell commands.

## 🗺️ Walkthrough Steps

### Step 1: Network Discovery with Netdiscover
- Use **Netdiscover** to identify live systems in the subnet by sending ARP requests.

### Step 2: Network Scanning with Nmap
- Perform a full port scan with `nmap -p-` to detect open ports and running services.

### Step 3: Accessing FTP
- Login to the open FTP server using `anonymous` credentials.
- Retrieve the file `Word.dir` from the server.

### Step 4: Directory Brute-Forcing with Gobuster
- Use **Gobuster** to find hidden directories on the target web server.
- Navigate to the `/happy` directory for further clues.

### Step 5: Analyzing the Web Page
- Inspect the `/happy` web page source code to find the username.

### Step 6: Password Brute-Forcing with Hydra
- Use **Hydra** to brute-force the password for the identified username.

### Step 7: SSH Login
- Login to the target system using SSH with the discovered credentials and specified port.

### Step 8: Editing Files with Vi/Vim
- Launch **Vi** to edit files or execute shell commands directly from the terminal.

### Step 9: Privilege Escalation with Vim
- Execute the command `sudo vim -c ':!/bin/sh'` to escalate privileges and gain root access.

## ⚠️ Disclaimer

This walkthrough is strictly for **educational purposes only**. Unauthorized use of these techniques is illegal and unethical. Always obtain proper authorization before conducting penetration tests.

---

🌟 **Pro Tip**: If you find this helpful, give the repository a ⭐ and contribute to the community by sharing your knowledge!
