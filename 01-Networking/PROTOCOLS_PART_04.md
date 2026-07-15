---

# 🛡️ Common Network Protocol Attacks

As a cybersecurity professional or ethical hacker, understanding how protocols can be attacked is just as important as knowing how they work.

Attackers often exploit weaknesses in protocols, poor configurations, or insecure implementations to gain unauthorized access or disrupt services.

Let's explore some of the most common protocol-based attacks.

---

# 1. ARP Spoofing (ARP Poisoning)

## What is ARP Spoofing?

ARP Spoofing is an attack where an attacker sends fake ARP replies on a local network.

The attacker tricks other devices into believing their MAC address belongs to another device, such as the router.

As a result, network traffic is redirected through the attacker's machine.

---

## Example

Imagine you tell everyone in your office:

> "I'm the receptionist."

Now everyone gives you their documents instead of the real receptionist.

That's exactly what happens during an ARP Spoofing attack.

---

## Risks

- Man-in-the-Middle (MITM)
- Data Theft
- Password Capture
- Session Hijacking

---

## Prevention

- Static ARP entries (where appropriate)
- Dynamic ARP Inspection (DAI)
- Secure switches
- VPN encryption

---

# 2. DNS Spoofing

## What is DNS Spoofing?

DNS Spoofing (or DNS Cache Poisoning) tricks a DNS server into returning a fake IP address.

Instead of visiting the real website, the victim is redirected to a malicious one.

---

## Example

You type:

```
www.bank.com
```

Instead of opening the real banking website, you're redirected to a fake login page designed to steal your credentials.

---

## Prevention

- DNSSEC
- HTTPS
- Secure DNS providers
- Verify website certificates

---

# 3. DHCP Starvation Attack

## What is DHCP Starvation?

An attacker floods the DHCP server with fake requests until all available IP addresses are assigned.

Legitimate users can no longer obtain an IP address.

---

## Prevention

- DHCP Snooping
- Port Security
- Rate Limiting

---

# 4. SYN Flood Attack

## What is a SYN Flood?

TCP uses a Three-Way Handshake to establish connections.

An attacker sends thousands of SYN packets but never completes the handshake.

The server keeps waiting for responses until its resources are exhausted.

---

## Prevention

- SYN Cookies
- Firewalls
- Rate Limiting
- Intrusion Prevention Systems (IPS)

---

# 5. ICMP Flood Attack (Ping Flood)

Attackers send massive numbers of ICMP Echo Requests to overwhelm a target.

---

## Prevention

- Firewall Rules
- Rate Limiting
- Disable unnecessary ICMP responses

---

# 6. SMB Exploitation

Older versions of SMB have contained serious vulnerabilities.

Examples include:

- EternalBlue
- WannaCry
- NotPetya

---

## Prevention

- Disable SMBv1
- Install security updates
- Restrict SMB access
- Use strong authentication

---

# 7. FTP Brute Force Attack

Attackers repeatedly try different username and password combinations to access an FTP server.

---

## Prevention

- Strong passwords
- Multi-Factor Authentication (where supported)
- Account lockout policies
- Prefer SFTP over FTP

---

# Secure vs Insecure Protocols

| Secure Protocol | Insecure Alternative |
|-----------------|----------------------|
| HTTPS | HTTP |
| SSH | Telnet |
| SFTP | FTP |
| LDAPS | LDAP |
| IMAPS | IMAP |
| POP3S | POP3 |
| SMTPS | SMTP |

Whenever possible, choose the secure version.

---

# Wireshark Examples

Wireshark is one of the most popular network packet analyzers.

Some useful filters include:

### HTTP

```
http
```

### HTTPS

```
tls
```

### DNS

```
dns
```

### ICMP

```
icmp
```

### ARP

```
arp
```

### TCP

```
tcp
```

### UDP

```
udp
```

### DHCP

```
bootp
```

### FTP

```
ftp
```

### SSH

```
ssh
```

---

# Nmap Examples

## Scan Top 1000 Ports

```bash
nmap 192.168.1.10
```

---

## Service Detection

```bash
nmap -sV 192.168.1.10
```

---

## Operating System Detection

```bash
nmap -O 192.168.1.10
```

---

## Aggressive Scan

```bash
nmap -A 192.168.1.10
```

---

## Scan Specific Ports

```bash
nmap -p 22,80,443 192.168.1.10
```

---

# Common Default Ports

