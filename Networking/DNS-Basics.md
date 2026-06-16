# DNS Basics

## What is DNS?

DNS (Domain Name System) translates human-readable domain names into IP addresses.

Example:

google.com → 142.250.190.14

Without DNS, users would need to remember IP addresses instead of domain names.

---

## How DNS Works

1. User enters a domain name.
2. The request is sent to a DNS resolver.
3. The resolver contacts DNS servers.
4. The IP address is returned.
5. The browser connects to the destination server.

---

## Common DNS Record Types

### A Record

Maps a domain name to an IPv4 address.

Example:

example.com → 192.168.1.10

### AAAA Record

Maps a domain name to an IPv6 address.

### MX Record

Specifies mail servers responsible for email delivery.

### CNAME Record

Creates an alias for another domain.

---

## Troubleshooting DNS Issues

### Verify DNS Resolution

```cmd
nslookup google.com
```

### Test Network Connectivity

```cmd
ping 8.8.8.8
```

### Flush DNS Cache

```cmd
ipconfig /flushdns
```

### Display Current DNS Settings

```cmd
ipconfig /all
```

---

## Common DNS Problems

- Incorrect DNS server configuration
- DNS cache corruption
- Missing DNS records
- Network connectivity issues

---

## Key Takeaways

- DNS translates names into IP addresses.
- DNS is essential for web browsing and email delivery.
- nslookup is a common troubleshooting tool.