# Step-by-Step Guide: Kali Linux Installation on VirtualBox

This repository provides a detailed guide to installing **Kali Linux** on **VirtualBox**. Kali Linux is a powerful tool for ethical hacking and penetration testing, and VirtualBox enables you to create a safe and isolated environment to run it.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Requirements](#requirements)
3. [Installation Steps](#installation-steps)
4. [Troubleshooting](#troubleshooting)
5. [Contributing](#contributing)
6. [License](#license)

---

## Introduction

This guide is designed to help beginners and professionals alike to set up Kali Linux on VirtualBox. Whether you're a cybersecurity enthusiast or a student, this guide provides clear, step-by-step instructions.

---

## Requirements

Before starting, ensure you have the following:

- A system with **VirtualBox** installed (download it from [VirtualBox](https://www.virtualbox.org/)).
- Kali Linux ISO file (download it from [Kali Linux Official Website](https://www.kali.org/)).
- Minimum hardware requirements:
  - 4GB of RAM (8GB recommended)
  - 20GB of free disk space

---

## Installation Steps

### 1. Download Required Software
- Download and install **VirtualBox** on your system.
- Download the latest version of the **Kali Linux ISO file**.

### 2. Create a New Virtual Machine
- Open VirtualBox and click on **"New"**.
- Enter the name (e.g., "Kali Linux") and select:
  - Type: **Linux**
  - Version: **Debian 64-bit**
- Allocate at least **2GB of RAM** (4GB recommended).

### 3. Configure Virtual Hard Disk
- Choose **Create a virtual hard disk now**.
- Select **VDI (VirtualBox Disk Image)** and **Dynamically Allocated**.
- Set the disk size to **20GB or more**.

### 4. Attach Kali Linux ISO
- Select your virtual machine and click **Settings**.
- Go to the **Storage** tab.
- Under **Controller: IDE**, click on the empty disk icon and choose **Add Optical Drive**.
- Select the downloaded **Kali Linux ISO** file.

### 5. Start the Virtual Machine
- Start the virtual machine by clicking **Start**.
- Follow the on-screen instructions:
  - Select **Graphical Install**.
  - Configure your language, region, and keyboard.
  - Set up a username and password.
  - Partition the disk (choose **Guided – Use entire disk**).
  - Wait for the installation to complete.

### 6. Install VirtualBox Guest Additions (Optional but Recommended)
- Insert the Guest Additions ISO from the VirtualBox menu.
- Mount the ISO in Kali Linux and run the installation script:
  ```bash
  sudo apt update
  sudo apt install -y build-essential linux-headers-$(uname -r)
  cd /media/cdrom
  sudo ./VBoxLinuxAdditions.run
