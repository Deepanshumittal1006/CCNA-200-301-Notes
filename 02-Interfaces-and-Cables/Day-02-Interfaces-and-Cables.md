# CCNA 200-301 Notes - Day 2

# Interfaces, Ethernet & Network Cables

## Overview

In this lesson, we learn how network devices are physically connected. Understanding interfaces, Ethernet standards, copper cables, fiber-optic cables, and transmission methods is fundamental for networking and the CCNA exam.

---

# Network Interfaces

A network interface (also called a port) is the physical connection point through which a device sends and receives network traffic.

### Example

A Cisco switch typically contains many interfaces:

* 24-port switch
* 48-port switch

These ports allow multiple devices to connect to the network.

---

# RJ-45 Ports and Connectors

## RJ-45 Port

The most common Ethernet port used on:

* PCs
* Laptops
* Routers
* Switches

RJ stands for:

```text
Registered Jack
```

---

## RJ-45 Connector

The connector found at the end of an Ethernet cable.

### Characteristics

* 8 pins
* Used with copper Ethernet cables
* Fits into RJ-45 ports

---

# Ethernet

## Definition

Ethernet is a collection of networking standards and protocols used for wired LAN communication.

### Purpose

Ethernet defines:

* Cable types
* Connectors
* Data transmission methods
* Speeds
* Physical standards

---

# Why Standards Matter

Without standards:

* Devices from different manufacturers may not communicate.
* Connectors may not fit.
* Data transmission methods may differ.

### Example

A cable manufacturer and switch manufacturer must follow the same standards so their products work together.

---

# Bits and Bytes

## Bit

A bit is the smallest unit of data.

Possible values:

```text
0
1
```

---

## Byte

A byte consists of:

```text
8 bits
```

---

# Network Speed Measurements

Network speeds are measured in:

```text
Bits Per Second (bps)
```

Not bytes per second.

---

## Common Units

| Unit   | Value                  |
| ------ | ---------------------- |
| 1 Kbps | 1,000 bits             |
| 1 Mbps | 1,000,000 bits         |
| 1 Gbps | 1,000,000,000 bits     |
| 1 Tbps | 1,000,000,000,000 bits |

---

# Ethernet Copper Standards

## Common Ethernet Standards

| Speed    | Common Name         | IEEE Standard | Informal Name | Max Distance |
| -------- | ------------------- | ------------- | ------------- | ------------ |
| 10 Mbps  | Ethernet            | 802.3i        | 10BASE-T      | 100 m        |
| 100 Mbps | Fast Ethernet       | 802.3u        | 100BASE-T     | 100 m        |
| 1 Gbps   | Gigabit Ethernet    | 802.3ab       | 1000BASE-T    | 100 m        |
| 10 Gbps  | 10 Gigabit Ethernet | 802.3an       | 10GBASE-T     | 100 m        |

---

## Naming Convention

### Example

```text
1000BASE-T
```

### Meaning

| Component | Meaning            |
| --------- | ------------------ |
| 1000      | Speed (Mbps)       |
| BASE      | Baseband Signaling |
| T         | Twisted Pair Cable |

---

# UTP Cable

## Definition

UTP stands for:

```text
Unshielded Twisted Pair
```

---

## Structure

A UTP cable contains:

* 4 twisted pairs
* 8 total wires

---

## Why Twisting?

Twisting reduces:

```text
Electromagnetic Interference (EMI)
```

---

# Ethernet Pin Usage

## RJ-45 Pins

```text
1 2 3 4 5 6 7 8
```

---

# 10BASE-T and 100BASE-T

Use only:

```text
Pins 1,2,3,6
```

Two wire pairs.

---

## PC / Router Interfaces

### Transmit

```text
Pins 1 and 2
```

### Receive

```text
Pins 3 and 6
```

---

## Switch Interfaces

### Receive

```text
Pins 1 and 2
```

### Transmit

```text
Pins 3 and 6
```

---

# Full-Duplex Communication

## Definition

Both devices can:

* Send data simultaneously
* Receive data simultaneously

without collisions.

---

# Straight-Through Cable

## Definition

A cable where each pin connects directly to the same pin on the opposite side.

### Example

```text
1 → 1
2 → 2
3 → 3
6 → 6
```

---

## Used Between

Different device types:

* PC ↔ Switch
* Router ↔ Switch
* Firewall ↔ Switch

---

# Crossover Cable

## Definition

A cable where transmit and receive pairs are crossed.

### Example

```text
1 → 3
2 → 6
3 → 1
6 → 2
```

---

## Used Between

Same device types:

* Switch ↔ Switch
* Router ↔ Router
* PC ↔ PC
* Router ↔ PC

---

# Device Transmission Chart

| Device   | Transmit | Receive |
| -------- | -------- | ------- |
| PC       | 1,2      | 3,6     |
| Router   | 1,2      | 3,6     |
| Firewall | 1,2      | 3,6     |
| Switch   | 3,6      | 1,2     |

