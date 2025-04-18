# 🔍 Nmap Red Flags & Indicators of Compromise (IOCs) Cheat Sheet

Use this checklist to spot potential vulnerabilities and suspicious services during Nmap scans.

---

## 🚨 High-Risk Services to Watch For

| Port | Service | Why It’s a Risk |
|------|---------|-----------------|
| 21   | FTP (vsFTPd 2.3.4) | Known backdoor (CVE-2011-2523) |
| 23   | Telnet | Unencrypted login — major red flag |
| 25   | SMTP | Open mail servers can be abused for spam/phishing |
| 139/445 | Samba/SMB | EternalBlue, LLMNR poisoning, etc. |
| 1524 | Root shell | Active backdoor — high severity |
| 3306 | MySQL | Older versions have many injection vulns |
| 5900 | VNC | Remote desktop — often unauthenticated |
| 6667 | IRC | Known botnet control channel |
| 8180 | Tomcat Manager | Often used for remote admin and vulnerable JSP apps |

---

## 🧠 Recognition Tips

- ❌ **Old version = vulnerable version**  
  Google: `vsftpd 2.3.4 CVE` to find vulnerabilities

- 🚫 **Exposed internal services**  
  - Telnet, RPC, X11, rshd should never be internet-facing

- 🕵️ **Unusual service ports**  
  - Anything like port 1524 (root shell) is highly suspicious

---

## ✅ What You Should Do After a Scan

1. Identify services running outdated versions
2. Note any open remote access protocols (Telnet, VNC, X11)
3. Check Google/CVE database for known issues:
   ```
   [service name] [version] CVE
   ```
4. Document the findings in a report or GitHub notes

---

This cheat sheet is based on real-world scenarios and CompTIA Security+ practices.
