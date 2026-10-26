# OverTheWire: Bandit (Levels 0 → 16) — Complete Walkthrough

[📖 قراءة الدليل بالعربية](README_AR.md) | [English Version](README.md)
[📄 Original Document (DOCX)](./Bandit_Writeup_0-16.docx) | [📄 Original PDF](./bandit.pdf)

---

## 📋 Overview & Metadata

| Attribute | Details |
| :--- | :--- |
| **Platform** | OverTheWire (OTW) |
| **Wargame** | Bandit (Levels 0 to 16) |
| **Target Host** | `bandit.labs.overthewire.org` |
| **Port** | `2220` |
| **Focus Areas** | Linux CLI Mastery, File System Navigation, Text Filtering, Data Encodings, Multi-Layer Compression, Network Sockets & SSL/TLS |
| **Audience** | Cybersecurity Beginners, Linux Learners & CTF Enthusiasts |

---

## 🎯 Skills & Commands Matrix

| Category | Commands & Tools Covered |
| :--- | :--- |
| **Basic Navigation** | `ssh`, `ls`, `cd`, `cat`, `pwd`, `file` |
| **File Attributes & Search** | `find`, `stat`, `du`, `test` |
| **Text Processing & Filtering** | `grep`, `sort`, `uniq`, `strings`, `cut`, `awk`, `head`, `tail` |
| **Encodings & Ciphers** | `base64`, `tr` (ROT13), `xxd` (Hex dump reverse) |
| **Archive Decompression** | `gzip`, `bzip2`, `tar`, `mv`, `file` |
| **Networking & Sockets** | `nc` (Netcat), `openssl s_client`, `nmap` |

---

## 🛠️ Step-by-Step Level Solutions (0 → 16)

### Level 0 → Level 1: SSH Basics & First Flag
Connect to the Bandit game server via SSH:
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
Password: `bandit0`

Inspect directory and read the readme:
```bash
ls -la
cat readme
```
Password for Level 1: `NH2SXQYrBad9PkMmODt0SxD5scmfcxqq`

---

### Level 1 → Level 2: Dashed Filenames
The file is named `-`. To prevent `cat` from interpreting `-` as standard input (stdin), specify the relative path or end-of-options delimiter:
```bash
cat ./-
# Or:
cat -- -
```
Password for Level 2: `rRGizSaX8Mk1RTb1CNQoXTcKiIDTX2kh`

---

### Level 2 → Level 3: Filenames with Spaces
The file is named `spaces in this filename`. Handle spaces using quotes or backslash escapes:
```bash
cat "spaces in this filename"
# Or:
cat spaces\ in\ this\ filename
```
Password for Level 3: `aBZ0W5EmUfAf7kHTQal8LzWVsWegAcB9`

---

### Level 3 → Level 4: Hidden Files
Change directory into `inhere` and list all hidden files:
```bash
cd inhere
ls -la
cat .hidden
```
Password for Level 4: `2EW7nGlPathdAQitOiAFquNIHNutabys`

---

### Level 4 → Level 5: Human-Readable File Detection
Inside `inhere/` are multiple binary/text files. Use `file` command to identify the ASCII text file:
```bash
cd inhere
file ./*
cat ./-file07
```
Password for Level 5: `lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR`

---

### Level 5 → Level 6: Finding Files by Size & Attributes
Find a file inside `inhere/` that is human-readable, 1033 bytes in size, and not executable:
```bash
find inhere -type f -size 1033c ! -executable
cat inhere/maybehere07/.file2
```
Password for Level 6: `P4L4vucdmLnm8OzspVlupzbqKmmfoWZZ`

---

### Level 6 → Level 7: System-Wide File Search by Ownership
Find a file owned by user `bandit7`, group `bandit6`, and 33 bytes in size:
```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```
Password for Level 7: `z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S`

---

### Level 7 → Level 8: Pattern Matching in Large Files
The password is next to the word `millionth` in `data.txt`:
```bash
grep "millionth" data.txt
```
Password for Level 8: `TESKZC0XvTetK0S9xNwm25STFBFtstB0`

---

### Level 8 → Level 9: Unique Lines
The password is the only line of text that occurs only once:
```bash
sort data.txt | uniq -u
```
Password for Level 9: `EN632PlfYiZ02xQYiVmAjRL6Ah0jHpKk`

---

### Level 9 → Level 10: Extracting Printable Strings
Find human-readable strings preceded by several `=` characters:
```bash
strings data.txt | grep "==="
```
Password for Level 10: `G7w8LIi6J3tSmgGBGB7q3TVywDG1ekLD`

---

### Level 10 → Level 11: Base64 Decoding
Decode Base64 encoded file:
```bash
base64 -d data.txt
```
Password for Level 11: `6zPeziLUIFnBoVAbtbdZssFQkZZunSr6`

---

### Level 11 → Level 12: ROT13 Cipher
Decode letters rotated by 13 positions using `tr`:
```bash
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
```
Password for Level 12: `JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv`

---

### Level 12 → Level 13: Multi-Layer Compression Pipeline
`data.txt` is a hex dump. Reverse the hex dump and uncompress sequentially:
```bash
mkdir /tmp/bandit12 && cd /tmp/bandit12
cp ~/data.txt .
xxd -r data.txt uncompressed

# Identify and decompress each layer
file uncompressed
# gzip: mv uncompressed file.gz && gunzip file.gz
# bzip2: bzip2 -d file.bz2
# tar: tar -xf file.tar
```
Repeat until plaintext is reached.
Password for Level 13: `wbBFrRv4HpDARFsNuCnFYxTTjQflSZdh`

---

### Level 13 → Level 14: SSH Key-Based Authentication
Use the private SSH key to authenticate as `bandit14` on localhost:
```bash
ssh -i sshkey.private bandit14@localhost -p 2220
```
Retrieve password for Level 14:
```bash
cat /etc/bandit_pass/bandit14
```
Password for Level 14: `fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq`

---

### Level 14 → Level 15: Submitting Data to a Network Socket (Netcat)
Submit the Level 14 password to port `30000` on localhost:
```bash
echo "fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq" | nc localhost 30000
```
Password for Level 15: `jN2kg0NYaFaSplKmmgxGL052NkDZ7CPv`

---

### Level 15 → Level 16: Encrypted SSL/TLS Network Connection
Send the password to an SSL-encrypted port (`30001`):
```bash
openssl s_client -connect localhost:30001 -quiet
```
Submit password to receive credentials for Level 16:
Password for Level 16: `MQ7TaCheck...`

---

### Level 16 → Level 17: Port Scanning & SSH Key Extraction
1. Scan ports 31000-32000 to find SSL listeners:
   ```bash
   nmap -sV -p 31000-32000 localhost
   ```
2. Connect using `openssl s_client` to the SSL port that echoes credentials:
   ```bash
   openssl s_client -connect localhost:31790 -quiet
   ```
3. Submit the Level 16 password. The server returns an **RSA Private Key** for user `bandit17`!
4. Save the key, set permissions (`chmod 600 key`), and connect to Level 17:
   ```bash
   ssh -i key bandit17@localhost -p 2220
   ```

---

## 🛡️ Key Takeaways for Beginners
1. **Linux Philosophy:** Everything is a file, and pipelines (`|`) allow chaining simple tools to solve complex forensic challenges.
2. **Standard Streams:** Understanding `stdin`, `stdout`, and `stderr` (`2>/dev/null`) is critical for clean filtering.
3. **Encodings vs Encryption:** Base64 and ROT13 are encodings/ciphers with no key requirement; SSL/TLS and SSH provide cryptographic security.
