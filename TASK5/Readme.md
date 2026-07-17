
# 🛡️ CyberShield SIEM – Real-Time Security Information and Event Management Using ELK Stack

> A mini Security Information and Event Management (SIEM) solution built using the ELK Stack to collect, analyze, and visualize security logs while detecting cyber attacks using MITRE ATT&CK mapping.

---

## 📖 Project Overview

CyberShield SIEM is a mini Security Information and Event Management (SIEM) system developed using the **ELK Stack (Elasticsearch, Logstash, Kibana)**. The project demonstrates centralized log collection, log analysis, security event monitoring, and visualization in a virtualized cybersecurity lab.

Security events generated from cyber attack simulations using **Kali Linux** are collected from a **Ubuntu victim machine** using **Filebeat**, processed by **Logstash**, stored in **Elasticsearch**, and visualized through interactive **Kibana dashboards**.

The project also enriches detected events using the **MITRE ATT&CK Framework**, making it easier to classify and understand attacker behavior.

---

# 🎯 Objectives

- Build a centralized log management system
- Collect Linux authentication and system logs
- Detect cyber attacks in real time
- Visualize security events using Kibana
- Map attacks to the MITRE ATT&CK Framework
- Understand the workflow of a Security Operations Center (SOC)

---

# 🏗️ System Architecture

```text
                     Kali Linux
                  (Attacker Machine)
                         │
        ┌────────────────┼────────────────┐
        │                │                │
        ▼                ▼                ▼
 SSH Brute Force     Nmap Scan      SSH Login
        │                │                │
        └────────────────┴────────────────┘
                         │
                         ▼
             Ubuntu Victim Machine
                (Filebeat Agent)
                         │
                         ▼
                  Logstash Pipeline
             (Parsing & MITRE Mapping)
                         │
                         ▼
                  Elasticsearch
                         │
                         ▼
                Kibana Dashboards
```

---

# 🛠️ Technologies Used

- Elasticsearch
- Logstash
- Kibana
- Filebeat
- Ubuntu Server
- Kali Linux
- VirtualBox
- Hydra
- Nmap
- OpenSSH
- MITRE ATT&CK Framework

---

# 💻 Lab Environment

| Machine | Operating System | Purpose |
|----------|------------------|---------|
| ELK Server | Ubuntu Server | Elasticsearch, Logstash, Kibana |
| Victim Machine | Ubuntu Server | Filebeat & Log Source |
| Attacker Machine | Kali Linux | Attack Simulation |

---

# ✨ Features

- Centralized Log Collection
- Real-Time Log Monitoring
- SSH Login Monitoring
- SSH Brute Force Detection
- Authentication Monitoring
- MITRE ATT&CK Mapping
- Kibana Security Dashboards
- Incident Investigation
- SOC-Style Monitoring

---

# 🔄 Project Workflow

```text
Kali Linux
      │
      ▼
Attack Simulation
      │
      ▼
Ubuntu Victim
(Filebeat)
      │
      ▼
Logstash
(Log Parsing & Enrichment)
      │
      ▼
Elasticsearch
(Indexing)
      │
      ▼
Kibana
(Visualization)
```

---

# 🧪 Attack Simulations

## 1. SSH Brute Force

**Tool:** Hydra

```bash
hydra -l victim -P passwords.txt ssh://192.168.56.30
```

**MITRE Technique**

- Technique ID: **T1110**
- Technique: **Brute Force**
- Tactic: **Credential Access**

---

## 2. Successful SSH Login

```bash
ssh victim@192.168.56.30
```

**MITRE Technique**

- Technique ID: **T1021.004**
- Technique: **Remote Services: SSH**
- Tactic: **Lateral Movement**

---

## 3. Invalid User Login

```bash
ssh admin@192.168.56.30
```

**MITRE Technique**

- Technique ID: **T1110**
- Technique: **Brute Force**

---

## 4. Network Service Discovery

```bash
nmap -A 192.168.56.30
```

**MITRE Technique**

- Technique ID: **T1046**
- Technique: **Network Service Discovery**
- Tactic: **Discovery**

---

## 5. Privilege Escalation

