# Nebu Mohan

### Web Vulnerability Research (Bug Hunting) | AI Security | SOC & Detection Engineering

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nebu-mohan-b13a05196/)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-212C42?style=for-the-badge&logo=tryhackme&logoColor=white)](https://tryhackme.com/p/wayne07)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nebumohan)

---

## 👨‍💻 About Me

Security engineer who learns by **building systems, breaking them, and fixing them**. I hunt web vulnerabilities, build AI-assisted security tooling, and automate SOC workflows.

- 🐞 **Bug hunting:** IDOR, Broken Access Control, authentication and API flaws
- 🤖 **AI security:** LLM-assisted triage, MCP tooling, securing AI-integrated systems
- 🛡️ **SOC & detection:** SIEM, log analysis, threat intelligence, ATT&CK mapping
- 🔨 **Currently building:** *Build-to-Break*, a series of apps I write, attack, and harden myself
- 🌍 **Location:** Dubai, United Arab Emirates
- 🏆 **Certifications:** CEH v12 (EC-Council) · CPT (Red Team Hacker Academy)

---

## 🐞 Web Vulnerability Research

### 🔓 [Build-to-Break: Vulnerable Flask Notes App](https://github.com/nebumohan/vuln-notes-app)

> Built a login/notes app, attacked it like a bug bounty hunter, then fixed every finding

| Vulnerability | How I exploited it | Fix |
|---|---|---|
| **IDOR** on `GET /notes/<id>` | Changed the ID to read other users' notes | Server-side ownership check |
| **Forgeable session** | Cracked the weak `secret_key` with `flask-unsign` and forged a session cookie | Strong secret loaded from environment |
| **Predictable password reset token** | Guessed tokens to take over other accounts | Cryptographically random, expiring token |
| **No rate limiting** | Brute-forced login with Burp Intruder | `Flask-Limiter` at 5 requests/min |
| **Username enumeration** | Different error responses revealed valid users | Uniform error responses |

- Wrote both the vulnerable and fixed versions myself, so I understand each bug at code level, not just tool level
- **Stack:** Python · Flask · SQLite · Burp Suite · flask-unsign · Flask-Limiter

**Next in the series:** a custom web scraper to learn HTTP internals, rate limiting, and bot-detection behaviour against my own app and legal practice targets.

---

## 🤖 AI Security

### 🔬 [AI-Powered Vulnerability Scanner (SAST + LLM + MCP)](https://github.com/nebumohan/ai-vulnerability-scanner)

> Static analysis pipeline with AI-driven triage and structured reporting

- Detects vulnerabilities with **Bandit** and **Semgrep** across Python codebases (OWASP Top 10 patterns)
- Sends findings to the **Google Gemini API** for contextual explanation, CVSS scoring, and fix suggestions
- Maps findings to **MITRE ATT&CK** techniques using CISA Decider
- Exposes a `scan_file` tool over **Model Context Protocol (MCP)**, callable from Claude Desktop for conversational security scanning
- Stores results in **SQLite** and generates **HTML reports** with Jinja2
- **Stack:** Python · Bandit · Semgrep · Gemini API · MCP · SQLite · Jinja2

**Learning track:** prompt injection, insecure tool use in MCP/agent systems, and the OWASP Top 10 for LLM Applications.

---

## 🛡️ SOC & Detection Engineering

### 🌐 [Azure Global Attack Honeypot](https://github.com/nebumohan/azure-global-attack-honeypot)

> Cloud-deployed deception infrastructure capturing real-world attacker behaviour

- Deployed a **Microsoft Sentinel**-backed honeypot on Azure and wrote custom **KQL detection rules**
- Enriched attacker IPs with **GeoIP** and visualised global attack origins on an attack map
- Captured real credential-stuffing attempts, port scans, and attacker TTPs
- **Stack:** Azure · Microsoft Sentinel · KQL · GeoIP · Python

### 🧠 [SOC Log Parser & Geo-Threat Intelligence Tool](https://github.com/nebumohan/log-parser)

> SOC automation tool for brute-force detection and threat actor geolocation

- Parses raw system logs to detect repeated failed login attempts
- Flags suspicious IPs and enriches them with geolocation and IOC data
- Generates structured `alerts.txt` reports that mirror real SOC triage output
- **Stack:** Python · IP-API · Requests

---

## 🧰 Technical Toolkit

**Web & Offensive Security**

![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square&logo=portswigger&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-4682B4?style=flat-square&logoColor=white)
![Metasploit](https://img.shields.io/badge/Metasploit-2596CD?style=flat-square&logo=metasploit&logoColor=white)

**AppSec & AI Security**

![Semgrep](https://img.shields.io/badge/Semgrep-1E2937?style=flat-square&logo=semgrep&logoColor=white)
![Bandit](https://img.shields.io/badge/Bandit-3776AB?style=flat-square&logo=python&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square&logoColor=white)

**Languages & Scripting**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![KQL](https://img.shields.io/badge/KQL-0078D4?style=flat-square&logoColor=white)

**Infrastructure & Platforms**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

---

## 🏆 Certifications

| Certification | Issuer | Focus |
|---|---|---|
| Certified Ethical Hacker v12 (CEH) | EC-Council | Offensive Security, Vulnerability Assessment |
| Certified Penetration Tester (CPT) | Red Team Hacker Academy | Red Teaming, Network Penetration Testing |

---

## 🤝 Connect

Building towards **application security, AI security, and SOC/cloud security** roles.

If you work on bug bounty, AI/LLM security, detection engineering, or security automation, I'd like to connect.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/nebu-mohan-b13a05196/)

---

*I build security tools and test systems the way attackers do, so I can defend them the way engineers should.*
