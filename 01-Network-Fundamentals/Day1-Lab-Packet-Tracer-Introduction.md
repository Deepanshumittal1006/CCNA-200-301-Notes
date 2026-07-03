# CCNA 200-301 Notes - Day 1 Lab

# Introduction to Cisco Packet Tracer

## Lab Objective

This lab introduces Cisco Packet Tracer, the network simulation software used throughout the CCNA course.

By completing this lab, you will learn how to:

* Download and install Packet Tracer
* Navigate the Packet Tracer interface
* Place network devices
* Rename devices
* Connect devices
* Recreate a simple enterprise network topology

---

# What is a Lab?

In networking, a lab is a hands-on exercise used to practice real-world networking concepts.

### Purpose

Labs help you:

* Apply theoretical knowledge
* Practice network configuration
* Develop troubleshooting skills
* Prepare for the CCNA exam

---

# Why Use Packet Tracer?

Instead of purchasing expensive Cisco hardware, Packet Tracer allows us to build virtual networks on a computer.

### Benefits

* Free to use
* Easy to install
* Simulates Cisco devices
* Great for CCNA preparation
* Supports networking labs and troubleshooting exercises

---

# Packet Tracer Overview

Packet Tracer is a network simulation tool developed by Cisco.

### Simulated Devices

* Routers
* Switches
* Firewalls
* PCs
* Servers
* Laptops
* Wireless devices

These are simulated devices, not actual Cisco hardware.

---

# Downloading Packet Tracer

## Requirements

A Cisco account is required.

### Supported Operating Systems

* Windows (64-bit)
* Windows (32-bit)
* Ubuntu Linux
* macOS

### Recommendation

Always install the latest Packet Tracer version to ensure compatibility with newer lab files.

---

# Packet Tracer Interface

## Main Components

### Workspace

The area where network topologies are built.

### Device Selection Panel

Used to select:

* Routers
* Switches
* Firewalls
* End Devices
* Connections

### Connections Tool

Represented by a lightning bolt icon.

Used to connect network devices together.

---

# Packet Tracer Preferences

Navigate to:

```text
Options → Preferences
```

---

## Useful Settings

### Device Name Labels

Shows device names:

```text
PC1
SW1
R1
```

---

### Device Model Labels

Shows hardware models:

```text
2911
2960
5505
```

---

### Font Settings

Customize:

* CLI font size
* Menu font size
* Colors

---

# Command Line Interface (CLI)

CLI stands for:

```text
Command-Line Interface
```

---

## Purpose

Routers and switches are configured primarily through the CLI.

Example:

```text
Router>
```

Most CCNA configurations will be performed through this interface.

---

# Network Topology Built in the Lab

The topology recreates the enterprise network shown in Day 1's lecture.

---

## Internet

Represented by:

```text
Cisco 2911 Router
```

Named:

```text
The Internet
```

---

# New York Branch

## Devices

### PCs

* PC1
* PC2

### Switch

* SW1

### Router

* R1

### Firewall

* FW1

---

# Tokyo Branch

## Devices

### Servers

* SRV1
* SRV2

### Switch

* SW2

### Router

* R2

### Firewall

* FW2

---

# Attacker Device

A laptop is used to represent:

```text
Attacker
```

Located outside the enterprise network.

---

# Devices Used

## Routers

### Cisco 2911

Used for:

* R1
* R2
* Internet

---

## Switches

### Cisco Catalyst 2960

Used for:

* SW1
* SW2

---

## Firewalls

### Cisco ASA 5505

Used for:

* FW1
* FW2

---

## End Devices

### PCs

* PC1
* PC2

### Servers

* SRV1
* SRV2

### Laptop

* Attacker

---

# Device Placement Process

## Step 1

Open:

```text
Network Devices → Routers
```

Place:

* R1
* R2

---

## Step 2

Open:

```text
Network Devices → Switches
```

Place:

* SW1
* SW2

---

## Step 3

Open:

```text
Network Devices → Firewalls
```

Place:

* FW1
* FW2

---

## Step 4

Open:

```text
End Devices
```

Place:

* PC1
* PC2
* SRV1
* SRV2
* Attacker Laptop

---

# Device Naming

Rename devices to match the topology.

### Example

```text
PC1
PC2
SW1
R1
FW1
R2
FW2
SW2
SRV1
SRV2
Attacker
```

---

# Connecting Devices

Use the lightning bolt icon:

```text
Connections
```

For this lab:

```text
Automatically Choose Connection Type
```

is used.

Packet Tracer automatically selects the correct cable.

---

# Network Connections

## New York Branch

```text
PC1 → SW1
PC2 → SW1
SW1 → R1
R1 → FW1
FW1 → Internet
```

---

## Tokyo Branch

```text
Internet → R2
R2 → FW2
FW2 → SW2
SW2 → SRV1
SW2 → SRV2
```

---

## External Device

```text
Attacker → Internet
```

---

# Productivity Tip

To create multiple connections faster:

### Windows

Hold:

```text
CTRL
```

while selecting the connection tool.

This keeps the connection tool active after each connection.

---

# Important Lab Concept

Throughout the CCNA course:

### Normal Labs

You configure devices yourself.

### Troubleshooting Labs

The instructor intentionally introduces configuration mistakes.

Your task is to:

* Identify issues
* Troubleshoot
* Fix configurations

---

# Skills Practiced

This lab develops familiarity with:

* Packet Tracer interface
* Device placement
* Network topology design
* Device naming
* Network connections
* CLI access

---

# CCNA Exam Tips

✅ Packet Tracer is one of the best tools for CCNA practice.

✅ Learn to navigate the CLI comfortably.

✅ Understand basic Cisco device models.

✅ Build topologies manually instead of only watching videos.

✅ Troubleshooting skills are just as important as configuration skills.

---

# Quick Revision

### Router Used

```text
Cisco 2911
```

### Switch Used

```text
Cisco Catalyst 2960
```

### Firewall Used

```text
Cisco ASA 5505
```

### CLI Meaning

```text
Command-Line Interface
```

### Connection Tool

```text
Lightning Bolt Icon
```

---

# Lab Summary

This lab introduced Cisco Packet Tracer and demonstrated how to build a simple enterprise network topology.

Key tasks completed:

* Installed and launched Packet Tracer
* Explored the user interface
* Added routers, switches, firewalls, and end devices
* Renamed devices
* Connected network devices
* Recreated a real-world enterprise network diagram

This foundation will be used throughout the remainder of the CCNA course for configuration and troubleshooting labs.
