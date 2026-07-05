# CCNA 200-301 Notes - Day 4

# Cisco IOS CLI (Command Line Interface)

## Overview

Cisco IOS (Internetwork Operating System) is the operating system used on Cisco networking devices such as:

* Routers
* Switches
* Firewalls

The primary method used by network engineers to configure Cisco devices is the **CLI (Command Line Interface)**.

This lesson introduces:

* Cisco IOS
* CLI modes
* Console connections
* Configuration files
* Password protection
* Configuration saving
* Basic IOS commands

---

# Cisco IOS

## Definition

Cisco IOS is the operating system used on Cisco networking devices.

### Examples

| Device       | Operating System |
| ------------ | ---------------- |
| Windows PC   | Windows          |
| Apple Mac    | macOS            |
| Cisco Router | Cisco IOS        |

---

## Important Note

Cisco IOS is NOT related to:

```text
Apple iOS
```

used on iPhones and iPads.

---

# CLI vs GUI

## CLI

### Full Form

```text
Command Line Interface
```

### Characteristics

* Text-based
* Faster for experienced engineers
* Preferred by most network professionals
* Used throughout CCNA

---

## GUI

### Full Form

```text
Graphical User Interface
```

### Example

Cisco ASDM firewall management software.

### Characteristics

* Graphical
* Easier for beginners
* Less common in enterprise networking

---

# Connecting to a Cisco Device

## Console Connection

The most common method for initial device configuration.

---

## Console Ports

Cisco devices typically provide:

### RJ45 Console Port

### USB Mini-B Console Port

---

# Rollover Cable

Used to connect a PC to the RJ45 console port.

---

## Pin Layout

| Side A | Side B |
| ------ | ------ |
| Pin 1  | Pin 8  |
| Pin 2  | Pin 7  |
| Pin 3  | Pin 6  |
| Pin 4  | Pin 5  |
| Pin 5  | Pin 4  |
| Pin 6  | Pin 3  |
| Pin 7  | Pin 2  |
| Pin 8  | Pin 1  |

---

## Important

A rollover cable is NOT the same as:

* Straight-through cable
* Crossover cable

---

# Terminal Emulator

After connecting physically, a terminal emulator is required.

### Common Example

```text
PuTTY
```

---

# Cisco Default Console Settings

These settings are important for CCNA exams.

| Setting           | Value    |
| ----------------- | -------- |
| Speed (Baud Rate) | 9600 bps |
| Data Bits         | 8        |
| Stop Bits         | 1        |
| Parity            | None     |
| Flow Control      | None     |

---

# Cisco CLI Modes

Cisco IOS has different operating modes.

---

# User EXEC Mode

## Prompt

```text
Router>
```

---

## Characteristics

* Default mode after login
* Limited access
* Can view basic information
* Cannot modify configuration

---

## Symbol

```text
>
```

---

# Entering Privileged EXEC Mode

Command:

```bash
enable
```

Shortcut:

```bash
en
```

---

# Privileged EXEC Mode

## Prompt

```text
Router#
```

---

## Characteristics

* Full monitoring access
* View configuration
* Save configuration
* Restart device

---

## Symbol

```text
#
```

---

# Entering Global Configuration Mode

Full Command:

```bash
configure terminal
```

Shortcut:

```bash
conf t
```

---

## Prompt

```text
Router(config)#
```

---

## Characteristics

* Used to modify device configuration
* Most configuration commands entered here

---

# CLI Help Features

## Question Mark (?)

Displays available commands.

Example:

```bash
?
```

---

## Context-Sensitive Help

Example:

```bash
e?
```

Displays commands beginning with "e".

Output may include:

```text
enable
exit
```

---

# Command Shortcuts

Cisco IOS allows abbreviated commands.

---

## Examples

| Full Command        | Shortcut |
| ------------------- | -------- |
| enable              | en       |
| exit                | ex       |
| configure terminal  | conf t   |
| show running-config | sh run   |

---

## Rule

The shortcut must uniquely identify the command.

Example:

```bash
en
```

works because only:

```text
enable
```

matches.

---

# Configuring an Enable Password

Purpose:

Protect access to Privileged EXEC Mode.

---

## Command

```bash
enable password CCNA
```

---

## Notes

* Case-sensitive
* Stored in configuration

Example:

```text
CCNA
≠
ccna
```

---

# Testing the Password

After exiting to User EXEC Mode:

```bash
enable
```

IOS requests a password.

Password characters are not displayed.

---

# Configuration Files

Cisco devices maintain two configuration files.

---

# Running Configuration

## Name

```text
running-config
```

---

## Purpose

Active configuration currently used by the device.

---

## View Command

```bash
show running-config
```

Shortcut:

```bash
sh run
```

---

# Startup Configuration

## Name

```text
startup-config
```

---

## Purpose

Configuration loaded after reboot.

---

## View Command

```bash
show startup-config
```

---

# Saving Configuration

Changes made to running-config are NOT automatically saved.

