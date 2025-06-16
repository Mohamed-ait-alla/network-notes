## What is a Switch
Is a device that connects multiple network devices (like computers, printers, or servers) together within a local area network (LAN).

## How it Works
1. **Devices connect** to the switch via Ethernet cables.
2. The switch **learns** each device's **MAC address** and remembers which port it's connected to (***in this phase the switch builds a table called Content Addressable Memory to recognize each device connected to it***).
3. When a device sends data (a frame), the switch first **searches the content Addressable Memory (CAM) table**  for an entry that matches the destination MAC address. If the **destination MAC address is not found** in the table, the Switch **sends a message to all its ports**. If the **destination MAC address is found** in the table, the Switch fowards the frame to **the appropriate port**. the **source MAC address** is added to the CAM table **if it did not previously exist** in the table.

## Basic Cisco Switch CLI Commands

```bash
# Enter privileged EXEC mode
Switch> enable

# Enter global configuration mode
Switch# configure terminal

# Set a hostname
Switch(config)# hostname MySwitch

# Set an interface (e.g., port FastEthernet 0/1)
MySwitch(config)# interface FastEthernet0/1

# Enable the port
MySwitch(config-if)# no shutdown

# Assign port to a VLAN
MySwitch(config-if)# switchport access vlan 10

# Set the port mode to access (for host devices)
MySwitch(config-if)# switchport mode access

# View MAC address table
MySwitch# show mac address-table

# Save the configuration
MySwitch# write memory
# or
MySwitch# copy running-config startup-config

# View running configuration
MySwitch# show running-config

# Show interface status
MySwitch# show interfaces status

```

## The Difference between Hubs and Switches
A Hub is also a device that connects multiple devices, but instead of sending data to **the destination only as Switches** does, **the hub broadcasting** data to all connected devices. So **Switches** are more intelligent and offering more efficient and reliable network traffic.