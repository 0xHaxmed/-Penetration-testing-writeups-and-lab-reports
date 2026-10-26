# Metasploitable 1 — Vulnerability Assessment & Exploitation Report

[📖 قراءة التقرير بالعربية](README_AR.md) | [English Version](README.md)
[📄 Original Report File (PDF)](./pentest-report-metasploitable1.pdf)

---

## 📋 Overview & Metadata

| Attribute | Details |
| :--- | :--- |
| **Target Machine** | Metasploitable 1 (VulnHub / Rapid7) |
| **Assessment Type** | Multi-Service Vulnerability Assessment & Penetration Test |
| **Target OS** | Ubuntu Linux 8.04 LTS (Hardy) |
| **Tools Used** | Nmap, Metasploit Framework, Netcat |
| **Key Services Audited** | vsftpd 2.3.4, distcc daemon, Samba, Apache CGI, MySQL, PostgreSQL |

---

## 🔍 Major Exploitation Vectors Tested

### 1. distcc Daemon Remote Code Execution (CVE-2004-2687)
* **Port:** `3632/tcp`
* **Vulnerability:** Unauthenticated remote compilation daemon executing arbitrary system commands.
* **Metasploit Module:** `exploit/unix/misc/distcc_exec`
* **Result:** Shell as `daemon`.

### 2. Samba trans2open Buffer Overflow (CVE-2003-0201)
* **Port:** `139/tcp`
* **Vulnerability:** Off-by-one buffer overflow in string handling.
* **Result:** Immediate root shell.

### 3. Database Services with Default / Weak Credentials
* **MySQL (Port 3306):** Root user with empty password (`mysql -u root -h <ip>`).
* **PostgreSQL (Port 5432):** Default administrative credentials (`postgres:postgres`).
