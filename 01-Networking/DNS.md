# 🌐 Domain Name System (DNS)

## What is DNS?

DNS stands for **Domain Name System**. It is a service that converts a website name (domain name) into an IP address. You can think of DNS as the **phonebook of the Internet**.

Humans remember names easily, but computers communicate using numbers called IP addresses.

For example:

```text
google.com
```

DNS converts it into something like:

```text
142.250.190.14
```

Your browser uses this IP address to connect to Google's server.

Without DNS, every time you wanted to visit a website, you would need to remember its IP address.

---

## Why Do We Need DNS?

Imagine you have 500 contacts on your phone.

Do you remember everyone's phone number?

Probably not.

Instead, you save their names.

For example:

```text
Ali → +92xxxxxxxxxx
Ahmed → +92xxxxxxxxxx
Sara → +92xxxxxxxxxx
```

When you tap **Ali**, your phone automatically finds his number.

DNS works in exactly the same way.

```text
google.com
        ↓
142.250.190.14
```

Instead of remembering numbers, we remember website names.

---

## How DNS Works

Let's say you type:

```text
www.github.com
```

inside your browser.

The following steps happen in the background.

### Step 1

You type the website name.

```text
www.github.com
```

### Step 2

Your browser checks if it already knows the IP address.

If it is stored in the cache, it uses it immediately.

If not, it asks a DNS Resolver.

### Step 3

The DNS Resolver starts searching for the correct IP address.

### Step 4

It contacts the Root DNS Server.

The Root Server does not know the exact IP address.

It simply says,

> "Ask the .com server."

### Step 5

The Resolver contacts the **.com TLD Server**.

The TLD Server replies,

> "Ask GitHub's Authoritative DNS Server."

### Step 6

The Resolver contacts GitHub's Authoritative Server.

This server knows the correct IP address.

Example:

```text
140.82.121.4
```

### Step 7

The Resolver sends the IP address back to your browser.

### Step 8

Your browser connects to GitHub's web server.

Finally,

GitHub opens on your screen.

All of this usually happens in less than one second.

---

## DNS Servers

There are four main DNS servers.

### Recursive Resolver

This is the first server your computer contacts.

Its job is to find the correct IP address for you.

You can think of it as a helper.

---

### Root Server

The Root Server is the starting point of DNS.

It tells the Resolver where to go next.

Example:

```text
Ask the .com server.
```

---

### TLD Server

TLD means **Top Level Domain**.

Examples are:

```text
.com
.net
.org
.edu
.pk
```

The TLD Server tells the Resolver which server manages that domain.

---

### Authoritative DNS Server

This server stores the actual DNS records.

It gives the final answer.

Example:

```text
google.com

↓

142.250.190.14
```

---

## DNS Records

DNS stores different types of records.

### A Record

Maps a domain name to an IPv4 address.

Example:

```text
google.com

↓

142.250.190.14
```

---

### AAAA Record

Maps a domain name to an IPv6 address.

It works like the A Record but for IPv6.

---

### CNAME Record

CNAME means **Canonical Name**.

It creates an alias for another domain.

Example:

```text
www.example.com

↓

example.com
```

---

### MX Record

MX stands for **Mail Exchange**.

It tells email servers where to send emails.

Example:

```text
gmail.com
```

uses MX records to receive emails.

---

### NS Record

NS stands for **Name Server**.

It tells which DNS server is responsible for a domain.

---

### TXT Record

TXT records store text information.

They are commonly used for:

- Domain verification
- Email security
- SPF
- DKIM

---

### PTR Record

PTR records perform reverse lookups.

Instead of:

```text
Name → IP
```

they do:

```text
IP → Name
```

---

## DNS Cache

DNS stores recently visited websites in memory.

This is called **DNS Cache**.

Example:

The first time you visit:

```text
google.com
```

DNS searches for the IP address.

The second time,

the IP is already saved.

The website opens much faster.

---

## DNS Ports

DNS mainly uses:

```text
UDP Port 53
```

because it is fast.

Sometimes DNS uses:

```text
TCP Port 53
```

for large responses and zone transfers.

---

## Common DNS Attacks

### DNS Spoofing

The attacker sends a fake DNS response.

Example:

You type:

```text
facebook.com
```

Instead of opening Facebook,

you are redirected to a fake website.

---

### DNS Cache Poisoning

The attacker inserts fake records into the DNS cache.

Now every user receives the fake IP address.

This can steal usernames and passwords.

---

### DNS Amplification

Attackers use DNS servers to perform DDoS attacks.

A very small request generates a very large response.

Thousands of responses flood the victim.

---

### DNS Tunneling

Attackers hide data inside DNS traffic.

This technique is used for:

- Data theft
- Malware communication
- Bypassing firewalls

---

## DNS in Ethical Hacking

DNS is very useful during reconnaissance.

Ethical hackers collect information such as:

- IP addresses
- Subdomains
- Mail servers
- Name servers
- Public DNS records

Useful tools include:

```bash
nslookup google.com
```

```bash
dig google.com
```

```bash
host google.com
```

```bash
dnsenum example.com
```

```bash
dnsrecon -d example.com
```

These tools help security professionals understand how a target domain is configured.

---

## Simple Example

Imagine you want to visit YouTube.

You type:

```text
youtube.com
```

DNS finds its IP address.

Your browser connects to YouTube's server.

The video starts playing.

Without DNS, you would need to remember a long IP address every time.

That is why DNS is one of the most important services on the Internet. Every website you visit depends on DNS to find the correct server quickly and accurately.