```bash
sudo -k
sudo ls
```

**MITRE Technique**

- Technique ID: **T1548**
- Technique: **Abuse Elevation Control Mechanism**
- Tactic: **Privilege Escalation**

---

# 🛡️ MITRE ATT&CK Mapping

| Attack | Technique ID | Technique | Tactic |
|---------|--------------|-----------|--------|
| SSH Brute Force | T1110 | Brute Force | Credential Access |
| Invalid User Login | T1110 | Brute Force | Credential Access |
| SSH Login | T1021.004 | Remote Services: SSH | Lateral Movement |
| Nmap Scan | T1046 | Network Service Discovery | Discovery |
| sudo Activity | T1548 | Abuse Elevation Control Mechanism | Privilege Escalation |

---

# 📊 Kibana Dashboards

### SOC Overview Dashboard

- Total Security Events
- Failed SSH Logins
- Successful SSH Logins
- Active Hosts
- Event Timeline

### Authentication Dashboard

- Failed Logins
- Successful Logins
- Invalid Users
- SSH Sessions

### MITRE ATT&CK Dashboard

- MITRE Techniques
- MITRE Tactics
- Attack Distribution
- Attack Timeline

### Incident Dashboard

- Top Source IPs
- Recent Events
- Security Alerts
- Authentication Logs

---

# 📂 Repository Structure

```text
CyberShield-SIEM/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── configs/
│   ├── filebeat.yml
│   ├── logstash.conf
│   ├── kibana.yml
│   └── elasticsearch.yml
│
├── dashboards/
│   ├── SOC_Dashboard.ndjson
│   ├── MITRE_Dashboard.ndjson
│   └── Authentication_Dashboard.ndjson
│
├── screenshots/
│   ├── dashboard.png
│   ├── discover.png
│   ├── hydra_attack.png
│   ├── nmap_scan.png
│   └── mitre_dashboard.png
│
├── attacks/
│   ├── hydra.md
│   ├── ssh.md
│   ├── nmap.md
│   └── mitre_mapping.md
│
├── docs/
│   ├── Installation.md
│   ├── Architecture.md
│   └── User_Guide.md
│
└── scripts/
    ├── install_elk.sh
    ├── install_filebeat.sh
    └── verify_services.sh
```

---

# 📸 Screenshots

Include screenshots of:

- ELK Services Running
- Kibana Home
- Discover Page
- SOC Dashboard
- MITRE Dashboard
- Hydra Attack Detection
- Nmap Detection
- Authentication Logs
- Logstash Pipeline

---

# 🚀 Future Enhancements

- Integrate Suricata IDS
- Add Zeek Network Monitoring
- Integrate Wazuh
- Winlogbeat Support
- Email Alerts
- GeoIP Mapping
- AI-Based Threat Detection
- Automated Incident Response
- PDF Report Generation
- Docker Log Monitoring

---

# 📚 Learning Outcomes

- Understood SIEM architecture and workflow
- Installed and configured the ELK Stack
- Implemented centralized log collection
- Monitored Linux authentication logs
- Simulated cyber attacks using Kali Linux
- Mapped events to the MITRE ATT&CK Framework
- Built interactive Kibana dashboards
- Performed basic SOC-style incident monitoring

---

# 👨‍💻 Author

**Rasikraj Santosh Angane**

**B.Tech – Computer Science & Engineering (Cybersecurity & Digital Forensics)**

**MIT Art, Design & Technology University, Pune**

---

# ⭐ Project Highlights

- ✅ Complete ELK Stack Deployment
- ✅ Centralized Log Management
- ✅ Real-Time Security Monitoring
- ✅ MITRE ATT&CK Integration
- ✅ SSH Brute Force Detection
- ✅ SSH Login Monitoring
- ✅ Nmap Attack Simulation
- ✅ Interactive Kibana Dashboards
- ✅ SOC-Style Security Monitoring
- ✅ Hands-on Cybersecurity Project

---

## 📄 License

This project is intended for **educational and research purposes only**. All attack simulations were performed in a controlled virtual lab environment on systems owned by the author.

---
**⭐ If you found this project useful, consider giving it a star on GitHub!**
