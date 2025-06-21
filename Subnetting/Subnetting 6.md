# Subnetting in Action - Let's Subnet a Coffe Shop
### Objective
We want to subnet an IP block to support three coffee shops, each requiring 30 to 40 hosts. Our goal is to divide a network into three subnets, each large enough to accommodate this number of hosts.
> In this lesson, we’re subnetting based on **host requirements**, unlike the previous lesson where we subnetted based on **the number of networks**.

###  Original Network
- Network Address: **`10.1.1.0/24`**

- Default Subnet Mask: **`255.255.255.0`**

- Available IPs: **256** total IPs (**254** usable)

###  Step 0 - Convert Subnet Mask to Binary
> Default **/24** Subnet Mask, So:
>
> Decimal: **255.255.255.0**  
> Binary:  **11111111.11111111.11111111.00000000**

###  Step 1 - Calculate How Many Host Bits to Hack
> Each shop needs at least **40 usable hosts**. <br>
> We calculate how many bits we need to leave for hosts:
> - Formula: **`2^n - 2 ≥ number_of_hosts`** <br>
>
> - Try **6 host bits**:<br>
> **`2^6 - 2 = 64 - 2 = 62 usable IPs`**
>
>
> ✅ **6 bits are enough** → That means we can **borrow 2 bits** from the host portion for subnetting.

### Step 2 - Hack the Host Bits
> - Original host bits: **8**
> - Borrowed for subnetting: **2**
> - Remaining host bits: **6**
> - New CIDR: **/26**
>
> **New Subnet Mask:**
> - **Binary**: `11111111.11111111.11111111.11000000`
> - **Decimal**: `255.255.255.192`

### Step 3 - Find the Increment
> - **Increment** = `256 - 192 = 64`
>
> This means each new subnet **increases by 64** in the last octet.

### Step 4 - Create Your Networks
> With a **/26** subnet, we divide **`10.1.1.0/24`** into **4** equal subnets:
>
> | Subnet | Network Address   | Usable IP Range            | Broadcast Address |
> |--------|-------------------|----------------------------|-------------------|
> | 1      | 10.1.1.0/26       | 10.1.1.1 – 10.1.1.62        | 10.1.1.63         |
> | 2      | 10.1.1.64/26      | 10.1.1.65 – 10.1.1.126      | 10.1.1.127        |
> | 3      | 10.1.1.128/26     | 10.1.1.129 – 10.1.1.190     | 10.1.1.191        |