If the device reloads before saving:

```text
Configuration is lost.
```

---

# Save Methods

## Method 1

```bash
write
```

---

## Method 2

```bash
write memory
```

---

## Method 3

```bash
copy running-config startup-config
```

---

## CCNA Recommendation

Most engineers use:

```bash
copy running-config startup-config
```

---

# Password Encryption

Without encryption:

```bash
enable password CCNA
```

appears in plain text.

This is a security risk.

---

# Service Password Encryption

Command:

```bash
service password-encryption
```

---

## Purpose

Encrypts passwords displayed in configuration files.

---

## Example

Before:

```text
enable password CCNA
```

After:

```text
enable password 7 08026F6028
```

---

## Type 7 Encryption

The number:

```text
7
```

indicates Cisco Type 7 encryption.

---

## Important

Type 7 encryption is weak and easily cracked.

---

# Enable Secret

A more secure method.

---

## Command

```bash
enable secret Cisco
```

---

## Benefits

* Automatically encrypted
* More secure than enable password
* Uses MD5 hashing

---

## Example

```text
enable secret 5 ...
```

---

## Meaning of Number 5

```text
Type 5 = MD5
```

---

# Enable Password vs Enable Secret

| Feature                 | Enable Password | Enable Secret |
| ----------------------- | --------------- | ------------- |
| Plain Text Possible     | Yes             | No            |
| Automatically Encrypted | No              | Yes           |
| More Secure             | No              | Yes           |
| Recommended             | No              | Yes           |

---

# Important Exam Fact

If both are configured:

```bash
enable password CCNA

enable secret Cisco
```

Only:

```text
enable secret
```

is used.

The enable password is ignored.

---

# Using "do" Command

Allows Privileged EXEC commands inside Configuration Mode.

---

## Example

```bash
do show running-config
```

---

## Shortcut Example

```bash
do sh run
```

---

# Removing Commands

Use:

```bash
no
```

before a command.

---

## Example

Disable password encryption:

```bash
no service password-encryption
```

---

# Service Password-Encryption Summary

## When Enabled

### Existing Passwords

Encrypted

### Future Passwords

Encrypted

### Enable Secret

Always encrypted

---

## When Disabled

### Existing Passwords

Remain encrypted

### Future Passwords

Not encrypted

### Enable Secret

Still encrypted

---

# CLI Modes Summary

| Mode                 | Prompt          |
| -------------------- | --------------- |
| User EXEC            | Router>         |
| Privileged EXEC      | Router#         |
| Global Configuration | Router(config)# |

---

# Essential Commands Summary

## Navigation Commands

```bash
enable
configure terminal
exit
```

---

## Security Commands

```bash
enable password PASSWORD
enable secret PASSWORD
service password-encryption
```

---

## Configuration Display Commands

```bash
show running-config
show startup-config
```

---

## Save Commands

```bash
write
write memory
copy running-config startup-config
```

---

## Utility Commands

```bash
do
no
?
```

---

# CCNA Exam Tips

### Remember Default Console Settings

```text
9600
8
1
None
None
```

(Baud Rate, Data Bits, Stop Bits, Parity, Flow Control)

---

### Know Prompt Symbols

```text
>
User EXEC

#
Privileged EXEC

(config)#
Global Configuration
```

---

### Most Secure Privileged Mode Password

```bash
enable secret
```

---

### Most Common Save Command

```bash
copy running-config startup-config
```

---

# Quick Revision

✅ Cisco IOS is Cisco's operating system.

✅ CLI is the primary configuration interface.

✅ Rollover cable connects to RJ45 console ports.

✅ PuTTY is a common terminal emulator.

✅ User EXEC prompt = >

✅ Privileged EXEC prompt = #

✅ Global Configuration prompt = (config)#

✅ enable enters Privileged EXEC mode.

✅ configure terminal enters Global Configuration mode.

✅ enable secret is more secure than enable password.

✅ service password-encryption encrypts passwords in configuration files.

✅ running-config is active configuration.

✅ startup-config loads after reboot.

✅ Configuration must be saved manually.

---

# Interview Questions

### Q1. What is Cisco IOS?

The operating system used on Cisco networking devices.

### Q2. What command enters Privileged EXEC mode?

```bash
enable
```

### Q3. What command enters Global Configuration Mode?

```bash
configure terminal
```

### Q4. Which password method is more secure?

```bash
enable secret
```

### Q5. What command displays the active configuration?

```bash
show running-config
```

### Q6. How do you save configuration changes?

```bash
copy running-config startup-config
```

### Q7. What cable is used for RJ45 console connections?

Rollover cable.

---

# Lesson Summary

The Cisco IOS CLI is the primary interface used to configure Cisco networking devices. Network engineers use CLI modes such as User EXEC, Privileged EXEC, and Global Configuration Mode to monitor and manage devices.

This lesson introduced console connections, configuration files, password security, command shortcuts, configuration saving, and essential IOS commands that will be used throughout the remainder of the CCNA course.
