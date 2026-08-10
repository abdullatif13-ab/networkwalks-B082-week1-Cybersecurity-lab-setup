NetworkWalks — Week 1: Cybersecurity Lab Setup

Isolated virtualization lab for penetration-testing and ethical-hacking practice, built by following the NetworkWalks Academy Cyber Lab Setup Guide v4.2. This repository covers Phase 1 — the Kali Linux attacker VM.

Status: Phase 1 complete ✅ · Phase 2 (victim machines) next.

📄 Full documentation — every setting, command, and screenshot: docs/Phase1_Kali_Setup_Record.pdf

Lab environment
Component	Detail
Host	ASUS VivoBook — Ryzen 7 5800HS, 16 GB RAM, Windows 11
Hypervisor	Oracle VirtualBox
Guest OS	Kali Linux 2026.2 (prebuilt VirtualBox image, amd64)
VM resources	4096 MB RAM · 2 vCPU · 128 MB video
Network design
Setting	Value
Type	NAT Network (custom), NatNetwork
Subnet	10.0.0.0/24
Kali (static)	10.0.0.2/24
Gateway / DNS	10.0.0.1
Step 1 — Install 7-Zip

Installed to extract the Kali .7z image.

Step 2 — Install VirtualBox

Installed Oracle VirtualBox and set the default machine folder.

Step 3 — Create the isolated NAT network

Created a custom NAT network NatNetwork on 10.0.0.0/24 with DHCP enabled.

Step 4 — Import & boot Kali

Verified the image's SHA256, extracted and imported the .vbox, tuned resources to the host, attached Adapter 1 to the NAT network, then booted and changed the default password.

Step 5 — Configure the static IP

Set a Manual IPv4 config (10.0.0.2/24, gateway/DNS 10.0.0.1) and verified connectivity with ping google.com.

Step 6 — Take a snapshot

Saved "Kali 2026.2 — Phase 1 baseline (static 10.0.0.2)" as a clean restore point.

📄 See the full PDF write-up for the detailed steps and screenshots.

Skills practiced
Type-2 virtualization and VM resource tuning
Linux networking — static IP, gateway, DNS, and connectivity troubleshooting
Download integrity verification (SHA256)
Snapshot / restore-point discipline
Clear, reproducible technical documentation
Next: Phase 2

Add isolated victim machines (Windows 11/10/7, Android) on the same NAT network and practice reconnaissance and testing between hosts — entirely within the contained lab.
