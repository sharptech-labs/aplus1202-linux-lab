# A+ Core 2 Linux Lab

This repository documents my hands-on Linux VM lab

I am using Ubuntu 24.04.3 LTS 

The core focus of this repository is to practice and demonstrate a working knowledge of the common features and tools of the Linux client/desktop operating system

I have documentented how to set up a Linux VM in Hyper-V, some troubleshooting you may run into, as well as my notes and observations while doing excersices regarding the objectives for the CompTIA A+ 220-1202 exam

You can follow along with my steps to set this lab up on your computer and learn the objectives for the exam

---

## Environment
- **Host OS:** Windows 10 Pro, Hyper-V enabled
- **Hardware:** Intel i7-6700K, 16 GB DDR4 RAM, 1 TB SSD, ASUS ROG Maximus VIII Hero motherboard
- **VM OS:** Ubuntu 24.04.3 LTS
- **VM Specs:** 8 GB RAM, 60 GB dynamically expanding disk, Generation 2 (UEFI)

---



## Learning Objectives (CompTIA A+ 220-1202 Objective 1.9 — Linux Client/Desktop)

This repo aligns with CompTIA A+ 220-1202 Objective 1.9 — Identify common features and tools of the Linux client/desktop OS

### File Management
- `ls` → List directory contents
- `pwd` → Show current working directory
- `mv` → Move files
- `cp` → Copy files
- `rm` → Remove files
- `chmod` → Change file permissions
- `chown` → Change file ownership
- `grep` → Search text patterns
- `find` → Search for files

### Filesystem Management
- `fsck` → Verify and repair filesystems
- `mount` → Mount and unmount storage devices

### Administrative
- `su` → Switch users
- `sudo` → Run commands with elevated privileges

### Package Management
- `apt` → Manage packages on Debian/Ubuntu
- `dnf` → Manage packages on Fedora/Red Hat

### Networking
- `ip` → Display and configure IP addresses
- `ping` → Test connectivity
- `curl` → Transfer data from/to a server
- `dig` → Query DNS records
- `traceroute` → Trace network paths

### Informational Commands
- `man` → Access manual pages
- `cat` → Display file contents
- `top` → Monitor system performance
- `ps` → View running processes
- `du` → Show disk usage by directory
- `df` → Show disk usage by filesystem

### Text Editing
- `nano` → Lightweight text editor

### Common Configuration Files
- `/etc/passwd` → User account information
- `/etc/shadow` → Encrypted passwords
- `/etc/hosts` → Local hostname resolution
- `/etc/fstab` → Filesystem mount points
- `/etc/resolv.conf` → DNS resolver configuration

### OS Components
- `systemd` → Service and process manager
- `kernel` → Core of the operating system
- `bootloader` → Loads the OS at startup

### Root Account
- Understand the purpose and risks of the root account
- Practice safe use of root privileges

---

## Repository Structure
- `setup/` → VM and environment setup notes  
- `labs/` → Command-focused exercises by topic  
- `troubleshooting/` → Case studies of real issues and fixes  
 
---

## Usage
Clone the repository and browse the Markdown files:

```bash
git clone https://github.com/sharptech-labs/aplus1202-linux-lab.git
cd aplus1202-linux-labs
