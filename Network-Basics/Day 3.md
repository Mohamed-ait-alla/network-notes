## Network models

A Network Model is a design framework used in networking to organize and simplify the complexities of communication systems. It divides the networking process into different layers. With each layer assigned a specific set of tasks and responsibilities. The most commonly used models are:<br>
- **OSI Model**
- **TCP/IP Model**

## What is OSI Model
Is a set of rules that explain how different computer systems communicate over a network. and was devlopped by the **International Organization for Standardization (ISO)**. The OSI model consists of 7 layers that are:<br>
- ***Physical Layer:*** It is responsible for transmitting data between devices in form of **bits**. When it receives data, it will convert the signal received into 0s and 1s and send them to the **Data Link** layer, which will put the frame back together. **Hubs**, **Repeaters**, **Modems** and **Cables** are common physical layer devices.

- ***Data Link Layer:*** The main function of this layer is to make sure data transfer is **error-free** from one node to another, over the physical layer. When a packet arrives in a network, it is the responsibility of the data link layer to transmit it to the Host Using its MAC address. Packet in the Data Link is referred to as **Frame**. **Switches** and **Bridges** are common devices in this layer.

- ***Network Layer:*** It is responsible for transmitting data from one host to the another located in different networks by using IP addresses. It also takes care of packet routing by selecting the shortest path to transmit the packet. Network layer is implemented by networking devices such as **Routers** and modern **Switches**.

- ***Transport Layer:*** It is responsible for the end-to-end delivery of the complete data. it also provides the acknowledgment of the successful data transmission and re-transmits the data if an error occured. It uses these protocols **TCP**, **UDP**, **NetBIOS**, **PPTP** to complete its mission.

- ***Session Layer:*** is responsible for the establishment of connections, management of connections, termination of sessions between two devices. It also provides authentication and security. Protocols used in the Session Layer are **NetBIOS**, **PPTP**.

- ***Presentation Layer:*** This layer is responsible for formatting, compressing, encrypting and decrypting data.

- ***Application Layer:*** This is the top layer in OSI model, acting as the interface between user applications and the network. It provides services and protocols that allow applications to communicate and share resources across the network such as **HTTP**, **FTP**, **SMTP** etc.

## How Data Flows in the OSI model

When we transfer information from one device to another, it travels through 7 layers of OSI model. First data travels down through 7 layers from the sender's end and then climbs back 7 layers on the receiver's end.
<br>
Data flows through the OSI model in a step-by-step process:

- ***Application Layer:*** Applications create the data.
- ***Presentation Layer:*** Data is formatted and encrypted.
- ***Session Layer:*** Connections are established and managed.
- ***Transport Layer:*** Data is broken into segments for reliable delivery.
- ***Network Layer:*** Segments are packaged into packets and routed.
- ***Data Link Layer:*** Packets are framed and sent to the next device.
- ***Physical Layer***: Frames are converted into bits and transmitted physically.

> **note!:** Each layer from the sender's end adds specific headers to ensure the data reaches its destination correctly, this process called ***Encapsulation***. and in the receive's end, each layer try to ***de-encapsulate*** the headers to extract it's data.

## What is TCP/IP model
Is a framework that describes how data is transmited across a network. Is a concise version of the OSI model, and it consists of 4 layers:
- ***Application Layer***
- ***Transport Layer***
- ***Network/Internet Layer***
- ***Network Access Layer***

> **note:** The TCP/IP model is the primary model used nowadays in modern networking, because of it's simplicity.
