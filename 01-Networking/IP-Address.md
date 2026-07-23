# IP Address

## Introduction

An **IP Address (Internet Protocol Address)** is a unique numerical identifier assigned to every device connected to a network. It allows devices to communicate with each other over local networks and the internet.

Think of an IP address like your home address. Just as a postal service needs your home address to deliver mail, computers need IP addresses to send and receive data.

---

# Why This Topic Matters

IP addresses are one of the most fundamental concepts in networking and cybersecurity.

Understanding IP addresses helps you:

- Learn how devices communicate
- Troubleshoot network problems
- Perform network scanning
- Understand penetration testing techniques
- Analyze network traffic
- Detect suspicious activities

Without IP addresses, the internet would not function.

---

# Learning Objectives

After completing this topic, you should be able to:

- Understand what an IP address is
- Differentiate between IPv4 and IPv6
- Identify public and private IP addresses
- Understand static and dynamic IP addresses
- Recognize loopback and localhost addresses
- View your IP address using operating system commands

---

# Key Concepts

| Term | Definition |
|------|------------|
| IP Address | A unique number assigned to a device on a network |
| IPv4 | 32-bit IP address format |
| IPv6 | 128-bit IP address format |
| Public IP | Address visible on the internet |
| Private IP | Address used inside local networks |
| Static IP | Fixed IP address |
| Dynamic IP | IP address assigned automatically by DHCP |
| Loopback Address | Special address used for testing the local machine |

---

# Detailed Explanation

## What is an IP Address?

An IP address uniquely identifies a device connected to a network.

Examples of devices with IP addresses:

- Laptop
- Smartphone
- Server
- Printer
- Router
- Smart TV

Every time you browse a website, send an email, or watch YouTube, your device communicates using IP addresses.

---

## IPv4

IPv4 is the most common version of the Internet Protocol.

Characteristics:

- 32-bit address
- Four numbers separated by dots
- Each number ranges from 0 to 255

Example:

```
192.168.1.10
```

Another example:

```
8.8.8.8
```

IPv4 supports approximately **4.3 billion** unique addresses.

Due to the rapid growth of internet-connected devices, IPv4 addresses are becoming limited.

---

## IPv6

IPv6 was developed to solve the IPv4 address shortage.

Characteristics:

- 128-bit address
- Uses hexadecimal numbers
- Separated by colons

Example:

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

Advantages:

- Vast number of addresses
- Better scalability
- Improved routing efficiency
- Built-in support for modern networking features

---

## Public IP Address

A public IP address is assigned by an Internet Service Provider (ISP).

It is visible on the internet.

Example:

```
39.41.120.15
```

Websites communicate with your public IP address when you access them.

---

## Private IP Address

Private IP addresses are used inside homes, schools, and offices.

Common private IPv4 ranges:

```
10.0.0.0 – 10.255.255.255
```

```
172.16.0.0 – 172.31.255.255
```

```
192.168.0.0 – 192.168.255.255
```

Example:

```
192.168.1.100
```

Private IP addresses cannot be accessed directly from the internet.

---

## Static IP Address

A static IP address never changes unless manually modified.

Common uses:

- Web servers
- Email servers
- CCTV systems
- Network devices

Advantages:

- Stable connection
- Easy remote access

Disadvantages:

- Requires manual configuration
- May cost extra from an ISP

---

## Dynamic IP Address

A dynamic IP address is assigned automatically by a **DHCP (Dynamic Host Configuration Protocol)** server.

Most home internet connections use dynamic IP addresses.

Advantages:

- Automatic configuration
- Easier management
- Efficient use of IP addresses

---

## Loopback Address

The loopback address is used to test the local computer.

IPv4:

```
127.0.0.1
```

IPv6:

```
::1
```

Typing:

```
ping 127.0.0.1
```

checks whether the network stack on your computer is working correctly.

---

# Practical Examples

### Example 1

Home Network

```
Laptop
192.168.1.10

↓

Wi-Fi Router

↓

Internet

↓

Google Server
142.250.x.x
```

---

### Example 2

Office Network

```
PC 1 → 192.168.0.5

PC 2 → 192.168.0.8

Printer → 192.168.0.20

Router → 192.168.0.1
```

Each device has a unique IP address so data reaches the correct destination.

---

# Commands or Code Examples

## Windows

Display IP configuration:

```cmd
ipconfig
```

Explanation:

Displays your IP address, subnet mask, and default gateway.

---

Display detailed information:

```cmd
ipconfig /all
```

Explanation:

Shows detailed network configuration, including MAC address, DNS servers, and DHCP information.

---

## Linux

```bash
ip addr
```

Explanation:

Displays all network interfaces and their assigned IP addresses.

---

```bash
hostname -I
```

Explanation:

Displays the IP address assigned to the current system.

---

Test connectivity:

```bash
ping 8.8.8.8
```

Explanation:

Sends packets to Google's public DNS server to verify internet connectivity.

---

# Best Practices

- Keep network devices updated.
- Use secure Wi-Fi passwords.
- Do not expose unnecessary services to the internet.
- Understand the difference between public and private IP addresses.
- Regularly monitor your network for unknown devices.
- Learn to identify suspicious IP activity during security analysis.

---

# Common Mistakes

- Confusing public IP addresses with private IP addresses.
- Assuming every device has the same IP address.
- Forgetting that dynamic IP addresses can change.
- Ignoring IPv6 because IPv4 is more common.
- Misconfiguring static IP addresses, causing network conflicts.

---

# Summary

An IP address uniquely identifies a device on a network. It enables communication between computers, servers, routers, and other connected devices. IPv4 is still widely used, while IPv6 provides a much larger address space for the future. Understanding IP addressing is essential for networking, cybersecurity, and ethical hacking.

---

# Key Takeaways

- Every network device needs an IP address.
- IPv4 uses 32-bit addresses.
- IPv6 uses 128-bit addresses.
- Public IPs are internet-facing.
- Private IPs are used within local networks.
- Static IPs remain fixed.
- Dynamic IPs are assigned automatically by DHCP.
- Loopback addresses are used for local testing.

---

# Practice Questions

1. What is an IP address?
2. What is the difference between IPv4 and IPv6?
3. What is the purpose of a public IP address?
4. Why are private IP addresses used?
5. What is DHCP?
6. What is the loopback address in IPv4?
7. What command displays your IP address on Windows?
8. What command displays your IP address on Linux?
9. What is the difference between static and dynamic IP addresses?
10. Why is IPv6 important?

---

# Useful Resources

- RFC 791 (Internet Protocol)
- RFC 8200 (IPv6 Specification)
- Cisco Networking Academy
- Google Cybersecurity Professional Certificate
- IBM Ethical Hacking with Open Source Tools Professional Certificate
- TryHackMe Networking Fundamentals
