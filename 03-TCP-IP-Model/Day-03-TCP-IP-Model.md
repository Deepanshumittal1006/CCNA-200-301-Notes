# CCNA 200-301 Notes - Day 3

# TCP/IP Model (Internet Protocol Suite)

## Overview

The Internet Protocol Suite (TCP/IP) is the collection of protocols that make communication across networks and the Internet possible.

The TCP/IP model provides a layered framework that explains:

* How devices communicate
* How data travels through networks
* How protocols work together
* How network devices perform their roles

Understanding the TCP/IP model is essential because nearly every networking technology fits into one of its layers.

---

# Protocols and Standards

## Protocol

A protocol is a set of rules that defines how devices communicate across a network.

### Examples

* IP
* TCP
* UDP
* HTTP
* HTTPS
* DNS

### Purpose

Protocols ensure that devices can:

* Exchange data
* Interpret information correctly
* Communicate reliably

---

## Standard

A standard is an agreed-upon specification describing how technologies and protocols should operate.

### Benefits

* Vendor interoperability
* Consistent communication
* Universal compatibility

### Example

A Windows PC can communicate with:

* Linux Server
* Apple MacBook
* Android Smartphone

because they follow common networking standards.

---

# History of TCP/IP

## ARPANET

The precursor to the modern Internet.

### Developed By

```text id="arp001"
ARPA
(Advanced Research Projects Agency)
```

### Year

```text id="arp002"
1969
```

---

## Original Protocol

```text id="arp003"
NCP
(Network Control Program)
```

---

## TCP Development

In 1974:

* Vint Cerf
* Bob Kahn

began developing TCP.

---

## Evolution

Original TCP later became:

### TCP

```text id="tcp001"
Transmission Control Protocol
```

### IP

```text id="ip001"
Internet Protocol
```

---

## Major Milestone

ARPANET officially adopted TCP/IP:

```text id="arp004"
January 1, 1983
```

---

# Standards Organizations

## IEEE

### Full Name

Institute of Electrical and Electronics Engineers

---

### Responsibilities

Develops:

* Ethernet (802.3)
* Wi-Fi (802.11)

---

## IETF

### Full Name

Internet Engineering Task Force

---

### Responsibilities

Develops Internet protocols such as:

* TCP
* IP
* UDP
* HTTP
* DNS

---

## RFC

IETF standards are published as:

```text id="rfc001"
RFC
(Request For Comments)
```

---

# Why Use Layers?

Networks perform many tasks:

* Signal transmission
* Local delivery
* Routing
* Process communication
* Application communication

Instead of combining everything together, networking uses layers.

---

# Benefits of Layered Models

### Simplicity

Each layer has a specific role.

### Modularity

Protocols can change without affecting other layers.

### Troubleshooting

Problems can be isolated to specific layers.

### Scalability

Technologies can evolve independently.

---

# TCP/IP Five-Layer Model

| Layer   | Function      |
| ------- | ------------- |
| Layer 5 | Application   |
| Layer 4 | Transport     |
| Layer 3 | Internet      |
| Layer 2 | Local Network |
| Layer 1 | Physical      |

---

# Layer 5 – Application Layer

## Purpose

Provides communication between applications.

---

## Responsibilities

* Creates data
* Formats messages
* Interprets received data

---

## Examples

### Web Browsing

```text id="app001"
HTTP
HTTPS
```

### File Transfer

```text id="app002"
FTP
TFTP
```

### Email

```text id="app003"
SMTP
POP3
IMAP
```

---

## Example Scenario

Chrome browser requests a webpage from a web server.

The Application Layer creates the HTTP request.

---

# Layer 4 – Transport Layer

## Purpose

Provides end-to-end communication between application processes.

---

## Key Concept

Uses:

```text id="tr001"
Port Numbers
```

to identify applications.

---

## Example

| Service | Port |
| ------- | ---- |
| HTTP    | 80   |
| FTP     | 21   |

---

## Main Protocols

### TCP

Transmission Control Protocol

### UDP

User Datagram Protocol

---

## Example

A web request is delivered to:

```text id="tr002"
Port 80
```

on the destination server.

---

# Layer 3 – Internet Layer

## Purpose

Provides end-to-end communication between hosts.

---

## Key Components

### IP Addresses

Used to identify hosts.

### Routers

Used to forward traffic.

---

## Example

```text id="int001"
10.1.1.1
```

could be a server IP address.

---

## Main Protocols

### IPv4

Internet Protocol Version 4

### IPv6

Internet Protocol Version 6

### ICMP

Internet Control Message Protocol

---

# Layer 2 – Local Network Layer

## Purpose

Provides hop-to-hop delivery across local networks.

---

# What Is a Hop?

A hop is one step between devices.

### Example

```text id="hop001"
PC → Router = 1 Hop
Router → Router = 1 Hop
Router → Server = 1 Hop
```

---

## Key Components

### MAC Addresses

Used to identify interfaces.

### Switches

Forward traffic within LANs.

---

## Main Protocols

### Ethernet

### Wi-Fi

---

# Layer 1 – Physical Layer

## Purpose

Transmits bits across the physical medium.

---

## Transmission Methods

### Electrical Signals

Copper Ethernet

