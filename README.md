# A+ Core 2 Linux Labs

This repository documents my hands-on Linux VM labs and troubleshooting exercises in Hyper-V.  
I am using Ubuntu 24.04.3 LTS to practice the Linux objectives for the CompTIA A+ 220-1202 exam. 
The core focus of this repository is to practice and demonstrate a working knowledge of the common features and tools of the Linux client/desktop operating system 

---

## Environment
- **Host OS:** Windows 10 Pro, Hyper-V enabled
- **Hardware:** Intel i7-6700K, 16 GB DDR4 RAM, 1 TB SSD, ASUS ROG Maximus VIII Hero motherboard
- **VM OS:** Ubuntu 24.04.3 LTS
- **VM Specs:** 8 GB RAM, 60 GB dynamically expanding disk, Generation 2 (UEFI)

---

## Setup & Troubleshooting Summary
- Enabled virtualization in BIOS (Intel VT-x)
- Turned on Hyper-V in Windows Features
- Created a Generation 2 VM with 8 GB RAM and 60 GB disk
- Attached Ubuntu ISO to DVD drive
- Fixed PXE boot error by changing boot order
- Disabled Secure Boot to allow Ubuntu installer
- Installed Ubuntu successfully
- Changed boot order to boot from hard disk first
- Removed ISO file after installation
- Installed Hyper-V integration tools to reduce mouse lag
- Enabled Enhanced Session Mode for smoother input

---

## Learning Objectives
This repo aligns with the Linux-related objectives of the CompTIA A+ 220-1202 exam:
- Demonstrate Linux file system navigation (`ls`, `cd`, `pwd`, `mv`, `cp`, `rm`, `chmod`, `chown`, `grep`, `find`)
- Manage users, groups, and permissions (`chmod`, `chown`, `passwd`)
- Configure and troubleshoot services (`systemctl`, `journalctl`)
- Apply networking commands (`ip`, `ping`, `curl`, `ufw`)
- Document troubleshooting steps clearly and professionally

---

## Repository Structure
- `setup/` → VM and environment setup notes  
- `labs/` → Hands-on exercises by topic  
- `troubleshooting/` → Case studies of real issues and fixes  
- `snapshots/` → Notes on checkpoints and rollback testing  

---

## Usage
Clone the repository and browse the Markdown files:

```bash
git clone https://github.com/yourusername/aplus1202-linux-labs.git
cd aplus1202-linux-labs