| Port | Protocol |
|------|----------|
| 20 | FTP Data |
| 21 | FTP |
| 22 | SSH / SFTP |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 67 | DHCP Server |
| 68 | DHCP Client |
| 69 | TFTP |
| 80 | HTTP |
| 110 | POP3 |
| 123 | NTP |
| 143 | IMAP |
| 161 | SNMP |
| 162 | SNMP Trap |
| 389 | LDAP |
| 443 | HTTPS |
| 445 | SMB |
| 465 | SMTPS |
| 587 | SMTP Submission |
| 636 | LDAPS |
| 993 | IMAPS |
| 995 | POP3S |
| 3389 | RDP |

---

# Memory Tricks

## Secure Protocols

Remember:

> **If it starts with "S", it usually means Secure.**

Examples:

- SSH
- SFTP
- SMTPS
- POP3S
- IMAPS

HTTPS is also secure because it uses TLS/SSL.

---

## Easy Way to Remember

HTTP → Web

HTTPS → Secure Web

FTP → Files

SFTP → Secure Files

SSH → Secure Remote Login

Telnet → Old Remote Login

SMTP → Send Email

POP3 → Download Email

IMAP → Sync Email

DNS → Website Names

DHCP → IP Address Assignment

SNMP → Device Monitoring

SMB → File Sharing

NTP → Time Synchronization

---

# Interview Questions

### What is a protocol?

A protocol is a set of rules that defines how devices communicate over a network.

---

### Which protocol is used for secure web browsing?

HTTPS

---

### Which protocol converts domain names into IP addresses?

DNS

---

### Which protocol automatically assigns IP addresses?

DHCP

---

### Which protocol is used for secure remote login?

SSH

---

### Which protocol is insecure for remote login?

Telnet

---

### Which protocol sends emails?

SMTP

---

### Which protocols receive emails?

POP3 and IMAP

---

### Which protocol shares files in Windows?

SMB

---

### Which protocol synchronizes time?

NTP

---

### Which protocol is used for network monitoring?

SNMP

---

# Quick Cheat Sheet

| Protocol | Port | Main Purpose |
|----------|------|--------------|
| HTTP | 80 | Web |
| HTTPS | 443 | Secure Web |
| DNS | 53 | Name Resolution |
| DHCP | 67/68 | IP Assignment |
| FTP | 20/21 | File Transfer |
| SFTP | 22 | Secure File Transfer |
| SSH | 22 | Secure Remote Access |
| Telnet | 23 | Remote Access |
| SMTP | 25 | Send Email |
| POP3 | 110 | Download Email |
| IMAP | 143 | Synchronize Email |
| SNMP | 161 | Network Monitoring |
| LDAP | 389 | Directory Services |
| SMB | 445 | File Sharing |
| RDP | 3389 | Remote Desktop |
| NTP | 123 | Time Synchronization |

---

# Summary

Network protocols are the foundation of computer networking and cybersecurity. They define how devices communicate, exchange information, and provide services across local and global networks.

In this guide, we explored:

- What network protocols are
- Why protocols are important
- Core protocols (IP, TCP, UDP, ICMP, ARP)
- Web protocols (HTTP, HTTPS)
- Infrastructure protocols (DNS, DHCP)
- File transfer protocols (FTP, SFTP, TFTP)
- Remote access protocols (SSH, Telnet, RDP)
- Email protocols (SMTP, POP3, IMAP)
- Network service protocols (SMB, LDAP, SNMP, NTP)
- Common protocol attacks
- Wireshark filters
- Nmap commands
- Secure vs. insecure protocols
- Default ports
- Interview questions
- Quick revision cheat sheet

A solid understanding of these protocols is essential for networking, ethical hacking, penetration testing, malware analysis, digital forensics, and security operations. As you continue your cybersecurity journey, you'll encounter these protocols in tools like Wireshark, Nmap, Burp Suite, Metasploit, and during real-world security assessments.

---

# References

- RFC 791 – Internet Protocol (IP)
- RFC 793 – Transmission Control Protocol (TCP)
- RFC 768 – User Datagram Protocol (UDP)
- RFC 826 – Address Resolution Protocol (ARP)
- RFC 1035 – Domain Name System (DNS)
- RFC 959 – File Transfer Protocol (FTP)
- RFC 854 – Telnet
- RFC 4251 – Secure Shell (SSH)
- CompTIA Network+
- Cisco CCNA Study Guide
- Wireshark Documentation
- Nmap Official Documentation

---

⭐ **Thank you for reading!**

If you found these notes helpful, consider giving this repository a ⭐ and follow my cybersecurity journey as I continue exploring networking, Linux, ethical hacking, web security, penetration testing, and practical labs.
