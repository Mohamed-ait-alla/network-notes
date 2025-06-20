# Subnet Mask
### 1. What is Subnetting?
**Subnetting** is the process of **dividing a larger IP network** into smaller, more manageable **subnetworks (subnets)**. This allows network administrators to:

- Organize devices into logical groups
- Improve security by isolating traffic
- Optimize IP address usage, especially in large organizations.

### 2. What is a Subnet Mask?
##### Description
**Subnet Mask** is a 32-bit number (ex. 255.255.255.0) used in IPv4 networking that identifies the network and host portions of an IP address.
- **The network portion** identifies which network the IP belongs to.
- **The host portion** identifies the specific device within that network.

##### Purpose of Subnet Mask
Subnet masks help routers and other network devices **determine whether an IP address is on the same local network** or **needs to be routed to a different network**.

##### How It Works?
Consider we have this subnet mask **255.255.255.0**, first of all, we need to convert it to binary version, After convertion we have: **11111111.11111111.11111111.00000000**. ***1's*** in this format identify the **network bits** that we can not touch, and ***0's*** define the assignable host range, In this case we have 8 zeros, so **2^8 - 2** (2 reserved IPs **Broadcast and Network** IPs) will gives us **254 Usable IPs**.<br>
For example, if we have an IP address **192.168.1.0**, and it's subnet mask is **255.255.255.0**, the process of subnetting will be that:
- `192.168.1.1` to `192.168.1.254` → **valid IPs for devices**
- `192.168.1.0` → **network address**
- `192.168.1.255` → **broadcast address**

> **Note!:** Every valid mask is **contiguous ones** followed by **zeros**