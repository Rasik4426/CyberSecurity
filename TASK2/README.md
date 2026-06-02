# 🔐 Cybersecurity Lab Project

## 📌 Overview

This repository documents a hands-on cybersecurity lab focused on reconnaissance, network scanning, vulnerability assessment, packet analysis, and firewall configuration. The objective is to gain practical experience with industry-standard tools and techniques used in cybersecurity.

---

## 🎯 Objective

Learn and perform:

- Reconnaissance and Information Gathering
- Port and Service Scanning
- Vulnerability Assessment
- Packet Analysis using Wireshark
- Basic Firewall Configuration

---

## 🖥️ Lab Environment

### Operating Systems
- Kali Linux
- Metasploitable2

### Tools Used
- Nmap
- Wireshark
- OpenVAS / Nessus Essentials
- Netcat
- hping3
- Whois
- Nslookup
- Shodan
- iptables

---

## 📚 Lab Activities

### 1. Reconnaissance

#### Passive Reconnaissance
- Whois Lookup
- DNS Enumeration (Nslookup)
- Google Dorking
- Shodan Search

#### Active Reconnaissance
- Ping Sweep
- Banner Grabbing

**Example Commands**

```bash
whois target.com
nslookup target.com
nmap -sn 192.168.1.0/24
nc -nv <IP_ADDRESS> 80
```

---

### 2. Port & Service Scanning

#### TCP SYN Scan

```bash
sudo nmap -sS <TARGET_IP>
```

#### UDP Scan

```bash
sudo nmap -sU <TARGET_IP>
```

#### Service Version Detection

```bash
sudo nmap -sV <TARGET_IP>
```

#### OS Detection

```bash
sudo nmap -O <TARGET_IP>
```

#### Aggressive Scan

```bash
sudo nmap -A <TARGET_IP>
```

#### Save Scan Report

```bash
sudo nmap -A <TARGET_IP> -oN nmap_report.txt
```

---

### 3. Vulnerability Scanning

Performed using:

- OpenVAS
- Nessus Essentials

#### Tasks

- Configure scanner
- Create target
- Run vulnerability scan
- Analyze results

#### Severity Levels

| Severity | Description |
|-----------|------------|
| Critical | Immediate action required |
| High | Serious vulnerability |
| Medium | Moderate risk |
| Low | Minor issue |
| Info | Informational finding |

---

### 4. Packet Analysis with Wireshark

#### Capture and Analyze

- HTTP Traffic
- FTP Traffic
- DNS Traffic

#### Useful Filters

```text
http
ftp
dns
tcp
udp
```

#### Objectives

- Analyze packet flow
- Observe protocol communication
- Identify unencrypted FTP credentials
- Understand network behavior

---

### 5. SYN Flood Analysis

Simulated in a controlled lab environment using hping3.

```bash
sudo hping3 -S --flood <TARGET_IP>
```

Wireshark Filter:

```text
tcp.flags.syn == 1
```

---

### 6. Firewall Basics

#### Allow SSH

```bash
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT
```

#### Block HTTP

```bash
sudo iptables -A INPUT -p tcp --dport 80 -j DROP
```

#### View Rules

```bash
sudo iptables -L
```

---

## 📊 Deliverables

- Nmap Scan Report
- OpenVAS/Nessus Vulnerability Report
- Packet Capture Analysis
- Firewall Configuration Demonstration
- GitHub Documentation
- Demo Video

---


---

## ⚠️ Disclaimer

This project was conducted in a controlled lab environment for educational purposes only. All activities were performed on authorized systems. Unauthorized scanning or exploitation of systems without permission is illegal and unethical.

---

## 👨‍💻 Author

**Rasikraj**

B.Tech Computer Science & Engineering  
Cybersecurity Enthusiast 🔐
