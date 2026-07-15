---

# 🔐 Secure Shell (SSH)

## What is SSH?

**SSH (Secure Shell)** is a protocol used to securely connect to and manage another computer over a network.

Unlike Telnet, SSH encrypts all communication, making it the preferred protocol for remote administration.

System administrators, cloud engineers, and ethical hackers use SSH every day to securely access Linux servers.

---

## Real-Life Example

Imagine your house has a smart lock that only opens with your unique fingerprint.

Only authorized people can enter.

SSH works in a similar way by allowing only authenticated users to access a remote system securely.

---

## Default Port

| Protocol | Port |
|----------|------|
| SSH | 22 |

---

## Common Uses

- Remote server management
- Secure file transfer (SFTP)
- Running commands remotely
- Cloud server administration
- Git over SSH

---

## Advantages

✅ Encrypted communication

✅ Secure authentication

✅ Supports public/private key authentication

✅ Protects usernames and passwords

---

## Cybersecurity Perspective

Ethical hackers often test SSH for:

- Weak passwords
- Brute-force attacks
- Default credentials
- Outdated SSH versions
- Misconfigured SSH settings

---

# 📡 Telnet

## What is Telnet?

Telnet is an older protocol used to remotely access another computer.

Unlike SSH, **Telnet does not encrypt data**.

Everything—including usernames and passwords—is sent in plain text.

---

## Default Port

| Protocol | Port |
|----------|------|
| Telnet | 23 |

---

## Why Is Telnet Insecure?

Anyone monitoring the network can capture:

- Username
- Password
- Commands
- Data

Because of this, Telnet is rarely used today except in labs or for testing legacy devices.

---

## SSH vs Telnet

| Feature | SSH | Telnet |
|----------|-----|---------|
| Encryption | ✅ Yes | ❌ No |
| Secure Login | ✅ | ❌ |
| Recommended | ✅ Yes | ❌ No |
| Port | 22 | 23 |

---

# 🖥️ Remote Desktop Protocol (RDP)

## What is RDP?

RDP stands for **Remote Desktop Protocol**.

It allows you to control another computer using a graphical interface.

Instead of only typing commands, you can interact with the remote computer as if you were sitting in front of it.

---

## Default Port

| Protocol | Port |
|----------|------|
| RDP | 3389 |

---

## Common Uses

- Remote technical support
- Managing Windows servers
- Working from home
- Remote administration

---

## Cybersecurity Perspective

RDP is a common target for attackers because it is often exposed to the Internet.

Common attacks include:

- Password brute-force attacks
- Credential stuffing
- Exploiting unpatched RDP vulnerabilities

To improve security:

- Use strong passwords
- Enable Multi-Factor Authentication (MFA)
- Restrict access with a firewall
- Use a VPN for remote access
- Disable RDP if it isn't needed

---

# 📧 Simple Mail Transfer Protocol (SMTP)

## What is SMTP?

SMTP stands for **Simple Mail Transfer Protocol**.

It is responsible for **sending emails**.

Whenever you send an email, SMTP delivers it from your email client to the mail server and then to the recipient's mail server.

---

## Default Ports

| Port | Purpose |
|------|----------|
| 25 | Standard SMTP |
| 587 | Secure Mail Submission |
| 465 | SMTPS (Encrypted) |

---

## Real-Life Example

Imagine sending a letter.

SMTP is like the postal service that takes your letter from your mailbox and delivers it to the recipient's city.

---

## Cybersecurity Perspective

Attackers may abuse SMTP for:

- Spam campaigns
- Email spoofing
- Phishing attacks

Organizations often implement SPF, DKIM, and DMARC to reduce email spoofing.

---

# 📥 Post Office Protocol Version 3 (POP3)

## What is POP3?

POP3 is used to **receive emails**.

It downloads emails from the mail server to your device.

In many cases, emails are removed from the server after downloading.

---

## Default Ports

| Port | Purpose |
|------|----------|
| 110 | POP3 |
| 995 | POP3 Secure (POP3S) |

---

## Best For

- Accessing email from a single device
- Offline email reading

---

## Limitation

If you use multiple devices, your emails may not stay synchronized.

---

# 📬 Internet Message Access Protocol (IMAP)

## What is IMAP?

IMAP is another protocol used to receive emails.

Unlike POP3, IMAP keeps emails stored on the mail server.

This allows multiple devices to stay synchronized.

---

## Default Ports

