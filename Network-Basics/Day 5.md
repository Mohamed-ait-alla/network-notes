## What is Network Design
**Network design** is the process of creating a plan for how a computer network will be physically and logically structured to meet the specific needs of an organization, to ensure efficient data flow and connectivity and avoid the downtime of networks.

## Common Network Design Mistakes

- ***Flat Network Structure:*** Placing all devices on a single subnet without segmentation can lead to performance issues and security vulnerabilities.

- ***Single Point of Failure:*** Relying on one device for multiple functions increases the risk of network downtime.

## Best Practices for Robust Network Design

A well-designed network ensures **reliability**, **scalability**, and **security** of networks, In this section we will talk about solutions that makes sure that:

#### Implement Redundancy

1. **Dual Connections:** Connect switches and routers in a way that if one link fails, another can take over.

2. **Multiple Devices:** Use multiple distribution and core switches to ensure continuous network operation.

#### Network Segmentation
1. **VLANs:** Divide the network into Virtual Local Area Networks (VLANs) to improve security and performance.

2. **Subnets:** Create subnets to manage traffic efficiently and enhance security.

#### Network Architectures

#####  Two-Tier Architecture
This architecture combines the **access** and **distribution** layers. Devices (like PCs, printers) connect directly to a distribution switch, which may also act as a core. It is designed  for small and medium-sized networks.

##### Three-Tier Architecture

A structured approach dividing the network into **Access**, **Distribution**, and **Core** layers. It's expensive, but it is the best one. It is desinged for medium-sized to large networks.