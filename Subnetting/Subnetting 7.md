# VLSM Subnetting
### What is VLSM?
**VLSM (Variable Length Subnet Masking)** is a subnetting technique that **allows the use of different subnet masks within the same network**.
Instead of splitting the network into equal-sized subnets (as in traditional subnetting), VLSM enables you **to allocate IPs based on actual host requirements, conserving IP space**.

> **Key Strategy:** <br>
> Always allocate IPs to the largest subnet first, then work your way down to smaller subnets.

### Real-Life Example
#### Problem Overview
> You are given a single IP network: <br>
> `172.21.42.0/24` (i.e., 256 total addresses)<br>
> Your task is to divide this network into four subnets of **different sizes**, each fitting a specific number of required hosts:
> - Workers: **117** hosts
> - Robots: **57** hosts
> - Servers: **26** hosts
> - Guests: **10** hosts

#### Step-by-Step Solution (Using VLSM)
> **Note!:**  We're using the same 4-step subnetting process covered in earlier lessons to solve this problem. Instead we're just subnetting from largest host requirements to smaller, and each time we're working on the previous subnet mask. So let's do it.
>
>
> 1.  **Workers - 117 Hosts**
> - Needed bits for 117 hosts: **7** bits (**2⁷ = 128 addresses**)
> - Subnet mask: **/25 (255.255.255.128)**
> - Network: `172.21.42.0/25`
> - Usable IPs: from `172.21.42.1` to `172.21.42.126`
> - Broadcast: `172.21.42.127`
>
>
> 2.  **Robots - 57 Hosts**
> - Next available address: `172.21.42.128 /25`
> - Needed bits: **6** bits (**2⁶ = 64** addresses)
> - Subnet mask: **/26 (255.255.255.192)**
> - Network: `172.21.42.128/26`
> - Usable IPs: from `172.21.42.129` to `172.21.42.190`
> - Broadcast: `172.21.42.191`
>
>
> 3.  **Servers - 26 Hosts**
> - Next available address: `172.21.42.192 /26`
> - Needed bits: **5** bits (**2⁵ = 32** addresses)
> - Subnet mask: **/27 (255.255.255.224)**
> - Network: `172.21.42.192/27`
> - Usable IPs: from `172.21.42.193` to `172.21.42.222`
> - Broadcast: `172.21.42.223`
>
>
> 3. **Guests - 10 Hosts**
> - Next available address: `172.21.42.224 /27`
> - Needed bits: **4** bits (**2⁴ = 16** addresses)
> - Subnet mask: **/28 (255.255.255.240)**
> - Network: `172.21.42.224/28`
> - Usable IPs: from `172.21.42.225` to `172.21.42.238`
> - Broadcast: `172.21.42.239`
