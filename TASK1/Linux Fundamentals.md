#  Linux Fundamentals

## Objective

To understand the basics of Linux, including file system navigation, file permissions, package management, and essential networking commands used in cybersecurity and system administration.

---

# Introduction to Linux

Linux is an open-source operating system widely used in cybersecurity, networking, cloud computing, and system administration. It is known for its security, stability, flexibility, and powerful command-line interface (CLI).

### Why Linux is Important in Cybersecurity?

* Most security tools are designed for Linux.
* Provides powerful command-line utilities.
* Highly customizable and secure.
* Widely used in servers and cloud environments.
* Supports penetration testing distributions such as Kali Linux.

---

# File System Navigation Commands

Linux uses a hierarchical file system structure where files and directories are organized in a tree-like format.

## 1. pwd (Print Working Directory)

Displays the current directory in which the user is working.

### Syntax

```bash
pwd
```

### Example Output

```bash
/home/kali/Documents
```

### Purpose

* Identify the current location in the file system.
* Useful while navigating directories.

---

## 2. ls (List Directory Contents)

Lists files and folders within a directory.

### Syntax

```bash
ls
```

### Common Options

```bash
ls -l
```

Displays detailed file information.

```bash
ls -a
```

Shows hidden files and folders.

### Purpose

* View directory contents.
* Check file permissions and ownership.

---

## 3. cd (Change Directory)

Used to move between directories.

### Syntax

```bash
cd directory_name
```

### Examples

```bash
cd Documents
```

```bash
cd ..
```

Moves one directory back.

### Purpose

* Navigate the Linux file system efficiently.

---

# File and Directory Permissions

Linux uses permissions to control who can access files and directories.

## Basic Permissions

| Permission | Symbol | Description             |
| ---------- | ------ | ----------------------- |
| Read       | r      | View file contents      |
| Write      | w      | Modify file contents    |
| Execute    | x      | Run a file as a program |

### Permission Example

```bash
-rwxr-xr-x
```

This indicates:

* Owner: Read, Write, Execute
* Group: Read, Execute
* Others: Read, Execute

---

## chmod Command

The `chmod` command is used to change file permissions.

### Syntax

```bash
chmod permissions filename
```

### Example

```bash
chmod 755 script.sh
```

### Purpose

* Control file access.
* Make scripts executable.
* Improve system security.

---

## chown Command

The `chown` command changes file ownership.

### Syntax

```bash
sudo chown user:group filename
```

### Example

```bash
sudo chown kali:kali notes.txt
```

### Purpose

* Assign files to different users.
* Manage file ownership securely.

---

# Package Management

Package management allows software installation, updates, and removal in Linux.

---

## apt (Advanced Package Tool)

`apt` is the default package manager in Debian-based distributions such as Ubuntu and Kali Linux.

### Update Package List

```bash
sudo apt update
```

### Upgrade Installed Packages

```bash
sudo apt upgrade
```

### Install Software

```bash
sudo apt install nmap
```

### Remove Software

```bash
sudo apt remove nmap
```

### Purpose

* Install new applications.
* Update system packages.
* Manage software dependencies.

---

## dpkg (Debian Package Manager)

`dpkg` is used to manage `.deb` package files directly.

### Install a Package

```bash
sudo dpkg -i package.deb
```

### List Installed Packages

```bash
dpkg -l
```

### Purpose

* Install local Debian packages.
* Manage package information.

---

# Networking Commands

Networking commands help monitor and troubleshoot network connectivity.

---

## 1. ifconfig

Displays network interface information.

### Syntax

```bash
ifconfig
```

### Information Displayed

* IP Address
* MAC Address
* Network Interface Status

### Purpose

* View network configuration.
* Troubleshoot connectivity issues.

---

## 2. ping

Tests connectivity between two devices.

### Syntax

```bash
ping google.com
```

### Purpose

* Check network connectivity.
* Measure response time.
* Verify host availability.

---

## 3. netstat

Displays active network connections and listening ports.

### Syntax

```bash
netstat -tulnp
```

### Purpose

* Monitor network activity.
* Identify open ports.
* Troubleshoot services.

---

## 4. traceroute

Shows the path packets take to reach a destination.

### Syntax

```bash
traceroute google.com
```

### Purpose

* Analyze network routes.
* Detect network delays.
* Troubleshoot routing issues.

---

# Key Learning Outcomes

After completing this task, you should be able to:

✅ Navigate the Linux file system.

✅ Understand Linux file permissions.

✅ Modify permissions and ownership using chmod and chown.

✅ Install and manage software using apt and dpkg.

✅ Use networking commands to troubleshoot connectivity issues.

✅ Build a strong foundation for cybersecurity and ethical hacking.

---

# Conclusion

Linux is one of the most important operating systems in cybersecurity. Understanding Linux commands, permissions, package management, and networking tools is essential for ethical hackers, penetration testers, and security professionals. Mastering these fundamentals provides a strong foundation for advanced cybersecurity concepts and practical security assessments.
