## TCP and UDP (Transport Layer Protocols)

Both **TCP** and **UDP** operate at Layer 4 (Transport Layer) of the OSI model and are responsible for **getting data from one device to another**, but they do it in very different ways.

## TCP (Transimission Control Protocol)

#### Features:
- **Connection-oriented**: It first establishes a connection using a **3-way handshake** which is a special sequence of three TCP segments (SYN → SYN-ACK → ACK) exchanged between a client and a server to establish an end-to-end connection over an unreliable IP network .

- **Reliable**: Guarantees delivery, order, and error-checking.

- **Slower**, but safer.

#### Use Case Examples

- ***Web browsing*** (HTTP/HTTPS) because pages must load fully and in the right order.
- ***Emails*** (SMTP/IMAP/POP3) no data can be lost.
- ***File Transfers*** (FTP/SFTP)

##  UDP (User Datagram Protocol)

#### Features
- **Connectionless**: No handshake, no session, just sends packets.

- **Unreliable**, but **fast**.

- **No guarantee** of order or delivery.

#### Use Case Examples

- ***Video/voice calls*** (VoIP)

- ***Streaming (e.g., Netflix, YouTube)***

## Ports
Some applications are running multiple services such as, sending emails (SMTP), transfering files (FTP/SFTP) etc. But how they do it?. This is Where **Ports** comes in, so Think of **ports** as doors in a house (the IP address is the house address).
Each **door** (**port**) leads to a different service or application.
In networking:

> A port is a software-defined number associated to a network protocol that receives or transmits communication for a specific service. here is some exmaples:

- HTTP  -> 80
- HTTPS -> 443
- FTP   -> 21
- SMTP  -> 25
- SSH   -> 22
- DNS   -> 53