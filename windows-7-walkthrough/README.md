# Windows 7 Exploitation Walkthrough

This repository provides a detailed walkthrough of exploiting a Windows 7 system using tools like **Netdiscover**, **Nmap**, and **Searchsploit**, and leveraging the EternalBlue vulnerability to gain access.

## Table of Contents
- [Introduction](#introduction)
- [Tools Used](#tools-used)
- [Exploitation Steps](#exploitation-steps)
- [Important Links](#important-links)
- [Disclaimer](#disclaimer)

## Introduction

This guide demonstrates a penetration testing scenario where a Windows 7 system is exploited using EternalBlue. The walkthrough includes:
1. Network reconnaissance.
2. Vulnerability identification.
3. Exploitation using a payload to gain shell access.

This material is intended for ethical hacking and cybersecurity training purposes only.

## Tools Used

- **Netdiscover**: A network reconnaissance tool to identify devices in a network.
- **Nmap**: A network scanning tool to discover hosts, services, and vulnerabilities.
- **Searchsploit**: A tool for searching exploits in the Exploit-DB database.
- **Metasploit Framework**: A widely used framework for developing and executing exploit code.

## Exploitation Steps

### Step 1: Network Discovery
Use **Netdiscover** to identify devices on the network, especially useful in non-DHCP environments.

### Step 2: Network Scanning
Run **Nmap** to scan for open ports and services. This helps identify vulnerabilities in the target system.

### Step 3: Identifying Vulnerabilities
Search for the EternalBlue exploit using a browser or **Searchsploit**:
- EternalBlue is an SMB exploit targeting Windows kernel vulnerabilities.

### Step 4: Preparing the Exploit
1. Use **Searchsploit** to locate EternalBlue in the Exploit-DB database.
2. Note down the exploit details and proceed.

### Step 5: Setting Up the Exploit
1. Open Metasploit and load the EternalBlue exploit.
2. Set the required parameters:
   - `RHOSTS`: The target's IP address.
   - `LHOST`: The attacker's IP address.

### Step 6: Configure the Payload
1. Display available payloads using the `show payloads` command.
2. Select `generic/shell_reverse_tcp` for a reverse shell.

### Step 7: Exploit the Target
Run the exploit to execute the payload and gain access to the target system.

### Step 8: Gaining a Shell
Once the exploit is successful, use the Meterpreter shell to interact with the target system.

## Important Links
- [Exploit-DB](https://www.exploit-db.com): A repository of exploits and vulnerable software.
- [Metasploit Framework](https://www.metasploit.com): Official Metasploit website.

## Disclaimer

This guide is intended for educational purposes and authorized testing only. Unauthorized access to systems or networks is illegal and unethical. Always obtain proper permissions before conducting penetration tests.

---

Feel free to contribute or raise issues in this repository!
