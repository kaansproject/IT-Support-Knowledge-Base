# DHCP Basics

## What is DHCP?

DHCP (Dynamic Host Configuration Protocol) is a network service that automatically assigns IP addresses and other network configuration settings to devices on a network.

Without DHCP, administrators would need to manually configure every device with an IP address.

---

## Why DHCP is Important

DHCP simplifies network administration by automatically providing:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server

This reduces configuration errors and saves time.

---

## How DHCP Works

When a device connects to a network, it requests an IP address from a DHCP server.

The DHCP process follows four steps known as **DORA**:

### Discover

The client broadcasts a request looking for a DHCP server.

### Offer

The DHCP server offers an available IP address.

### Request

The client requests to use the offered IP address.

### Acknowledge

The DHCP server confirms the assignment.

Example:

```text
Client → Discover
Server → Offer
Client → Request
Server → Acknowledge
```

---

## DHCP Components

### DHCP Server

A device or server that distributes IP addresses.

Examples:

* Windows Server DHCP
* Router DHCP Service

---

### DHCP Client

Any device requesting network settings.

Examples:

* Desktop Computer
* Laptop
* Smartphone
* Printer

---

## DHCP Lease

A lease is the amount of time an IP address is assigned to a device.

Example:

```text
Lease Duration: 8 Days
```

When the lease expires, the client must renew it.

---

## DHCP Scope

A DHCP scope defines the range of IP addresses available for assignment.

Example:

```text
192.168.1.100 - 192.168.1.200
```

Devices will receive addresses within this range.

---

## DHCP Reservation

A reservation ensures that a specific device always receives the same IP address.

Commonly used for:

* Printers
* Servers
* Network Devices

Example:

```text
Printer MAC Address:
00-1A-2B-3C-4D-5E

Reserved IP:
192.168.1.50
```

---

## DHCP Advantages

* Automatic configuration
* Reduced administrative workload
* Fewer IP conflicts
* Easy device deployment
* Centralized management

---

## Common DHCP Issues

### No IP Address Assigned

Symptoms:

```text
Limited Connectivity
No Internet Access
```

Possible Causes:

* DHCP Server Offline
* Network Cable Issue
* Wireless Connectivity Problem

---

### APIPA Address

When DHCP fails, Windows may assign an APIPA address.

Example:

```text
169.254.x.x
```

This indicates that the computer could not obtain an IP address from a DHCP server.

---

### IP Address Conflict

Occurs when two devices attempt to use the same IP address.

Possible Causes:

* Incorrect static IP configuration
* Duplicate IP assignment

---

## Useful DHCP Commands

### View Network Configuration

```cmd
ipconfig /all
```

Displays DHCP information and lease details.

---

### Release Current IP Address

```cmd
ipconfig /release
```

Removes the current DHCP-assigned IP address.

---

### Request a New IP Address

```cmd
ipconfig /renew
```

Requests a new IP address from the DHCP server.

---

## Example Help Desk Scenario

**Issue:**

User cannot access the network.

**Troubleshooting Steps:**

1. Check physical network connection.
2. Run:

```cmd
ipconfig /all
```

3. Verify that DHCP is enabled.
4. Check for a 169.254.x.x address.
5. Run:

```cmd
ipconfig /release
ipconfig /renew
```

6. Verify connectivity by pinging the default gateway.

---

## Summary

DHCP automatically provides network configuration information to devices. Understanding DHCP concepts such as DORA, leases, scopes, reservations, and troubleshooting techniques is essential for IT Support and System Administration roles.
