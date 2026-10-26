# 🛡️ Penetration Testing & Cybersecurity Lab Reports Repository

[![Platform: TryHackMe](https://img.shields.io/badge/Platform-TryHackMe-red.svg)](https://tryhackme.com)
[![Platform: VulnHub](https://img.shields.io/badge/Platform-VulnHub-blue.svg)](https://www.vulnhub.com)
[![Platform: OverTheWire](https://img.shields.io/badge/Platform-OverTheWire-green.svg)](https://overthewire.org)
[![Documentation: Bilingual](https://img.shields.io/badge/Docs-English%20%7C%20العربية-orange.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[📖 قراءة الدليل الرئيسي بالعربية](README_AR.md) | [English Version](README.md)

---

## 📌 About This Repository

Welcome to the **Penetration Testing & Red Teaming Assessment Reports Repository**. This repository serves as a centralized, high-quality reference and portfolio documenting real-world vulnerability assessments, Capture The Flag (CTF) challenges, and offensive security methodologies across **Linux**, **Windows**, and **Network Pivoting** environments.

Every lab report is documented with:
* **Executive Summaries & Attack Graphs (`Mermaid`)**
* **Vulnerability Details (CVEs, Severity & CVSS)**
* **Step-by-step Exploitation Commands & Proof-of-Concept (PoC)**
* **Privilege Escalation Mechanics & Root Cause Explanations**
* **Defensive Hardening & Remediation Guidance (Blue Team / SysAdmin)**
* **Dual-Language Documentation:** Complete English (`README.md`) and Arabic (`README_AR.md`) reports.

---

## 🗂️ Complete Lab Matrix

| Machine / Lab | Platform | Target OS | Difficulty | Core Vectors & CVEs | English | العربية |
| :--- | :---: | :---: | :---: | :--- | :---: | :---: |
| **[HackPark](TryHackMe%20(THM)/HackPark)** | TryHackMe | Windows | Medium | BlogEngine.NET RCE (`CVE-2019-6714`), Scheduled Task `Message.exe` | [EN](TryHackMe%20(THM)/HackPark/README.md) | [AR](TryHackMe%20(THM)/HackPark/README_AR.md) |
| **[Internal](TryHackMe%20(THM)/Internal)** | TryHackMe | Linux | Hard | WordPress 404.php Shell, Docker Pivoting, Jenkins Groovy RCE | [EN](TryHackMe%20(THM)/Internal/README.md) | [AR](TryHackMe%20(THM)/Internal/README_AR.md) |
| **[Overpass 2: Hacked](TryHackMe%20(THM)/Overpass2_Hacked)** | TryHackMe | Linux | Medium | PCAP Forensics (Wireshark), Hash Cracking, Go Backdoor Reversing, SUID | [EN](TryHackMe%20(THM)/Overpass2_Hacked/README.md) | [AR](TryHackMe%20(THM)/Overpass2_Hacked/README_AR.md) |
| **[Relevant](TryHackMe%20(THM)/Relevant)** | TryHackMe | Windows | Medium | Writable Anonymous SMB Share, IIS Web Mapping, PrintSpoofer Token Impersonation | [EN](TryHackMe%20(THM)/Relevant/README.md) | [AR](TryHackMe%20(THM)/Relevant/README_AR.md) |
| **[VulnNet: DotPy](TryHackMe%20(THM)/VulnNet_DotPy)** | TryHackMe | Linux | Medium | Werkzeug Flask SSTI (Jinja2), Sudo `pip3 install`, Module Hijacking | [EN](TryHackMe%20(THM)/VulnNet_DotPy/README.md) | [AR](TryHackMe%20(THM)/VulnNet_DotPy/README_AR.md) |
| **[Wreath](TryHackMe%20(THM)/Wreath)** | TryHackMe | Multi-Host | Hard | Multi-hop Chisel Pivoting, Webmin RCE (`CVE-2019-15107`), GitStack, Mimikatz | [EN](TryHackMe%20(THM)/Wreath/README.md) | [AR](TryHackMe%20(THM)/Wreath/README_AR.md) |
| **[Basic Pentesting 1](VulnHub%20VMs/Basic_Pentesting_1)** | VulnHub | Linux | Easy | ProFTPD 1.3.5 mod_copy RCE (`CVE-2015-3306`), WordPress | [EN](VulnHub%20VMs/Basic_Pentesting_1/README.md) | [AR](VulnHub%20VMs/Basic_Pentesting_1/README_AR.md) |
| **[Basic Pentesting 2](VulnHub%20VMs/Basic_Pentesting_2)** | VulnHub | Linux | Easy | SMB User Enum, SSH Password Cracking, World-Readable `id_rsa`, Sudo `ALL` | [EN](VulnHub%20VMs/Basic_Pentesting_2/README.md) | [AR](VulnHub%20VMs/Basic_Pentesting_2/README_AR.md) |
| **[Hackable III](VulnHub%20VMs/Hackable_III)** | VulnHub | Linux | Medium | Port Knocking Sequences, SSH Brute-Forcing, SUID / Cronjob Escalation | [EN](VulnHub%20VMs/Hackable_III/README.md) | [AR](VulnHub%20VMs/Hackable_III/README_AR.md) |
| **[Kioptrix Level 1](VulnHub%20VMs/Kioptrix_Level_1)** | VulnHub | Linux | Easy | Apache mod_ssl OpenFuck (`CVE-2002-0082`), Samba trans2open (`CVE-2003-0201`) | [EN](VulnHub%20VMs/Kioptrix_Level_1/README.md) | [AR](VulnHub%20VMs/Kioptrix_Level_1/README_AR.md) |
| **[Kioptrix Level 2](VulnHub%20VMs/Kioptrix_Level_2)** | VulnHub | Linux | Easy | SQL Injection Auth Bypass, Ping Command Injection, Kernel Exploit 9542.c | [EN](VulnHub%20VMs/Kioptrix_Level_2/README.md) | [AR](VulnHub%20VMs/Kioptrix_Level_2/README_AR.md) |
| **[LupinOne](VulnHub%20VMs/LupinOne)** | VulnHub | Linux | Medium | `~secret` Fuzzing, Fastcipher Key Decryption, Python Library Hijacking, Sudo Pip | [EN](VulnHub%20VMs/LupinOne/README.md) | [AR](VulnHub%20VMs/LupinOne/README_AR.md) |
| **[Matrix 1](VulnHub%20VMs/Matrix_1)** | VulnHub | Linux | Medium | Web Steganography, Brainfuck Esoteric Decoding, SUID / Sudo Escalation | [EN](VulnHub%20VMs/Matrix_1/README.md) | [AR](VulnHub%20VMs/Matrix_1/README_AR.md) |
| **[Metasploitable 1](VulnHub%20VMs/Metasploitable_1)** | VulnHub | Linux | Easy | distcc RCE (`CVE-2004-2687`), Samba trans2open, Default Databases | [EN](VulnHub%20VMs/Metasploitable_1/README.md) | [AR](VulnHub%20VMs/Metasploitable_1/README_AR.md) |
| **[Metasploitable 2](VulnHub%20VMs/Metasploitable_2)** | VulnHub | Linux | Easy | vsftpd Backdoor (`CVE-2011-2523`), Samba usermap script, UnrealIRCd, Tomcat | [EN](VulnHub%20VMs/Metasploitable_2/README.md) | [AR](VulnHub%20VMs/Metasploitable_2/README_AR.md) |
| **[Mr. Robot](VulnHub%20VMs/Mr_Robot)** | VulnHub | Linux | Medium | `robots.txt` Recon, WordPress Elliot Brute-Force, MD5 Cracking, SUID Nmap | [EN](VulnHub%20VMs/Mr_Robot/README.md) | [AR](VulnHub%20VMs/Mr_Robot/README_AR.md) |
| **[Vulnix](VulnHub%20VMs/Vulnix)** | VulnHub | Linux | Medium | Overly Permissive NFS Export, UID Spoofing (2008), `sudoedit /etc/exports` | [EN](VulnHub%20VMs/Vulnix/README.md) | [AR](VulnHub%20VMs/Vulnix/README_AR.md) |
| **[Bandit (0-16)](OverTheWire%20(Bandit)/Bandit)** | OverTheWire | Linux | Fund. | Linux CLI, Encodings (Base64/ROT13), Multi-Layer Decompression, Sockets, SSL | [EN](OverTheWire%20(Bandit)/Bandit/README.md) | [AR](OverTheWire%20(Bandit)/Bandit/README_AR.md) |

---

## 🏗️ Repository Structure

```text
.
├── OverTheWire (Bandit)/
│   └── Bandit/
│       ├── README.md               # English Bandit Guide
│       ├── README_AR.md            # Arabic Bandit Guide
│       ├── Bandit_Writeup_0-16.docx
│       └── bandit.pdf
├── TryHackMe (THM)/
│   ├── HackPark/                   # BlogEngine.NET RCE & Windows Scheduler PrivEsc
│   ├── Internal/                   # WordPress, Docker & Jenkins Pivoting
│   ├── Overpass2_Hacked/           # PCAP Forensics & Go Backdoor Reversing
│   ├── Relevant/                   # Anonymous SMB & PrintSpoofer Token Escalation
│   ├── VulnNet_DotPy/              # Werkzeug Jinja2 SSTI & Sudo Pip PrivEsc
│   └── Wreath/                     # 3-Host Enterprise Network Pivoting Chain
├── VulnHub VMs/
│   ├── Basic_Pentesting_1/         # ProFTPD mod_copy RCE
│   ├── Basic_Pentesting_2/         # SMB User Enumeration & Passphrase Cracking
│   ├── Hackable_III/               # Port Knocking & Linux PrivEsc
│   ├── Kioptrix_Level_1/           # mod_ssl OpenFuck & Samba trans2open
│   ├── Kioptrix_Level_2/           # SQLi Auth Bypass & Kernel Exploit 9542.c
│   ├── LupinOne/                   # Fastcipher Decryption & Library Hijacking
│   ├── Matrix_1/                   # Web Steganography & Brainfuck Decoding
│   ├── Metasploitable_1/           # Legacy Linux Network Services Auditing
│   ├── Metasploitable_2/           # Multi-Daemon Vulnerability Lab
│   ├── Mr_Robot/                   # Mr. Robot Full CTF Walkthrough
│   └── Vulnix/                     # NFS UID Spoofing & Sudoedit Escalation
├── README.md                       # Master Documentation (English)
└── README_AR.md                    # Master Documentation (العربية)
```

---

## 🧰 Primary Toolset Utilized

* **Network Scanning & Enumeration:** `Nmap`, `Wireshark`, `tshark`, `enum4linux`, `showmount`, `Netcat`
* **Web Exploitation & Fuzzing:** `Burp Suite`, `ffuf`, `Gobuster`, `WPScan`, `DirBuster`
* **Credential Cracking:** `John the Ripper`, `Hydra`, `ssh2john`
* **Pivoting & Tunneling:** `Chisel`, `SSH Local/Dynamic Port Forwarding`, `Proxychains`, `Socat`
* **Privilege Escalation & Post-Exploitation:** `WinPEAS`, `LinPEAS`, `PrintSpoofer`, `Mimikatz`, `Evil-WinRM`, `GTFOBins`

---

## ⚖️ Legal & Ethical Disclaimer

> [!WARNING]
> All testing, techniques, exploits, and methodologies documented in this repository were conducted strictly inside **authorized, purpose-built, and isolated lab environments** (TryHackMe, VulnHub, and OverTheWire). 
> 
> These reports are published strictly for **educational, defensive, and research purposes**. Executing any offensive techniques against targets without explicit, written authorization from the system owner is illegal and violates global cyber laws. The authors assume no liability for misuse.

---

## 👥 Authors & Contributors

* **Mohamed Hesham Mohamed**
* **Mohamed Ibrahim Mohamed**
* **Mohamed Elsayed Mohamed**
* **Ebrahim Hesham Awad**
* **Youssef Ayman Mohamed**
