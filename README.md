<div align="center">

# 🔒 Cybersecurity Lab Environment Setup

**Building an isolated virtual lab for penetration testing and ethical hacking practice**

![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-C00000?style=for-the-badge)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-FF6B6B?style=for-the-badge)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-4CAF50?style=for-the-badge)
![Phase 1](https://img.shields.io/badge/Phase%201-Complete-brightgreen?style=for-the-badge)

</div>

---

## 📋 Project Overview

Isolated virtualization lab for penetration-testing and ethical-hacking practice, built by following the NetworkWalks Academy *Cyber Lab Setup Guide v4.2*. This repository covers **Phase 1** — the Kali Linux attacker VM.

> 📝 **Note:** This lab is designed for educational purposes only. All machines run isolated from production networks.

**📄 Full documentation:** All detailed steps, settings, commands, and screenshots are in [`docs/Phase1_Kali_Setup_Record.pdf`](docs/Phase1_Kali_Setup_Record.pdf).

## 📺 Video Walkthrough

> **▶️ Watch Phase 1 Setup:** [View the complete video walkthrough on YouTube](https://youtu.be/a3cQ-Q7RzqU)
> 
> This video shows all 7 steps in real-time, including downloading software, creating the network, configuring the VM, and testing connectivity. Follow along as we build the lab from scratch.

---

## 💻 Lab Environment

| 🖥️ Component | Detail |
|-----------|--------|
| **Host** | ASUS VivoBook — Ryzen 7 5800HS, 16 GB RAM, Windows 11 |
| **Hypervisor** | Oracle VirtualBox 7.2.14 |
| **Guest OS** | Kali Linux 2026.2 (prebuilt VirtualBox image, amd64) |
| **VM Resources** | 4096 MB RAM · 2 vCPU · 128 MB video |

---

## 🌐 Network Configuration

| ⚙️ Setting | Value |
|---------|-------|
| **Type** | NAT Network (custom) — `NatNetwork` |
| **Subnet** | 10.0.0.0/24 |
| **DHCP** | ✅ Enabled |
| **Kali Static IP** | 10.0.0.2/24 |
| **Gateway / DNS** | 10.0.0.1 |

> ℹ️ **Info:** The NAT Network provides isolation while allowing internet access through the gateway.

---

## 🛠️ Setup Steps

1. **Install 7-Zip** — to extract the Kali `.7z` image.
2. **Install VirtualBox** — and set the default machine folder.
3. **Create the isolated NAT network** — `NatNetwork` on 10.0.0.0/24, DHCP enabled.
4. **Import & boot Kali** — verify SHA256, import the `.vbox`, tune resources, attach to the NAT network, change the default password.
5. **Configure the static IP** — 10.0.0.2/24, gateway/DNS 10.0.0.1; verify with a ping test.
6. **Take a snapshot** — save the Phase 1 baseline restore point.

---

## 📸 Visual Walkthrough

### Step 1: VirtualBox Installation

![VirtualBox About](https://raw.githubusercontent.com/abdullatif13-ab/networkwalks-B082-week1-Cybersecurity-lab-setup/main/screenshots/07-VBox.png)

*VirtualBox 7.2.14 successfully installed.*

---

### Step 2: Create NAT Network

![NAT Network](https://raw.githubusercontent.com/abdullatif13-ab/networkwalks-B082-week1-Cybersecurity-lab-setup/main/screenshots/01-natnetwork.png)

*VirtualBox → Network → NAT Networks: NatNetwork on 10.0.0.0/24, DHCP enabled.*

---

### Step 3: Configure VM Network

![VM Network Adapter](https://raw.githubusercontent.com/abdullatif13-ab/networkwalks-B082-week1-Cybersecurity-lab-setup/main/screenshots/02-vm-adapter.png)

*Kali VM → Settings → Network: Adapter 1 attached to NAT Network "NatNetwork".*

---

### Step 4: Boot Kali Linux

![Kali Booted](https://raw.githubusercontent.com/abdullatif13-ab/networkwalks-B082-week1-Cybersecurity-lab-setup/main/screenshots/03-kali-uname.png)

*Kali 2026.2 booted successfully; uname confirms kernel 6.19.14+kali-amd64 (x86_64).*

---

### Step 5: Static IP Configuration

![IPv4 Configuration](https://raw.githubusercontent.com/abdullatif13-ab/networkwalks-B082-week1-Cybersecurity-lab-setup/main/screenshots/04-ip-config.png)

*Wired connection 1 → IPv4 Manual: address 10.0.0.2/24, gateway 10.0.0.1, DNS 10.0.0.1.*

> ⚠️ **Warning:** Ensure DNS is set to 10.0.0.1 (gateway) for proper name resolution in the lab environment.

---

### Step 6: Verify Connectivity

![Connectivity Test](https://raw.githubusercontent.com/abdullatif13-ab/networkwalks-B082-week1-Cybersecurity-lab-setup/main/screenshots/05-connectivity-ping.png)

*ifconfig shows eth0 = 10.0.0.2; ping google.com succeeds — static IP and DNS resolution working.*

---

### Step 7: Create Snapshot

![Snapshot](https://raw.githubusercontent.com/abdullatif13-ab/networkwalks-B082-week1-Cybersecurity-lab-setup/main/screenshots/06-snapshot.png)

*Snapshot "Kali 2026.2 — Phase 1 baseline (static 10.0.0.2)" saved as the clean restore point.*

> ✓ **Success:** Phase 1 is now complete with a clean baseline snapshot ready for Phase 2.

---

## 🎯 Skills Practiced

- ✓ Type-2 virtualization and VM resource tuning
- ✓ Linux networking — static IP, gateway, DNS, and connectivity troubleshooting
- ✓ Download integrity verification (SHA256)
- ✓ Snapshot / restore-point discipline
- ✓ Clear, reproducible technical documentation
- ✓ Network isolation and containment

---

## 🚀 Next: Phase 2

Add isolated victim machines (Windows 11/10/7, Android) on the same NAT network and practice reconnaissance and testing between hosts — entirely within the contained lab.

---

## ⚖️ Disclaimer

This lab is for **educational use only**. Every machine runs as a virtual machine isolated from production networks, and all activity is performed against systems I own inside this contained environment. Nothing here is intended for use against any system without explicit authorization.

---

*Lab based on the NetworkWalks Academy Cyber Lab Setup Guide v4.2.*

*Contact: info@networkwalks.com*