---

# Auto MDI-X

## Definition

Auto MDI-X allows devices to automatically detect transmission pairs and adjust accordingly.

---

## Benefits

No need to worry about:

* Straight-through cables
* Crossover cables

Modern devices usually handle this automatically.

---

# Gigabit Ethernet

## 1000BASE-T and 10GBASE-T

Use all 8 wires:

```text
1,2
3,6
4,5
7,8
```

---

## Bidirectional Communication

Unlike Fast Ethernet:

* Every pair can transmit and receive.
* Higher performance.
* Faster speeds.

---

# Fiber Optic Networking

## Definition

Fiber-optic cables transmit:

```text
Light
```

instead of electrical signals.

---

# SFP Modules

## SFP

Stands for:

```text
Small Form-factor Pluggable
```

---

## Purpose

Allows fiber-optic connections on:

* Switches
* Routers

---

# Fiber Optic Cable Structure

## Components

### 1. Core

Glass fiber carrying light.

### 2. Cladding

Reflects light within the core.

### 3. Buffer

Protects the fiber.

### 4. Outer Jacket

Protective outer layer.

---

# Multimode Fiber (MMF)

## Characteristics

* Wider core
* Multiple light paths
* LED-based transmitters
* Lower cost

### Advantages

* Cheaper
* Longer distance than UTP

### Disadvantages

* Shorter distance than single-mode fiber

---

# Single-Mode Fiber (SMF)

## Characteristics

* Narrower core
* Single light path
* Laser-based transmitters
* More expensive

### Advantages

* Longest distance support
* Highest performance

### Disadvantages

* Higher cost

---

# Fiber Standards

## 1000BASE-LX

| Feature      | Value  |
| ------------ | ------ |
| Speed        | 1 Gbps |
| MMF Distance | 550 m  |
| SMF Distance | 5 km   |

---

## 10GBASE-SR

| Feature    | Value   |
| ---------- | ------- |
| Speed      | 10 Gbps |
| Fiber Type | MMF     |
| Distance   | 400 m   |

---

## 10GBASE-LR

| Feature    | Value   |
| ---------- | ------- |
| Speed      | 10 Gbps |
| Fiber Type | SMF     |
| Distance   | 10 km   |

---

## 10GBASE-ER

| Feature    | Value   |
| ---------- | ------- |
| Speed      | 10 Gbps |
| Fiber Type | SMF     |
| Distance   | 30 km   |

---

# UTP vs Fiber Optic

| Feature         | UTP                     | Fiber Optic          |
| --------------- | ----------------------- | -------------------- |
| Cost            | Lower                   | Higher               |
| Distance        | Up to 100m              | Much Longer          |
| EMI Resistance  | Vulnerable              | Immune               |
| Security        | Signal Leakage Possible | No Leakage           |
| Connector       | RJ-45                   | SFP/Fiber Connectors |
| Speed Potential | High                    | Very High            |

---

# CCNA Exam Tips

### Remember

* RJ-45 = Copper Ethernet
* UTP = Unshielded Twisted Pair
* Switches use opposite TX/RX pins from PCs and routers
* Straight-through = Different device types
* Crossover = Same device types
* Auto MDI-X removes cable concerns
* Fiber supports longer distances
* Single-mode > Multimode for distance

---

# Quick Revision

✅ Ethernet uses standardized cables and connectors.

✅ RJ-45 connectors contain 8 pins.

✅ UTP cables contain 4 twisted pairs.

✅ 10BASE-T and 100BASE-T use only 4 wires.

✅ Gigabit Ethernet uses all 8 wires.

✅ Straight-through cables connect different device types.

✅ Crossover cables connect similar device types.

✅ Auto MDI-X automatically adjusts transmit/receive pairs.

✅ Fiber-optic cables use light instead of electricity.

✅ Single-mode fiber supports the longest distances.

---

# Interview Questions

### Q1. What does RJ-45 stand for?

Registered Jack 45.

### Q2. What is Auto MDI-X?

A feature that automatically adjusts transmit and receive pairs.

### Q3. What is the difference between straight-through and crossover cables?

Straight-through connects different device types, while crossover connects similar device types.

### Q4. Why is fiber-optic cable preferred for long distances?

Because it supports much longer distances and is immune to EMI.

### Q5. Which fiber type supports longer distances?

Single-mode fiber.

---

# Lesson Summary

This lesson introduced Ethernet cabling and physical network connectivity. We covered:

* RJ-45 interfaces
* Ethernet standards
* UTP cables
* Straight-through and crossover cables
* Auto MDI-X
* Fiber-optic networking
* Single-mode and multimode fiber
* Ethernet speed standards

These concepts form the foundation for understanding physical network connectivity in enterprise networks.
