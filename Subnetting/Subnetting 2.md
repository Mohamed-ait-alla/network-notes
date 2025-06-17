# Challenges of IP Address allocation
> In this lesson, we gonna discover the history and challenges of IP address allocation, explaining how the internet nearly ran out of IPv4 addresses.

### IPv4 Address Exhaustion
 The **internet** initially utilized IPv4 addresses, which **provided approximately 4.3 billion** unique addresses (we get that number using 2^32). And **as the internet grew**, the demand for IP addresses surged, **leading to the exhaustion of available IPv4 addresses**.

### IP Address Classes
In the early days of networking, the internet needed a structured way to allocate IP addresses to organizations of varying sizes. A one-size-fits-all approach would waste address space, for example small networks would get more IPs than they needed, and large ones not enough.<br>
To solve this, **IP address classes** were introduced to divide the IPv4 space into chunks based on network size:
- **Class A** was for very large networks (e.g., governments, big corporations).
- **Class B** was for medium-sized organizations.
- **Class C** was for smaller networks like local businesses.
- **Class D** was reserved for multicast.
- **Class E** was reserved for experimental addresses, not for general use.
- **127.0.0.0/8** These are Loopback addresses used for testing and diagnostics, considred as our own addresses.

##### IP Address Classes Table
| IP Class | Starting IP      | Ending IP        | Default Subnet Mask | nb of Hosts per Network (approx.) | Purpose                       |
|----------|------------------|------------------|----------------------|----------------------------------|-------------------------------|
| A        | 1.0.0.0          | 126.255.255.255  | 255.0.0.0 (/8)       | 16,777,214                      | Very large networks           |
| B        | 128.0.0.0        | 191.255.255.255  | 255.255.0.0 (/16)    | 65,534                          | Medium-sized networks         |
| C        | 192.0.0.0        | 223.255.255.255  | 255.255.255.0 (/24)  | 254                             | Small networks                |
| D        | 224.0.0.0        | 239.255.255.255  | N/A                  | N/A                             | Multicast (not for hosts)     |
| E        | 240.0.0.0        | 255.255.255.255  | N/A                  | N/A                             | Reserved (experimental use)   |

> **Note!:** 127.0.0.0/8 is reserved for loopback and is not assigned to any class.