### Optical Signals

Fiber Optic

### Radio Signals

Wireless Networks

---

## Examples

* UTP Cable
* Fiber Cable
* Wireless Radios
* NICs

---

# Layer Responsibilities Summary

| Layer         | Primary Identifier |
| ------------- | ------------------ |
| Application   | Application Data   |
| Transport     | Port Numbers       |
| Internet      | IP Addresses       |
| Local Network | MAC Addresses      |
| Physical      | Bits               |

---

# Encapsulation

## Definition

The process of adding headers as data moves down the protocol stack.

---

## Process

### Layer 5

Creates application data.

↓

### Layer 4

Adds Transport Header.

↓

### Layer 3

Adds IP Header.

↓

### Layer 2

Adds MAC Header and Trailer.

↓

### Layer 1

Transmits bits.

---

# Decapsulation

## Definition

The process of removing headers as data moves up the protocol stack.

---

## Process

### Layer 1

Receives bits.

↓

### Layer 2

Removes Layer 2 Header and Trailer.

↓

### Layer 3

Removes IP Header.

↓

### Layer 4

Removes Transport Header.

↓

### Layer 5

Processes application data.

---

# Protocol Data Units (PDUs)

Different layers use different names for data.

---

## Layer 4

### TCP

```text id="pdu001"
Segment
```

### UDP

```text id="pdu002"
Datagram
```

---

## Layer 3

```text id="pdu003"
Packet
```

---

## Layer 2

```text id="pdu004"
Frame
```

---

# PDU Summary

| Layer           | PDU Name |
| --------------- | -------- |
| Application     | Data     |
| Transport (TCP) | Segment  |
| Transport (UDP) | Datagram |
| Internet        | Packet   |
| Local Network   | Frame    |
| Physical        | Bits     |

---

# Payload

## Definition

The contents inside a PDU excluding that layer's header or trailer.

---

## Example

At Layer 3:

```text id="pay001"
Packet Payload
=
Segment + Data
```

---

# Layer Interaction

## Adjacent-Layer Interaction

Each layer provides services to the layer above.

### Example

Layer 3 provides IP delivery services to Layer 4.

---

## Same-Layer Interaction

Layers communicate with equivalent layers on other devices.

### Example

Transport Layer ↔ Transport Layer

Application Layer ↔ Application Layer

---

# TCP/IP vs OSI Model

## TCP/IP Model

| Layer         |
| ------------- |
| Application   |
| Transport     |
| Internet      |
| Local Network |
| Physical      |

---

## OSI Model

| Layer        |
| ------------ |
| Application  |
| Presentation |
| Session      |
| Transport    |
| Network      |
| Data Link    |
| Physical     |

---

# Important Comparison

| TCP/IP        | OSI                                  |
| ------------- | ------------------------------------ |
| Application   | Application + Presentation + Session |
| Transport     | Transport                            |
| Internet      | Network                              |
| Local Network | Data Link                            |
| Physical      | Physical                             |

---

# Common CCNA Layer Mapping

| Layer   | Devices      |
| ------- | ------------ |
| Layer 1 | Cables, NICs |
| Layer 2 | Switches     |
| Layer 3 | Routers      |
| Layer 4 | TCP/UDP      |
| Layer 5 | Applications |

---

# CCNA Exam Tips

### Remember

Layer 1

```text id="tip001"
Bits
```

Layer 2

```text id="tip002"
Frames
```

Layer 3

```text id="tip003"
Packets
```

Layer 4

```text id="tip004"
Segments / Datagrams
```

---

### Key Associations

* Layer 2 = MAC Address
* Layer 3 = IP Address
* Layer 4 = Port Number
* Layer 5 = Application Data

---

# Quick Revision

✅ TCP/IP is the protocol suite used on modern networks.

✅ IEEE develops Ethernet and Wi-Fi standards.

✅ IETF develops Internet protocols.

✅ TCP/IP uses a layered architecture.

✅ Layer 1 handles physical transmission.

✅ Layer 2 uses MAC addresses.

✅ Layer 3 uses IP addresses.

✅ Layer 4 uses port numbers.

✅ Layer 5 handles applications.

✅ Encapsulation adds headers.

✅ Decapsulation removes headers.

✅ Frames travel across the wire.

✅ Routers operate primarily at Layer 3.

✅ Switches operate primarily at Layer 2.

---

# Interview Questions

### Q1. What is TCP/IP?

The protocol suite used for communication across modern networks and the Internet.

### Q2. Which layer uses IP addresses?

Internet Layer (Layer 3).

### Q3. Which layer uses MAC addresses?

Local Network Layer (Layer 2).

### Q4. What is encapsulation?

The process of adding protocol headers as data moves down the protocol stack.

### Q5. What is the PDU at Layer 3?

Packet.

### Q6. What is the difference between TCP and UDP?

TCP creates segments and provides reliable communication, while UDP creates datagrams and prioritizes speed.

---

# Lesson Summary

The TCP/IP model provides a framework for understanding how network communication works.

The five layers are:

1. Application
2. Transport
3. Internet
4. Local Network
5. Physical

Each layer performs a specific function and works together through encapsulation, decapsulation, and standardized protocols to enable communication across networks and the Internet.

