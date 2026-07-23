# MAC Address

## Introduction

A **MAC (Media Access Control) Address** is a unique hardware identifier assigned to a network interface card (NIC). It is mainly used for communication within a Local Area Network (LAN).

## Why This Topic Matters

- Identifies devices on a network.
- Enables communication between devices on the same LAN.
- Used in network troubleshooting and security.
- Helps understand how Ethernet and Wi-Fi networks operate.

## Learning Objectives

- Understand what a MAC address is.
- Learn its structure and purpose.
- Differentiate MAC and IP addresses.
- View a device's MAC address.

## Key Concepts

- **MAC Address:** Physical hardware address.
- **NIC:** Network Interface Card.
- **LAN:** Local Area Network.
- **Vendor Prefix (OUI):** First 24 bits identify the manufacturer.
- **Device Identifier:** Last 24 bits uniquely identify the device.

## Explanation

A MAC address is a **48-bit (6-byte)** hexadecimal value, usually written like:

```
00:1A:2B:3C:4D:5E
```

Unlike an IP address, a MAC address is used only for communication inside the local network (Layer 2 of the OSI Model).

```mermaid
flowchart LR
A[Device A] -->|Uses MAC Address| S[Switch]
S -->|Forwards Frame| B[Device B]
```

## Practical Example

A laptop sends data to a printer on the same Wi-Fi network. The switch/router uses the printer's MAC address to deliver the data to the correct device.

## Commands

### Windows

```cmd
ipconfig /all
```

Displays the **Physical Address** (MAC address).

### Linux

```bash
ip link
```

Shows MAC addresses of all network interfaces.

### Linux (Alternative)

```bash
ifconfig
```

Displays network interface details (if installed).

> [!TIP]
> MAC addresses are useful for identifying devices during network troubleshooting.

> [!NOTE]
> MAC addresses can be changed temporarily through MAC spoofing.

> [!WARNING]
> A MAC address alone does not provide security and should not be relied upon for authentication.

## Best Practices

- Record MAC addresses of important devices.
- Use MAC filtering only as a basic security layer.
- Verify device MAC addresses during troubleshooting.

## Common Mistakes

- Confusing MAC addresses with IP addresses.
- Assuming MAC addresses are always permanent.
- Believing MAC filtering alone secures a network.

## Summary

A MAC address uniquely identifies a network interface on a local network. It enables devices to communicate efficiently within a LAN and plays a key role in networking fundamentals.

## Key Takeaways

- MAC = Physical hardware address.
- Length: 48 bits (6 bytes).
- Written in hexadecimal.
- Operates at OSI Layer 2.
- Different from an IP address.

## Practice Questions

1. What does MAC stand for?
2. How many bits are in a MAC address?
3. Which OSI layer uses MAC addresses?
4. What command displays a MAC address in Windows?
5. What is the difference between a MAC and an IP address?

## Useful Resources

- IEEE 802 Standards
- Cisco Networking Academy
- Microsoft Networking Documentation

## Suggested Next Topic

**ARP (Address Resolution Protocol)**
