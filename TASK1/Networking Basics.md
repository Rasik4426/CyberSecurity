#  Networking Basics

## Objective

To understand the fundamental concepts of computer networking, including the OSI model, TCP/IP protocol suite, DNS, HTTP/HTTPS, IP addressing, subnetting, and NAT.

---

## Introduction

Networking is the process of connecting computers and devices to share data and resources. Understanding networking fundamentals is essential for cybersecurity professionals because most cyberattacks occur over networks.

---

## 1. OSI Model (Open Systems Interconnection)

The OSI Model is a conceptual framework that explains how data is transmitted between devices over a network. It consists of seven layers, where each layer performs specific functions and communicates with the layers directly above and below it.

### OSI Layers

| Layer No. | Layer Name   | Function                                             |
| --------- | ------------ | ---------------------------------------------------- |
| 7         | Application  | Provides services to end-user applications           |
| 6         | Presentation | Handles data formatting, encryption, and compression |
| 5         | Session      | Establishes and manages communication sessions       |
| 4         | Transport    | Ensures reliable data transfer                       |
| 3         | Network      | Handles routing and logical addressing               |
| 2         | Data Link    | Provides node-to-node communication                  |
| 1         | Physical     | Transmits raw bits over physical media               |

### Key Points

* The OSI model contains 7 layers.
* Each layer has a specific responsibility.
* It helps in troubleshooting network-related issues.

---

## 2. TCP/IP Protocol Suite

The TCP/IP model is the practical networking model used on the Internet. It defines how data is transmitted between devices.

### TCP/IP Layers

| Layer          | Function                           |
| -------------- | ---------------------------------- |
| Application    | User-facing protocols and services |
| Transport      | End-to-end communication           |
| Internet       | Routing and addressing             |
| Network Access | Physical network communication     |

### Common Protocols

| Protocol | Purpose                  |
| -------- | ------------------------ |
| HTTP     | Web communication        |
| HTTPS    | Secure web communication |
| DNS      | Domain name resolution   |
| TCP      | Reliable data transfer   |
| UDP      | Fast data transfer       |
| IP       | Addressing and routing   |

### Key Points

* TCP/IP is the foundation of the Internet.
* It consists of 4 layers.
* Most modern networks use the TCP/IP model.

---

## 3. DNS (Domain Name System)

DNS is a system that translates human-readable domain names into IP addresses.

### Example

Domain Name:
google.com

IP Address:
142.250.xxx.xxx

### Benefits

* Easy website access using names instead of numbers.
* Faster navigation on the Internet.
* Supports large-scale internet communication.

### Key Points

* DNS acts like the Internet's phonebook.
* Converts domain names into IP addresses.
* Essential for browsing websites.

---

## 4. HTTP and HTTPS

### HTTP (HyperText Transfer Protocol)

HTTP is a protocol used for communication between web browsers and web servers.

**Characteristics:**

* Data is transmitted in plain text.
* Less secure.
* Uses Port 80.

### HTTPS (HyperText Transfer Protocol Secure)

HTTPS is the secure version of HTTP that uses SSL/TLS encryption.

**Characteristics:**

* Data is encrypted.
* More secure.
* Uses Port 443.

### HTTP vs HTTPS

| Feature         | HTTP | HTTPS |
| --------------- | ---- | ----- |
| Security        | Low  | High  |
| Encryption      | No   | Yes   |
| Port            | 80   | 443   |
| Data Protection | No   | Yes   |

### Key Points

* HTTPS protects user data during transmission.
* Most modern websites use HTTPS.
* SSL/TLS certificates enable secure communication.

---

## 5. IP Addressing

An IP Address is a unique identifier assigned to a device connected to a network.

### Types of IP Addresses

#### IPv4

* 32-bit address.
* Example: 192.168.1.1

#### IPv6

* 128-bit address.
* Example: 2001:db8::1

### Importance

* Identifies devices on a network.
* Enables communication between systems.
* Supports internet connectivity.

---

## 6. Subnetting

Subnetting is the process of dividing a large network into smaller and manageable networks called subnets.

### Advantages

* Improves network performance.
* Enhances security.
* Reduces network congestion.
* Simplifies network management.

### Example

Network:
192.168.1.0/24

Possible Subnets:

* 192.168.1.0/26
* 192.168.1.64/26
* 192.168.1.128/26
* 192.168.1.192/26

### Key Points

* Subnetting divides large networks.
* Improves efficiency and security.
* Widely used in enterprise environments.

---

## 7. NAT (Network Address Translation)

NAT is a networking technique that allows multiple devices on a private network to share a single public IP address.

### Working of NAT

1. A device sends a request to the Internet.
2. The router replaces the private IP address with its public IP address.
3. The response is received by the router.
4. The router forwards the response to the correct device.

### Advantages

* Conserves public IP addresses.
* Improves network security.
* Allows multiple devices to access the Internet simultaneously.

### Example

Private IP:
192.168.1.10

Public IP:
103.25.50.100

The router translates the private address into the public address before sending traffic to the Internet.

---

## Conclusion

Networking forms the backbone of cybersecurity. Understanding the OSI model, TCP/IP, DNS, HTTP/HTTPS, IP addressing, subnetting, and NAT provides a strong foundation for advanced cybersecurity topics such as network security, penetration testing, traffic analysis, and ethical hacking.
