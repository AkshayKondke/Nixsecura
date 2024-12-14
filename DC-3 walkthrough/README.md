# 🛡️ Dc-3 Walkthrough

This repository contains a detailed walkthrough of the **Dc-3** Capture the Flag (CTF) challenge. It covers network reconnaissance, exploiting a Joomla CMS vulnerability, privilege escalation, and achieving root access on the target machine.

## 📋 Table of Contents
- [🔍 Introduction](#-introduction)
- [🛠️ Tools Used](#️-tools-used)
- [🗺️ Walkthrough Steps](#-walkthrough-steps)
- [⚠️ Disclaimer](#️-disclaimer)

## 🔍 Introduction

The **Dc-3** challenge is designed to test your penetration testing and ethical hacking skills. This walkthrough demonstrates:
1. Discovering active hosts and open ports.
2. Exploiting vulnerabilities in Joomla CMS.
3. Using reverse shells for remote access.
4. Escalating privileges to root using publicly available exploits.

This guide is intended for educational purposes to enhance practical cybersecurity skills.

## 🛠️ Tools Used

- 🕵️‍♂️ **Netdiscover**: Identifies live hosts in a network using ARP requests.
- 🌐 **Nmap**: Performs full port scans, service detection, and vulnerability assessments.
- 📚 **SearchSploit**: Searches for publicly available exploits in the Exploit Database.
- 🛡️ **Nmap Scripts (NSE)**: Automates tasks like banner grabbing and vulnerability scanning.
- 🐚 **Netcat (NC)**: Used for setting up reverse shells and networking tasks.
- 🖥️ **PHP Reverse Shell**: Retrieves access through injected PHP scripts.

## 🗺️ Walkthrough Steps

### Step 1: Network Discovery with Netdiscover
Use **Netdiscover** to identify live systems on the network using ARP requests.

### Step 2: Port Scanning with Nmap
Run **Nmap** to:
- Identify open ports, such as port 80.
- Detect services and vulnerabilities.

### Step 3: CMS Identification
Visit the web page on port 80 and use **Wappalyzer** to detect that the target is running Joomla CMS.

### Step 4: Search for Exploits
Use **SearchSploit** to find Joomla CMS-related vulnerabilities in the Exploit Database.

### Step 5: Log In to the Admin Page
Use the discovered credentials to access the Joomla admin page and view templates.

### Step 6: Reverse Shell Injection
1. Download a **PHP Reverse Shell** from [pentestmonkey](https://github.com/pentestmonkey/php-reverse-shell).
2. Modify the reverse shell script with your `LHOST` (listening IP) and port (e.g., 5555).
3. Inject the modified PHP shell into a template, such as the `error.php` file.
4. Save the template and preview it to execute the shell.

### Step 7: Gain Shell Access
Use **Netcat** to listen on the configured port and connect to the target system when the reverse shell executes.

### Step 8: Determine System Details
Run `lsb_release` to identify the OS version and look for relevant exploits.

### Step 9: Exploit the Target
1. Find an exploit for the detected system version in the Exploit Database.
2. Use `wget` to download the exploit to the `/tmp` directory on the target system.
3. Extract the exploit archive using the `tar` command.

### Step 10: Execute the Exploit
1. Compile and execute the exploit using `./compile.sh` or similar commands.
2. Achieve root access and retrieve the flag.

## ⚠️ Disclaimer

This walkthrough is strictly for **educational purposes only**. Unauthorized use of these techniques is illegal and unethical. Always obtain explicit permission before conducting penetration tests.

---

🌟 **Pro Tip**: If you find this helpful, consider starring this repository and contributing to the cybersecurity community!
