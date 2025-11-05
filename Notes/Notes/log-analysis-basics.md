# 🧠 Log Analysis Basics

## 🧾 Overview
Log analysis is one of the core skills in Blue Team operations.  
It allows analysts to identify patterns, detect intrusions, and correlate system behaviors with security events.

---

## 🧩 Common Log Sources
- **Windows Event Logs**
- **Firewall & IDS Logs**
- **Web Server Logs (Apache, Nginx)**
- **Authentication Logs**
- **Application Logs**

---

## 🧰 Useful Tools
| Tool | Description |
|------|--------------|
| **Event Viewer** | Built-in Windows tool for reviewing logs. |
| **Sysmon** | Advanced Windows logging with detailed system events. |
| **ELK Stack** | Elasticsearch, Logstash, Kibana — for log aggregation and visualization. |
| **Splunk** | SIEM tool widely used for search, correlation, and visualization. |

---

## 🧠 Analyst Tips
- Always **normalize timestamps** before correlating data.
- Look for **failed logins** followed by **successful ones**.
- Cross-check **source IP addresses** across multiple logs.
- Keep a **baseline of normal activity** for comparison.

---

## 📚 References
- [TryHackMe: Blue Primer](https://tryhackme.com/room/blueprimer)
- [MITRE ATT&CK](https://attack.mitre.org/)
- [Elastic Security Documentation](https://www.elastic.co/guide/en/security/current/index.html)
