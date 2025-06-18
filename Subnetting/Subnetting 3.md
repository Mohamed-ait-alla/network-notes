# Private IP Addresses and NAT

### Overview
IPv4 provides about 4.3 billion unique addresses, but with the **rapid growth of internet-connected devices**, we are **running out**. Since public IP addresses must be **globally unique** to ensure proper communication across networks, their limited supply has become a major challenge for the internet. This is where **Private IP addresses and NAT solutions comes in**.

### What is a Private IP Address
Is a unique number assigned to devices within a local network. They are reserved for use within **internal networks only**, and they are **not routable on the public internet**, which means multiple private networks can reuse the same ranges without conflict.
##### Private IP Addresses Ranges (RFC 1918)
| IP Class | Private IP Range          | Subnet Mask       | CIDR Notation   |
|----------|---------------------------|-------------------|-----------------|
| Class A  | 10.0.0.0 – 10.255.255.255 | 255.0.0.0         | 10.0.0.0/8      |
| Class B  | 172.16.0.0 – 172.31.255.255| 255.240.0.0       | 172.16.0.0/12   |
| Class C  | 192.168.0.0 – 192.168.255.255| 255.255.0.0    | 192.168.0.0/16  |

> This why you see probably your home network IP starts with 192.168.0.x or 192.168.1.x, But **how these Private IPs reach the Internet?**

### Network Address Translation (NAT)
Is a process that enables multiple devices on a private network **to share a single public IP address** when communicating with the internet. Essentially, it **translates private IPs into a public IP address (often that of a router)** before sending data packets to the internet, and then translates them back upon receiving a response.

> Although solutions like private IP addresses and Network Address Translation (NAT) have **helped extend the life of IPv4**, they are **not enough to keep up** with the **incredible growth** in the number of internet-connected devices. Despite these workarounds, we are still running out of IPv4 addresses because the demand for globally unique IPs continues to rise. **To solve this**, **IPv6** was introduced. It offers a vastly **larger** address space, using 128-bit addresses instead of 32-bit. Allowing for an almost unlimited number of unique IPs. An IPv6 address looks like this: **2001:db8:85a3:8d3:1319:8a2e:370:7348**, and it **ensures that every device can have a unique, public IP address well into the future**.

