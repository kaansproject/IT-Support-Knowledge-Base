# TCP/IP Fundamentals

## What is TCP/IP?

TCP/IP (Transmission Control Protocol / Internet Protocol) is the standard communication protocol used on modern networks and the Internet.

It defines how devices communicate, send data, and receive data across networks.

Without TCP/IP, computers would not be able to communicate with each other.

---

## What is an IP Address?

An IP address is a unique identifier assigned to a device on a network.

Think of it as a home address for a computer.

Example:

```text
192.168.1.100
```

Every device connected to a network requires an IP address.

---

## IPv4 vs IPv6

### IPv4

IPv4 uses 32-bit addresses.

Example:

```text
192.168.1.100
```

Characteristics:

* Most commonly used
* Approximately 4.3 billion addresses available

---

### IPv6

IPv6 uses 128-bit addresses.

Example:

```text
2001:0db8:85a3::8a2e:0370:7334
```

Characteristics:

* Much larger address space
* Designed to replace IPv4
* Better scalability for future networks

---

## Public and Private IP Addresses

### Public IP

A public IP address is accessible from the Internet.

Assigned by:

* Internet Service Providers (ISPs)

Example:

```text
85.100.25.10
```

---

### Private IP

Private IP addresses are used inside local networks.

Common private ranges:

```text
10.0.0.0 - 10.255.255.255

172.16.0.0 - 172.31.255.255

192.168.0.0 - 192.168.255.255
```

Example:

```text
192.168.1.100
```

Private IP addresses cannot be directly accessed from the Internet.

---

## Subnet Mask

A subnet mask determines which portion of an IP address represents the network and which portion represents the host.

Example:

```text
IP Address: 192.168.1.100
Subnet Mask: 255.255.255.0
```

This means:

```text
Network: 192.168.1.0
Host: 100
```

---

## Default Gateway

A default gateway is the device that allows computers to communicate with other networks.

In most environments, the default gateway is the router.

Example:

```text
Default Gateway:
192.168.1.1
```

If the gateway is unavailable, Internet access may fail.

---

## DNS Server

DNS servers translate domain names into IP addresses.

Example:

```text
google.com → 142.250.190.78
```

Popular DNS servers:

```text
Google DNS:
8.8.8.8

Cloudflare DNS:
1.1.1.1
```

---

## TCP vs UDP

### TCP (Transmission Control Protocol)

TCP is connection-oriented and reliable.

Features:

* Error checking
* Data retransmission
* Ordered delivery

Common Uses:

* Web Browsing (HTTP/HTTPS)
* Email
* File Transfers

Example Ports:

```text
80   HTTP
443  HTTPS
```

---

### UDP (User Datagram Protocol)

UDP is connectionless and faster.

Features:

* No delivery guarantee
* Lower overhead
* Faster transmission

Common Uses:

* Online Gaming
* Video Streaming
* Voice Calls (VoIP)
* DNS Queries

Example Port:

```text
53 DNS
```

---

## Basic Network Configuration Example

```text
IP Address:      192.168.1.100
Subnet Mask:     255.255.255.0
Default Gateway: 192.168.1.1
DNS Server:      8.8.8.8
```

This configuration allows a device to communicate within the local network and access Internet resources.

---

## Useful Networking Commands

### View Network Configuration

```cmd
ipconfig
```

---

### View Detailed Configuration

```cmd
ipconfig /all
```

---

### Test Connectivity

```cmd
ping google.com
```

---

### Display Routing Information

```cmd
route print
```

---

### Check Active Connections

```cmd
netstat -an
```

---

## Example Help Desk Scenario

**Issue:**

User cannot access websites.

**Troubleshooting Steps:**

1. Verify IP configuration.

```cmd
ipconfig /all
```

2. Confirm a valid IP address exists.
3. Verify the default gateway.
4. Ping the gateway.

```cmd
ping 192.168.1.1
```

5. Ping a public IP address.

```cmd
ping 8.8.8.8
```

6. Test DNS resolution.

```cmd
nslookup google.com
```

7. Resolve any network configuration issues found.

---

## Summary

TCP/IP is the foundation of modern networking. Understanding IP addresses, subnet masks, gateways, DNS servers, and the differences between TCP and UDP is essential for IT Support, Help Desk, and System Administration roles.
