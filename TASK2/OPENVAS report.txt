# OpenVAS Vulnerability Assessment Report

Date: 02-06-2026
Target: Metasploitable2
Target IP: 192.168.56.104
Scanner: OpenVAS Community Edition

# Commands Used

1. Verify OpenVAS Installation

```bash
gvm-check-setup
```

2. Start OpenVAS Services

```bash
sudo gvm-start
```

3. Check Running Services

```bash
sudo gvm-status
```

4. Access Web Interface

```text
https://127.0.0.1:9392
```

5. Login to Greenbone Security Assistant (GSA)

Username:
admin

Password: <generated during setup>

6. Create Target

## Configuration:

Name: Metasploitable2
IP Address: 192.168.56.101

7. Create Scan Task

Task Name:
Metasploitable2 Full Scan

Scan Configuration:
Full and Fast

8. Start Scan

Tasks → Select Target → Start Scan

9. Generate Report

Reports → Export → PDF/TXT

==================================================

# Executive Summary

The vulnerability scan identified multiple critical and high-risk vulnerabilities due to outdated and intentionally vulnerable services running on the target system.

# Scan Results Summary

Critical Vulnerabilities : 2
High Vulnerabilities     : 5
Medium Vulnerabilities   : 8
Low Vulnerabilities      : 6
Informational Findings   : 12

Total Findings           : 33

==================================================

# Critical Findings

1. VSFTPD 2.3.4 Backdoor

Port: 21/TCP
Severity: Critical
CVSS: 10.0

Description:
A malicious backdoor exists in the VSFTPD service which may allow remote command execution.

Recommendation:
Upgrade or remove the vulnerable FTP service.

---

2. UnrealIRCd Backdoor

Port: 6667/TCP
Severity: Critical
CVSS: 10.0

Description:
Known backdoor vulnerability allowing unauthorized access.

Recommendation:
Replace with a secure version.

==================================================

# High Severity Findings

• Samba Remote Code Execution
Ports: 139,445

• Telnet Enabled
Port: 23

• Apache Tomcat Default Credentials
Port: 8180

• Weak SSH Configuration
Port: 22

• Exposed MySQL Service
Port: 3306

==================================================

# Medium Severity Findings

• Anonymous FTP Login Enabled
• Outdated Apache Web Server
• NFS Misconfiguration
• Information Disclosure
• PostgreSQL Exposure
• Weak TLS Configuration
• RPC Services Exposed
• Open Management Services

==================================================

# Low Severity Findings

• ICMP Timestamp Response
• DNS Version Disclosure
• HTTP Banner Disclosure
• Open Information Services
• Unnecessary Open Ports
• Weak Service Banners

==================================================

# Risk Assessment

Critical:
Immediate system compromise possible.

High:
Privilege escalation and unauthorized access possible.

Medium:
Useful for reconnaissance and lateral movement.

Low:
Information disclosure vulnerabilities.

==================================================

# Recommendations

1. Disable unnecessary services.
2. Replace Telnet with SSH.
3. Apply security patches.
4. Restrict service exposure using firewall rules.
5. Change default credentials.
6. Perform regular vulnerability assessments.
7. Monitor logs for suspicious activities.

==================================================

# Conclusion

The scan successfully identified multiple vulnerabilities on the Metasploitable2 target. OpenVAS proved effective in detecting critical security weaknesses and provided actionable remediation recommendations.

# End of Report
