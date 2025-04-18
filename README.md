# Nmap Scan – Metasploitable 2

This project documents an Nmap scan of a vulnerable virtual machine (Metasploitable 2) from a Kali Linux attacker machine.

## 🔍 Tools Used
- Nmap 7.95
- VirtualBox
- Kali Linux
- Metasploitable 2

## 🔒 Key Findings (IOCs)
- vsFTPd 2.3.4 on port 21 (CVE-2011-2523)
- Unauthorized root shell on port 1524
- IRC service on port 6667 (CVE-2010-2075)
- Outdated MySQL, SSH, and Apache Tomcat

## 📁 Files
- `nmap-scan.txt` – Raw Nmap output
- `nmap-red-flags-cheatsheet.md` – IOC reference for future scans