| Port | Purpose |
|------|----------|
| 143 | IMAP |
| 993 | IMAPS (Secure) |

---

## Example

You read an email on your phone.

Later, you open your laptop.

The email still appears because IMAP synchronizes with the mail server.

---

# POP3 vs IMAP

| Feature | POP3 | IMAP |
|----------|------|------|
| Downloads Emails | ✅ | ❌ |
| Keeps Emails on Server | ❌ | ✅ |
| Multiple Devices | ❌ | ✅ |
| Best Choice Today | ❌ | ✅ |

---

# 📂 Server Message Block (SMB)

## What is SMB?

SMB stands for **Server Message Block**.

It allows computers to share:

- Files
- Printers
- Folders
- Network resources

SMB is commonly used in Windows networks.

---

## Default Port

| Protocol | Port |
|----------|------|
| SMB | 445 |

---

## Cybersecurity Perspective

SMB has been targeted by several major cyberattacks.

Examples include:

- EternalBlue
- WannaCry ransomware
- SMB Relay attacks

To reduce risk:

- Disable SMBv1
- Keep systems updated
- Restrict SMB access
- Use strong authentication

---

# 📖 Lightweight Directory Access Protocol (LDAP)

## What is LDAP?

LDAP stands for **Lightweight Directory Access Protocol**.

It is used to access and manage directory services such as users, groups, and permissions.

LDAP is commonly used with Microsoft Active Directory.

---

## Default Ports

| Port | Purpose |
|------|----------|
| 389 | LDAP |
| 636 | LDAPS (Secure) |

---

## Uses

- User authentication
- Group management
- Active Directory queries
- Enterprise user management

---

## Cybersecurity Perspective

LDAP attacks include:

- LDAP Injection
- Anonymous LDAP Enumeration
- Weak authentication

---

# 📊 Simple Network Management Protocol (SNMP)

## What is SNMP?

SNMP is used to monitor and manage network devices.

Network administrators use SNMP to monitor:

- Routers
- Switches
- Firewalls
- Servers
- Printers

---

## Default Ports

| Port | Purpose |
|------|----------|
| 161 | SNMP |
| 162 | SNMP Trap |

---

## Cybersecurity Perspective

Older SNMP versions use weak community strings like:

```
public
private
```

Attackers often try these default values to gather information about network devices.

Always use SNMPv3 when possible because it supports authentication and encryption.

---

# ⏰ Network Time Protocol (NTP)

## What is NTP?

NTP stands for **Network Time Protocol**.

It synchronizes the clocks of computers and network devices.

Accurate time is important because security logs rely on correct timestamps.

---

## Default Port

| Protocol | Port |
|----------|------|
| NTP | 123 |

---

## Why Is NTP Important?

Imagine investigating a cyberattack.

If one server's clock is five minutes ahead and another is three minutes behind, the logs become difficult to correlate.

NTP keeps all devices synchronized, making troubleshooting and forensic investigations much easier.

---

# 📋 Protocol Summary

| Protocol | Port | Secure | Primary Purpose |
|----------|------|---------|-----------------|
| SSH | 22 | ✅ | Secure Remote Access |
| Telnet | 23 | ❌ | Remote Access |
| RDP | 3389 | ⚠️ Can Be Secured | Remote Desktop |
| SMTP | 25/465/587 | ✅ (465/587) | Send Email |
| POP3 | 110/995 | ✅ (995) | Receive Email |
| IMAP | 143/993 | ✅ (993) | Synchronize Email |
| SMB | 445 | ⚠️ Depends on Configuration | File Sharing |
| LDAP | 389/636 | ✅ (636) | Directory Services |
| SNMP | 161/162 | ✅ (v3) | Network Management |
| NTP | 123 | ❌ | Time Synchronization |

---

# 📝 Key Takeaways

- **SSH** is the secure choice for remote administration.
- **Telnet** is outdated and insecure.
- **RDP** provides remote graphical access to Windows systems.
- **SMTP** sends emails.
- **POP3** downloads emails.
- **IMAP** keeps emails synchronized across devices.
- **SMB** shares files and printers across networks.
- **LDAP** manages users and directories.
- **SNMP** monitors network devices.
- **NTP** keeps system clocks synchronized.

---

➡️ **Next Part:** We'll cover **protocol attacks, secure vs insecure protocols, Wireshark examples, Nmap scanning, protocol comparison charts, interview questions, cheat sheet, and final revision notes.**
