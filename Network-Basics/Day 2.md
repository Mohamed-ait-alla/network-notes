## What is a Router
Is a device that connects **different multiple networks** together and forwards data between them. Is the device that enables you to **access to the internet**. Routers are working in the third layer of OSI model (**means they understand only IP addresses**).

## How it works

1. It looks at **IP addresses** to decide **where the data should go**
2. Then it looks at the **routing table**, which is a list of paths to various network destinations, to find the best path for the **packet** to reach its destination.
3. forwards the packet.

> **note:** when we send data over the network, it's divided into smaller packets to make it easier to manage and route.

## Basic Router CLI Commands
```bash

# Enter privileged EXEC mode
Router> enable

# Enter global configuration mode
Router# configure terminal

# Set a hostname
Router(config)# hostname MyRouter

# Configure an interface with an IP address
MyRouter(config)# interface GigabitEthernet0/0
MyRouter(config-if)# ip address 192.168.1.1 255.255.255.0
MyRouter(config-if)# no shutdown

# Add a description to the interface (optional)
MyRouter(config-if)# description LAN interface

# Configure a default gateway (for local devices)
# Routers don't need a default gateway but can have a default route instead
MyRouter(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.254

# Configure a static route
MyRouter(config)# ip route 10.0.0.0 255.255.255.0 192.168.1.2

# Enable routing protocols (example: RIP)
MyRouter(config)# router rip
MyRouter(config-router)# network 192.168.1.0

# View the routing table
MyRouter# show ip route

# View interface status and IPs
MyRouter# show ip interface brief

# Save the configuration
MyRouter# copy running-config startup-config

# View running config
MyRouter# show running-config

```