# CCNA 200-301 Notes - Day 2 Lab

# Packet Tracer Lab: Interfaces & Cables

## Lab Objective

This lab reinforces the concepts learned in Day 2 regarding:

* Straight-through cables
* Crossover cables
* Fiber-optic connections
* Device interface types
* Distance limitations of network media

The goal is to correctly connect network devices based on their device type and physical distance.

---

# Devices Used

## End Hosts

* PC1
* PC2
* PC3
* SRV1 (Server)

## Switches

* SW1
* SW2
* SW3
* SW4
* SW5
* SW6
* SW7
* SW8

## Routers

* R1
* R2
* R3
* R4

---

# Cable Types Used

## Copper Straight-Through Cable

Used between different device types.

### Examples

* PC ↔ Switch
* Router ↔ Switch
* Firewall ↔ Switch

---

## Copper Crossover Cable

Used between same device types.

### Examples

* Switch ↔ Switch
* Router ↔ Router
* PC ↔ PC

---

## Fiber-Optic Cable

Used when distance exceeds UTP limitations.

### Types

* Multimode Fiber (MMF)
* Single-Mode Fiber (SMF)

---

# Connection Rules Review

## PCs and Routers

Transmit:

```text
Pins 1 and 2
```

Receive:

```text
Pins 3 and 6
```

---

## Switches

Transmit:

```text
Pins 3 and 6
```

Receive:

```text
Pins 1 and 2
```

---

# Step 1: Connect End Devices to Switches

Since PCs and servers are different device types than switches, use:

```text
Copper Straight-Through Cable
```

### Connections

| Device | Connected To |
| ------ | ------------ |
| PC1    | SW3          |
| PC2    | SW4          |
| PC3    | SW7          |
| SRV1   | SW8          |

---

# Step 2: Connect Switches Together

Switches are the same device type.

Therefore use:

```text
Copper Crossover Cable
```

### Connections

| Switch | Switch |
| ------ | ------ |
| SW3    | SW1    |
| SW1    | SW2    |
| SW4    | SW2    |
| SW7    | SW5    |
| SW5    | SW6    |
| SW8    | SW6    |

---

# Step 3: Connect Switches to Routers

Routers and switches are different device types.

Therefore use:

```text
Copper Straight-Through Cable
```

### Connections

| Switch | Router |
| ------ | ------ |
| SW1    | R2     |
| SW2    | R2     |
| SW5    | R4     |
| SW6    | R4     |

---

# Step 4: Connect R2 and R1

Distance:

```text
50 meters
```

Maximum UTP distance:

```text
100 meters
```

Since routers are the same device type:

```text
Copper Crossover Cable
```

### Connection

| Router | Router |
| ------ | ------ |
| R2     | R1     |

---

# Step 5: Connect R1 and R3

Distance:

```text
3 kilometers
```

UTP maximum distance:

```text
100 meters
```

Multimode fiber maximum distance:

```text
550 meters
```

Since 3 km exceeds multimode limitations:

```text
Single-Mode Fiber
```

### Connection

| Router | Router |
| ------ | ------ |
| R1     | R3     |

---

# Step 6: Connect R3 and R4

Distance:

```text
250 meters
```

UTP maximum distance:

```text
100 meters
```

Multimode fiber maximum distance:

```text
550 meters
```

Since 250 meters is within multimode limits:

```text
Multimode Fiber
```

### Connection

| Router | Router |
| ------ | ------ |
| R3     | R4     |

---

# Final Topology Summary

## Straight-Through Connections

* PC1 ↔ SW3
* PC2 ↔ SW4
* PC3 ↔ SW7
* SRV1 ↔ SW8
* SW1 ↔ R2
* SW2 ↔ R2
* SW5 ↔ R4
* SW6 ↔ R4

---

## Crossover Connections

* SW3 ↔ SW1
* SW1 ↔ SW2
* SW4 ↔ SW2
* SW7 ↔ SW5
* SW5 ↔ SW6
* SW8 ↔ SW6
* R2 ↔ R1

---

## Fiber Connections

### Single-Mode Fiber

* R1 ↔ R3 (3 km)

### Multimode Fiber

* R3 ↔ R4 (250 m)

---

# Key Concepts Learned

### Different Device Types

Use:

```text
Straight-Through Cable
```

---

### Same Device Types

Use:

```text
Crossover Cable
```

---

### UTP Distance Limit

```text
100 meters
```

---

### Multimode Fiber Distance

Typically:

```text
Up to 550 meters
```

---

### Single-Mode Fiber Distance

Supports:

```text
Several kilometers
```

---

# CCNA Exam Tips

✅ PC ↔ Switch = Straight-through

✅ Router ↔ Switch = Straight-through

✅ Switch ↔ Switch = Crossover

✅ Router ↔ Router = Crossover

✅ UTP maximum distance = 100 m

✅ Multimode fiber = Medium-distance links

✅ Single-mode fiber = Long-distance links

✅ Modern devices often use Auto MDI-X, but CCNA questions may still test cable-selection concepts.

---

# Lab Summary

In this lab, we applied Ethernet cabling rules to build a complete network topology. We selected cable types based on:

* Device type
* Pin transmission behavior
* Distance requirements
* Fiber-optic capabilities

Understanding these cabling decisions is essential for both the CCNA exam and real-world network deployments.
