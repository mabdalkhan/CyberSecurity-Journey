---

# 🌍 Hypertext Transfer Protocol (HTTP)

## What is HTTP?

**HTTP (Hypertext Transfer Protocol)** is the protocol used to transfer web pages between a web browser and a web server.

Whenever you visit a website, your browser sends an HTTP request to the server, and the server responds with the requested webpage.

Simply put:

> **HTTP is the language that web browsers and web servers use to communicate.**

---

## Real-Life Example

Imagine you're in a restaurant.

- You (Browser) place an order.
- The waiter (HTTP) takes your order.
- The kitchen (Web Server) prepares the food.
- The waiter brings your food back.

The waiter doesn't cook the food.

He simply carries requests and responses.

HTTP works the same way.

---

## Default Port

| Protocol | Port |
|----------|------|
| HTTP | 80 |

---

## Common HTTP Methods

| Method | Purpose |
|---------|---------|
| GET | Retrieve data |
| POST | Send data |
| PUT | Update data |
| DELETE | Delete data |
| PATCH | Modify part of data |

---

## Example

When you visit

```
http://example.com
```

Your browser sends:

```
GET / HTTP/1.1
Host: example.com
```

The server replies:

```
HTTP/1.1 200 OK
```

along with the webpage.

---

## Is HTTP Secure?

❌ No.

HTTP sends data in **plain text**.

Anyone intercepting the traffic can read:

- Usernames
- Passwords
- Cookies
- Messages

---

## Cybersecurity Perspective

Attackers may exploit HTTP traffic through:

- Packet sniffing
- Session hijacking
- Man-in-the-Middle (MITM) attacks

Because HTTP is not encrypted, it should not be used for sensitive information.

---

# 🔒 Hypertext Transfer Protocol Secure (HTTPS)

## What is HTTPS?

HTTPS is the secure version of HTTP.

It combines:

- HTTP
- SSL/TLS Encryption

HTTPS encrypts the communication between your browser and the web server.

Even if someone intercepts the traffic, they cannot easily read the data.

---

## Default Port

| Protocol | Port |
|----------|------|
| HTTPS | 443 |

---

## Real-Life Example

Imagine sending a postcard.

Anyone who handles it can read your message.

That's HTTP.

Now imagine placing the same message inside a locked box.

Only the sender and receiver have the key.

That's HTTPS.

---

## Advantages

✅ Encryption

✅ Authentication

✅ Data Integrity

---

## Uses

- Online Banking
- Gmail
- Facebook
- Amazon
- Government Websites
- Online Shopping

---

## Cybersecurity Perspective

Ethical hackers often examine:

- SSL Certificates
- Weak TLS versions
- Certificate misconfigurations

HTTPS protects confidentiality but does **not** guarantee a website is trustworthy.

Always verify the website's legitimacy.

---

# 🌍 Domain Name System (DNS)

## What is DNS?

DNS stands for **Domain Name System**.

Humans remember names.

Computers remember numbers (IP addresses).

DNS translates domain names into IP addresses.

---

## Real-Life Example

Think of DNS as the contacts list on your phone.

You tap:

```
Mom
```

instead of remembering:

```
+92-300-1234567
```

Similarly,

Instead of remembering:

```
142.250.183.206
```

you simply type:

```
google.com
```

DNS performs the translation.

---

## Default Port

| Protocol | Port |
|----------|------|
| DNS | 53 |

Uses:

- UDP (most queries)
- TCP (large responses and zone transfers)

---

## DNS Lookup Process

```
Browser

↓

DNS Resolver

↓

Root Server

↓

TLD Server (.com)

↓

Authoritative DNS Server

↓

IP Address Returned

↓

Website Opens
```

---

## Cybersecurity Perspective

Common DNS attacks include:

- DNS Spoofing
- DNS Cache Poisoning
- DNS Tunneling
- DNS Amplification

---

# 📡 Dynamic Host Configuration Protocol (DHCP)

## What is DHCP?

DHCP automatically assigns IP addresses to devices.

Without DHCP,

every device would need manual IP configuration.

---

## Real-Life Example

Imagine checking into a hotel.

The receptionist automatically assigns you a room number.

You don't choose the room yourself.

DHCP works in exactly the same way.

---

## Default Ports

| Protocol | Client | Server |
|----------|-------|--------|
| DHCP | 68 | 67 |

---

## DHCP Process (DORA)

### D – Discover

The device asks:

> "Is there any DHCP server?"

---

### O – Offer

The DHCP server replies:

> "Yes, here is an available IP address."

---

### R – Request

The device says:

> "I would like to use this IP address."

---

### A – Acknowledge

The DHCP server confirms the assignment.

The device can now communicate on the network.

---

## Cybersecurity Perspective

Possible attacks:

- Rogue DHCP Server
- DHCP Starvation Attack

---

# 📂 File Transfer Protocol (FTP)

## What is FTP?

FTP stands for **File Transfer Protocol**.

It is used to transfer files between computers.

---

## Default Ports

| Port | Purpose |
|------|----------|
| 21 | Control Connection |
| 20 | Data Connection |

---

## Uses

- Uploading websites
- Downloading files
- Server backups

---

## Problem

FTP sends:

- Username
- Password
- Files

in plain text.

This makes it insecure.

---

## Cybersecurity Perspective

Common attacks:

- Credential sniffing
- Brute-force attacks
- Anonymous FTP abuse

Today, secure alternatives such as **SFTP** are preferred.

---

# 🔐 Secure File Transfer Protocol (SFTP)

## What is SFTP?

SFTP stands for **Secure File Transfer Protocol**.

Unlike FTP,

SFTP encrypts all communication using SSH.

---

## Default Port

| Protocol | Port |
|----------|------|
| SFTP | 22 |

---

## Advantages

✅ Encrypted communication

✅ Secure authentication

✅ Secure file transfers

---

# 📁 Trivial File Transfer Protocol (TFTP)

## What is TFTP?

TFTP is a simplified version of FTP.

It is mainly used for:

- Network device configuration
- Firmware updates
- Boot files

---

## Default Port

| Protocol | Port |
|----------|------|
| TFTP | 69 |

---

## Characteristics

- No authentication
- No encryption
- Very lightweight
- Fast

---

## Cybersecurity Perspective

Because it has no authentication or encryption, TFTP should only be used in trusted internal networks.

---

# 📋 Comparison Table

| Protocol | Port | Secure | Purpose |
|----------|------|---------|----------|
| HTTP | 80 | ❌ | Web Browsing |
| HTTPS | 443 | ✅ | Secure Web Browsing |
| DNS | 53 | ❌ | Name Resolution |
| DHCP | 67/68 | ❌ | IP Assignment |
| FTP | 20/21 | ❌ | File Transfer |
| SFTP | 22 | ✅ | Secure File Transfer |
| TFTP | 69 | ❌ | Lightweight File Transfer |

---

# 💡 Quick Revision

- **HTTP** → Opens websites.
- **HTTPS** → Opens websites securely.
- **DNS** → Converts names into IP addresses.
- **DHCP** → Assigns IP addresses automatically.
- **FTP** → Transfers files (not secure).
- **SFTP** → Transfers files securely.
- **TFTP** → Simple file transfer for trusted networks.

---

➡️ **Next Part:** We'll cover **SSH, Telnet, SMTP, POP3, IMAP, SMB, LDAP, SNMP, NTP, RDP**, along with common attacks, Wireshark examples, and Nmap scanning examples.
