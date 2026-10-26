# 🛡️ مستودع تقارير اختبار الاختراق والأمن السيبراني (Penetration Testing Portfolio)

[![Platform: TryHackMe](https://img.shields.io/badge/Platform-TryHackMe-red.svg)](https://tryhackme.com)
[![Platform: VulnHub](https://img.shields.io/badge/Platform-VulnHub-blue.svg)](https://www.vulnhub.com)
[![Platform: OverTheWire](https://img.shields.io/badge/Platform-OverTheWire-green.svg)](https://overthewire.org)
[![Documentation: Bilingual](https://img.shields.io/badge/Docs-العربية%20%7C%20English-orange.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[English Version](README.md) | [📖 قراءة الدليل الرئيسي بالعربية](README_AR.md)

---

## 📌 عن هذا المستودع

مرحباً بك في **مستودع تقارير اختبار الاختراق والـ Red Teaming**. تم إنشاء هذا المستودع ليكون مرجعاً تقنياً وبورتفوليو عملياً شاملاً يوثق عمليات تقييم الثغرات، واختبار الأنظمة (Windows & Linux)، والتنقل الشبكي المتقدم (Network Pivoting)، والتحقيق الجنائي الرقمي (DFIR) في أشهر بيئات التدريب: **TryHackMe** و **VulnHub** و **OverTheWire**.

يتميز كل تقرير في هذا المستودع باحتوائه على:
* **ملخص تنفيذي ومخطط مرئي لمسار الهجوم (`Mermaid Attack Graph`)**
* **جدول تفصيلي بالثغرات مع أرقام الـ CVE ومستوى الخطورة (Severity)**
* **أوامر وخطوات الاستغلال العملية بالتفصيل مع إثبات المفهوم (PoC)**
* **آليات تصعيد الصلاحيات (Privilege Escalation) وتحليل الأسباب الجذرية للثغرة**
* **خطة معالجة أمنية (Remediation) موجهة لفرق الدفاع وإدارة الأنظمة**
* **توثيق ثنائي اللغة:** يتوفر لكل ماشين تقريران كاملان؛ أحدهما باللغة الإنجليزية (`README.md`) والآخر باللغة العربية (`README_AR.md`).

---

## 🗂️ الفهرس الشامل للمختبرات والتقارير

| الماشين / التحدي | المنصة | نظام التشغيل | مستوى الصعوبة | أبرز الثغرات والتقنيات | النسخة الإنجليزية | النسخة العربية |
| :--- | :---: | :---: | :---: | :--- | :---: | :---: |
| **[HackPark](TryHackMe%20(THM)/HackPark)** | TryHackMe | Windows | متوسط | رفع ملفات تعسفي في BlogEngine (`CVE-2019-6714`)، استغلال المهام المجدولة | [English](TryHackMe%20(THM)/HackPark/README.md) | [العربية](TryHackMe%20(THM)/HackPark/README_AR.md) |
| **[Internal](TryHackMe%20(THM)/Internal)** | TryHackMe | Linux | صعب | قالب ووردبريس 404، شبكات دوكر، استغلال أوامر Groovy في Jenkins | [English](TryHackMe%20(THM)/Internal/README.md) | [العربية](TryHackMe%20(THM)/Internal/README_AR.md) |
| **[Overpass 2: Hacked](TryHackMe%20(THM)/Overpass2_Hacked)** | TryHackMe | Linux | متوسط | تحليل حزم PCAP، كسر الهاشات، الهندسة العكسية لباك دور Go، استغلال SUID | [English](TryHackMe%20(THM)/Overpass2_Hacked/README.md) | [العربية](TryHackMe%20(THM)/Overpass2_Hacked/README_AR.md) |
| **[Relevant](TryHackMe%20(THM)/Relevant)** | TryHackMe | Windows | متوسط | مشاركة SMB قابلة للكتابة، ربط مجلد الـ SMB بالويب، أداة PrintSpoofer | [English](TryHackMe%20(THM)/Relevant/README.md) | [العربية](TryHackMe%20(THM)/Relevant/README_AR.md) |
| **[VulnNet: DotPy](TryHackMe%20(THM)/VulnNet_DotPy)** | TryHackMe | Linux | متوسط | حقن قوالب بايثون (Jinja2 SSTI)، خطأ تصريح `pip3`، استغلال PYTHONPATH | [English](TryHackMe%20(THM)/VulnNet_DotPy/README.md) | [العربية](TryHackMe%20(THM)/VulnNet_DotPy/README_AR.md) |
| **[Wreath](TryHackMe%20(THM)/Wreath)** | TryHackMe | شبكة أجهزة | صعب | تنقل شبكي بـ Chisel، ثغرة Webmin (`CVE-2019-15107`)، استغلال GitStack وسحب الذاكرة بـ Mimikatz | [English](TryHackMe%20(THM)/Wreath/README.md) | [العربية](TryHackMe%20(THM)/Wreath/README_AR.md) |
| **[Basic Pentesting 1](VulnHub%20VMs/Basic_Pentesting_1)** | VulnHub | Linux | سهل | ثغرة ProFTPD 1.3.5 mod_copy (`CVE-2015-3306`)، ووردبريس | [English](VulnHub%20VMs/Basic_Pentesting_1/README.md) | [العربية](VulnHub%20VMs/Basic_Pentesting_1/README_AR.md) |
| **[Basic Pentesting 2](VulnHub%20VMs/Basic_Pentesting_2)** | VulnHub | Linux | سهل | تعداد مستخدمي SMB، كسر تشفير مفتاح `id_rsa` بـ ssh2john، استغلال Sudo | [English](VulnHub%20VMs/Basic_Pentesting_2/README.md) | [العربية](VulnHub%20VMs/Basic_Pentesting_2/README_AR.md) |
| **[Hackable III](VulnHub%20VMs/Hackable_III)** | VulnHub | Linux | متوسط | تقنية قرع المنافذ (Port Knocking)، تخمين SSH، استغلال Crontab | [English](VulnHub%20VMs/Hackable_III/README.md) | [العربية](VulnHub%20VMs/Hackable_III/README_AR.md) |
| **[Kioptrix Level 1](VulnHub%20VMs/Kioptrix_Level_1)** | VulnHub | Linux | سهل | ثغرة mod_ssl OpenFuck (`CVE-2002-0082`)، ثغرة Samba trans2open | [English](VulnHub%20VMs/Kioptrix_Level_1/README.md) | [العربية](VulnHub%20VMs/Kioptrix_Level_1/README_AR.md) |
| **[Kioptrix Level 2](VulnHub%20VMs/Kioptrix_Level_2)** | VulnHub | Linux | سهل | تجاوز الدخول بـ SQLi، حقن أوامر في أداة Ping، ثغرة كيرنل 9542.c | [English](VulnHub%20VMs/Kioptrix_Level_2/README.md) | [العربية](VulnHub%20VMs/Kioptrix_Level_2/README_AR.md) |
| **[LupinOne](VulnHub%20VMs/LupinOne)** | VulnHub | Linux | متوسط | فحص المسار `~secret`، فك تشفير Fastcipher، اعتراض مكتبات بايثون، استغلال Sudo Pip | [English](VulnHub%20VMs/LupinOne/README.md) | [العربية](VulnHub%20VMs/LupinOne/README_AR.md) |
| **[Matrix 1](VulnHub%20VMs/Matrix_1)** | VulnHub | Linux | متوسط | فحص سورس كود الويب، فك شفرة لغة Brainfuck، تصعيد الصلاحيات لـ Root | [English](VulnHub%20VMs/Matrix_1/README.md) | [العربية](VulnHub%20VMs/Matrix_1/README_AR.md) |
| **[Metasploitable 1](VulnHub%20VMs/Metasploitable_1)** | VulnHub | Linux | سهل | ثغرة distcc (`CVE-2004-2687`)، ثغرة Samba trans2open، قواعد بيانات مفتوحة | [English](VulnHub%20VMs/Metasploitable_1/README.md) | [العربية](VulnHub%20VMs/Metasploitable_1/README_AR.md) |
| **[Metasploitable 2](VulnHub%20VMs/Metasploitable_2)** | VulnHub | Linux | سهل | باك دور vsftpd (`CVE-2011-2523`)، ثغرة Samba usermap، باك دور UnrealIRCd، تومكات | [English](VulnHub%20VMs/Metasploitable_2/README.md) | [العربية](VulnHub%20VMs/Metasploitable_2/README_AR.md) |
| **[Mr. Robot](VulnHub%20VMs/Mr_Robot)** | VulnHub | Linux | متوسط | استطلاع `robots.txt`، تخمين ووردبريس، كسر تشفير MD5، تصعيد الصلاحيات بـ SUID Nmap | [English](VulnHub%20VMs/Mr_Robot/README.md) | [العربية](VulnHub%20VMs/Mr_Robot/README_AR.md) |
| **[Vulnix](VulnHub%20VMs/Vulnix)** | VulnHub | Linux | متوسط | ثغرة مشاركة NFS المفتوحة، انتحال الـ UID، استغلال `sudoedit /etc/exports` | [English](VulnHub%20VMs/Vulnix/README.md) | [العربية](VulnHub%20VMs/Vulnix/README_AR.md) |
| **[Bandit (0-16)](OverTheWire%20(Bandit)/Bandit)** | OverTheWire | Linux | تأسيسي | أساسيات سطر أوامر لينكس، فك التشفير والترميز، فك الضغط المتعدد، اتصالات SSL والشبكات | [English](OverTheWire%20(Bandit)/Bandit/README.md) | [العربية](OverTheWire%20(Bandit)/Bandit/README_AR.md) |

---

## 🛠️ أبرز الأدوات المستخدمة في المختبرات

* **الفحص والاستطلاع:** `Nmap`, `Wireshark`, `tshark`, `enum4linux`, `showmount`, `Netcat`
* **اختبار تطبيقات الويب:** `Burp Suite`, `ffuf`, `Gobuster`, `WPScan`, `DirBuster`
* **كسر كلمات السر والتشفير:** `John the Ripper`, `Hydra`, `ssh2john`
* **التنقل الشبكي والأنفاق (Pivoting):** `Chisel`, `SSH Port Forwarding`, `Proxychains`, `Socat`
* **تصعيد الصلاحيات:** `WinPEAS`, `LinPEAS`, `PrintSpoofer`, `Mimikatz`, `Evil-WinRM`, `GTFOBins`

---

## ⚖️ إخلاء مسؤولية قانوني وأخلاقي (Legal Disclaimer)

> [!WARNING]
> تم تنفيذ جميع الاختبارات، الهجمات، واستغلال الثغرات الموثقة داخل هذا المستودع **حصرياً داخل بيئات تدريبية معزولة ومصرح بها قانونياً** (TryHackMe, VulnHub, OverTheWire).
>
> هذا المحتوى منشور لأغراض **تعليمية وبحثية وتوعوية ودفاعية فقط**. يُحظر تماماً استخدام أي من هذه التقنيات أو الأدوات ضد أي خوادم أو شبكات دون إذن خطي صريح ومسبق من مالك النظام، ويتحمل المستخدم وحده كامل المسؤولية الجنائية والقانونية عن أي سوء استخدام.

---

## 👥 أصحاب العمل والمؤلفون

* **محمد هشام محمد**
* **محمد ابراهيم محمد**
* **محمد السيد محمد**
* **ابراهيم هشام عوض**
* **يوسف ايمن محمد**
