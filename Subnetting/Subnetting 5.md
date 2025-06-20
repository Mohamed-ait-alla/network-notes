# Subnetting in Action - Let's Subnet Your Home Network
### Objective
We want to subnet our home network (192.168.1.0/24) into 4 smaller networks: **Wireless**,**IOT**, **DMZ**, **User**, so Let's do it.

### Original Network
- Network Address: **192.168.1.0**
- Subnet Mask: **255.255.255.0**
- CIDR Notation: **/24**
- Total IPs: **256**
- Usable Hosts: **254**

### Step 0 - Convert Subnet Mask to Binary
>Using the **hack table**: `128 64 32 16 8 4 2 1` <br>
>`255.255.255.0` → `11111111.11111111.11111111.00000000` → 24 **network bits**, 8 **host bits**.<br>
>We’ll be “hacking” into these **8 host bits**.

### Step 1 - Calculate How Many Host Bits to Hack
>We want **4 networks**, so we need to find how many bits are required to represent 4 subnets.<br>
>
>We use the **formula**:<br>
>**`2^n ≥ number_of_subnets`** <br>
>So:<br>
>**`2^2 = 4 → ✅`** <br>
>So we need to hack **2 host bits**

### Step 2 - Hack the Host Bits
> We **steal** **2** bits from the host portion and **add** them to the network portion:
> - Original subnet mask: `/24 → 255.255.255.0 | 11111111.11111111.11111111.00000000`
> - New subnet mask: `/26 → 255.255.255.192 | 11111111.11111111.11111111.11000000`
>
>**Why .192?** <br>
> Use the **hack table** again for the 4th octet: <br>
> `128 64 32 16 8 4 2 1` <br>
> **Add the first 2 bits**: `128 + 64 = 192`

### Step 3 - Find the Increment
>Now we calculate the **block size** or **increment**:<br>
>
>**Formula**:<br>
>`Increment = 256 – subnet_mask_octet` <br>
>So: <br>
>`Increment = 256 – 192 = 64` <br>
>Each subnet increases by **64**.

### Step 4 - Create Your Networks
>We now break down `192.168.1.0/24` into 4 `/26` subnets:
>| Subnet  | Network Address     | IP Range                  | Broadcast Address   | Usable Hosts | Suggested Use |
>|----------|---------------------|---------------------------|---------------------|--------------|----------------|
>| 1        | 192.168.1.0/26      | 192.168.1.1 – 192.168.1.62  | 192.168.1.63        | 62           | Wireless       |
>| 2        | 192.168.1.64/26     | 192.168.1.65 – 192.168.1.126 | 192.168.1.127       | 62           | IoT            |
>| 3        | 192.168.1.128/26    | 192.168.1.129 – 192.168.1.190 | 192.168.1.191     | 62           | DMZ            |
>| 4        | 192.168.1.192/26    | 192.168.1.193 – 192.168.1.254 | 192.168.1.255     | 62           | User Devices   |


> **Note!**: You can subnet any IP into small pieces by following the steps covered in this lesson.