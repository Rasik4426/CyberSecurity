# Nmap Scan Report

Date: 02-06-2026
Scanner: Kali Linux
Target: Metasploitable2
Target IP: 192.168.56.104

## Command Used:

sudo nmap -sS -sV -O -A 192.168.56.104 -oN nmap_report.txt

## Scan Results

Nmap scan report for 192.168.56.104
Host is up (0.00045s latency).

PORT      STATE SERVICE     VERSION
21/tcp    open  ftp         vsftpd 2.3.4
22/tcp    open  ssh         OpenSSH 4.7p1 Debian
23/tcp    open  telnet      Linux telnetd
25/tcp    open  smtp        Postfix smtpd
53/tcp    open  domain      ISC BIND DNS
80/tcp    open  http        Apache httpd 2.2.8
111/tcp   open  rpcbind     RPC #100000
139/tcp   open  netbios-ssn Samba smbd
445/tcp   open  microsoft-ds Samba smbd
512/tcp   open  exec        netkit-rsh rexecd
513/tcp   open  login       rlogin
514/tcp   open  shell       Netkit rshd
1099/tcp  open  java-rmi    GNU Classpath grmiregistry
1524/tcp  open  bindshell   Metasploitable Root Shell
2049/tcp  open  nfs         NFS Service
2121/tcp  open  ftp         ProFTPD 1.3.1
3306/tcp  open  mysql       MySQL 5.0.51a
5432/tcp  open  postgresql  PostgreSQL DB
5900/tcp  open  vnc         VNC Server
6000/tcp  open  X11         X Server
6667/tcp  open  irc         UnrealIRCd
8009/tcp  open  ajp13       Apache JServ
8180/tcp  open  http        Apache Tomcat

## OS Detection

Linux 2.6.X (Accuracy: 95%)

## Traceroute

1 hop to target

## Key Findings

1. FTP service (vsftpd 2.3.4) detected.

2. Multiple remote access services exposed:

   * SSH
   * Telnet
   * Rlogin
   * RSH

3. Samba services running on:

   * Port 139
   * Port 445

4. Database services exposed:

   * MySQL
   * PostgreSQL

5. Web services detected:

   * Apache HTTP Server
   * Apache Tomcat

6. Known vulnerable services identified:

   * vsftpd 2.3.4
   * UnrealIRCd
   * Samba
   * Tomcat

## Risk Assessment

Critical:

* vsftpd 2.3.4 Backdoor Vulnerability
* UnrealIRCd Backdoor

High:

* Samba Misconfigurations
* Telnet Service Enabled

Medium:

* Exposed Database Services
* NFS Service Accessible

Low:

* Information Disclosure through Banner Grabbing

## Recommendations

1. Disable unused services.
2. Replace Telnet with SSH.
3. Update vulnerable software versions.
4. Restrict access using firewall rules.
5. Regularly perform vulnerability assessments.
6. Monitor exposed services and logs.

# End of Report
