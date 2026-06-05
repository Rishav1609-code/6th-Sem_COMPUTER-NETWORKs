# Computer Networks – Unit 1 Notes

# 7. LAN (Local Area Network) (MAKAUT Exam-Oriented Notes)

---

# 📖 Topic Overview

A **Local Area Network (LAN)** is a network that connects computers and devices within a limited geographical area such as a room, office, laboratory, school, university building, or home.

LAN is the most commonly used network type because it provides:

✅ High-speed communication

✅ Resource sharing

✅ Internet access

✅ Centralized management

Modern LANs can be either **Wired LANs** (Ethernet) or **Wireless LANs (WLANs)** (Wi-Fi).

---

# 🎯 Learning Objectives

After studying this chapter, you will be able to:

✔ Explain LAN and its characteristics.

✔ Understand Ethernet and Ethernet standards.

✔ Differentiate Wired and Wireless LAN.

✔ Explain LAN connecting devices.

✔ Understand VLAN concepts and architecture.

✔ Compare Static VLAN and Dynamic VLAN.

✔ Explain VLAN tagging and Inter-VLAN communication.

✔ Answer MAKAUT semester examination questions.

---

# 7.1 Introduction to LAN

---

## Definition

A Local Area Network (LAN) is a network that connects computers and devices within a small geographical area for communication and resource sharing.

---

## Simple Explanation

A LAN allows multiple devices to communicate and share resources such as:

* Printers
* Files
* Internet Connection
* Storage Devices

---

## Example

```text
PC1
  │
PC2 ── Switch ── Server
  │
PC3
```

---

## Real-Life Examples

* School Computer Lab
* Office Network
* Home Wi-Fi Network
* University Department Network

---

# 7.2 Characteristics of LAN

---

## 1. Small Geographical Area

Usually covers:

* Room
* Building
* Office
* Campus Block

---

## 2. High Data Transfer Rate

Typical speed:

* 100 Mbps
* 1 Gbps
* 10 Gbps

---

## 3. Low Error Rate

Because communication distance is short.

---

## 4. Private Ownership

Usually owned by:

* Organizations
* Schools
* Companies
* Homes

---

## 5. Resource Sharing

Supports sharing of:

* Printers
* Files
* Software
* Internet

---

## 6. Easy Maintenance

Networks are easier to manage due to limited coverage.

---

# Advantages of LAN

✅ High Speed

✅ Low Cost

✅ Resource Sharing

✅ Easy Expansion

✅ Centralized Control

---

# Disadvantages of LAN

❌ Limited Coverage

❌ Security Threats

❌ Server Failure Can Affect Users

❌ Initial Setup Cost

---

# Memory Trick

👉 SHLPR

S → Small Area

H → High Speed

L → Low Error

P → Private Ownership

R → Resource Sharing

---

# 7.3 Wired LAN

---

## Definition

A Wired LAN uses physical cables to connect devices.

---

## Structure

```text
PC ── Cable ── Switch ── Cable ── Server
```

---

# Ethernet

---

## Definition

Ethernet is the most widely used LAN technology.

Developed by:

Robert Metcalfe

---

## Features

✅ High Speed

✅ Reliable

✅ Easy Implementation

✅ Low Cost

---

## Ethernet Frame

```text
Header | Data | Trailer
```

---

## Ethernet Uses

* Offices
* Schools
* Data Centers
* Enterprises

---

# Ethernet Standards

---

## IEEE Standard

Ethernet is standardized under:

### IEEE 802.3

---

## Common Ethernet Standards

| Standard   | Speed    |
| ---------- | -------- |
| 10Base-T   | 10 Mbps  |
| 100Base-T  | 100 Mbps |
| 1000Base-T | 1 Gbps   |
| 10GBase-T  | 10 Gbps  |

---

### Memory Trick

10 → 100 → 1000 → 10000

Increasing Ethernet Speeds

---

# LAN Devices

---

## NIC (Network Interface Card)

Provides network connectivity.

Each NIC has:

* MAC Address

---

## Ethernet Cable

Connects devices physically.

---

## Switch

Connects multiple devices efficiently.

---

## Router

Connects LAN to Internet.

---

# 7.4 Wireless LAN (WLAN)

---

## Definition

A Wireless LAN uses radio waves instead of cables.

---

## Example

Home Wi-Fi Network

---

## Structure

```text
Laptop
     │
 Smartphone
     │
Access Point
     │
 Router
     │
Internet
```

---

# Wi-Fi Architecture

---

## Components

### Station (STA)

Wireless client device.

Examples:

* Mobile
* Laptop
* Tablet

---

### Access Point (AP)

Central wireless communication device.

---

### Distribution System

Connects multiple access points.

---

### Internet Connection

Provides external network access.

---

## Architecture Diagram

```text
Laptop
    │
Mobile
    │
Access Point
    │
Switch
    │
Internet
```

---

# Access Point (AP)

---

## Definition

An Access Point is a networking device that allows wireless devices to connect to a wired network.

---

## Functions

✅ Wireless Communication

✅ Signal Broadcasting

✅ Device Authentication

✅ Internet Access

---

## Real-Life Example

Home Wi-Fi Router

---

# Wireless Standards (IEEE 802.11)

---

## Definition

IEEE 802.11 defines Wi-Fi standards.

---

## Major Standards

| Standard | Frequency | Speed        |
| -------- | --------- | ------------ |
| 802.11a  | 5 GHz     | 54 Mbps      |
| 802.11b  | 2.4 GHz   | 11 Mbps      |
| 802.11g  | 2.4 GHz   | 54 Mbps      |
| 802.11n  | 2.4/5 GHz | 600 Mbps     |
| 802.11ac | 5 GHz     | Several Gbps |
| 802.11ax | Wi-Fi 6   | Higher Speed |

---

### Exam Tip

IEEE 802.11 = Wi-Fi

IEEE 802.3 = Ethernet

Frequently Asked MCQ

---

# Wired LAN vs WLAN

| Feature      | Wired LAN | WLAN        |
| ------------ | --------- | ----------- |
| Medium       | Cable     | Radio Waves |
| Mobility     | No        | Yes         |
| Speed        | Higher    | Lower       |
| Installation | Difficult | Easy        |
| Security     | Higher    | Lower       |
| Cost         | Higher    | Lower       |

---

# 7.5 Connecting LANs

---

# 1. Repeater

---

## Layer

Physical Layer (Layer 1)

---

## Function

Regenerates weak signals.

---

## Diagram

```text
LAN ─ Repeater ─ LAN
```

---

## Advantage

Extends communication distance.

---

# 2. Hub

---

## Layer

Physical Layer (Layer 1)

---

## Function

Broadcasts data to all devices.

---

## Characteristics

* No intelligence
* No filtering

---

# 3. Bridge

---

## Layer

Data Link Layer (Layer 2)

---

## Function

Connects LAN segments.

Uses MAC Address filtering.

---

## Advantage

Reduces unnecessary traffic.

---

# 4. Switch

---

## Layer

Data Link Layer (Layer 2)

---

## Function

Forwards frames using MAC addresses.

---

## Advantages

✅ High Speed

✅ Collision Reduction

✅ Efficient Communication

---

# 5. Router

---

## Layer

Network Layer (Layer 3)

---

## Function

Routes packets between networks.

Uses IP addresses.

---

# 6. Gateway

---

## Layer

Operates across multiple layers

---

## Function

Connects networks using different protocols.

---

# Device Comparison Table

| Device   | Layer | Address Used        |
| -------- | ----- | ------------------- |
| Repeater | 1     | None                |
| Hub      | 1     | None                |
| Bridge   | 2     | MAC                 |
| Switch   | 2     | MAC                 |
| Router   | 3     | IP                  |
| Gateway  | All   | Protocol Conversion |

---

### Memory Trick

👉 RHBSRG

Repeater

Hub

Bridge

Switch

Router

Gateway

---

# 7.6 Virtual LAN (VLAN)

---

# VLAN Concept

---

## Definition

A VLAN (Virtual Local Area Network) logically divides a physical LAN into multiple virtual networks.

---

## Why VLAN?

Without VLAN:

```text
All Devices
     │
 Same Broadcast Domain
```

Too much traffic.

---

With VLAN:

```text
VLAN 10 → HR
VLAN 20 → Finance
VLAN 30 → Sales
```

Traffic becomes isolated.

---

# VLAN Architecture

---

## Example

```text
Switch
 │
 ├── VLAN 10 (HR)
 │
 ├── VLAN 20 (Finance)
 │
 └── VLAN 30 (Sales)
```

---

## Benefits

* Better Security
* Reduced Broadcast Traffic
* Easier Management

---

# Static VLAN

---

## Definition

Administrator manually assigns ports to VLANs.

---

## Example

```text
Port 1 → VLAN 10
Port 2 → VLAN 20
Port 3 → VLAN 30
```

---

## Advantages

✅ Simple

✅ Secure

---

## Disadvantages

❌ Manual Configuration

---

# Dynamic VLAN

---

## Definition

Devices are automatically assigned VLANs.

Based on:

* MAC Address
* User Identity
* Policies

---

## Advantages

✅ Automatic Management

✅ Flexible

---

## Disadvantages

❌ Complex Configuration

---

# Static VLAN vs Dynamic VLAN

| Feature        | Static | Dynamic   |
| -------------- | ------ | --------- |
| Assignment     | Manual | Automatic |
| Complexity     | Low    | High      |
| Flexibility    | Low    | High      |
| Administration | Simple | Advanced  |

---

# VLAN Tagging

---

## Definition

A VLAN ID is inserted into Ethernet frames.

This process is called VLAN Tagging.

---

## Standard

### IEEE 802.1Q

---

## Example

```text
Frame
 │
 VLAN ID = 20
```

---

## Purpose

Allows multiple VLANs to share the same switch link.

---

# Advantages of VLAN

---

✅ Better Security

✅ Reduced Broadcast Traffic

✅ Improved Performance

✅ Easier Management

✅ Better Scalability

✅ Department-Based Segmentation

---

# Inter-VLAN Communication

---

## Problem

Different VLANs cannot communicate directly.

Example:

```text
VLAN 10 ↔ VLAN 20
```

Communication blocked.

---

## Solution

Use a Router or Layer-3 Switch.

---

## Diagram

```text
VLAN 10
    │
 Router
    │
VLAN 20
```

---

## Importance

Allows communication between departments.

---

# Frequently Asked 2 Marks Questions

### Q1. What is LAN?

A network covering a limited geographical area.

---

### Q2. What is Ethernet?

A widely used LAN technology.

---

### Q3. What is WLAN?

A LAN using wireless communication.

---

### Q4. What is VLAN?

Logical division of a physical LAN.

---

### Q5. Which standard defines Wi-Fi?

IEEE 802.11

---

# Frequently Asked 5 Marks Questions

### Q1. Explain characteristics of LAN.

### Q2. Explain Ethernet technology.

### Q3. Explain Access Point.

### Q4. Compare Wired LAN and WLAN.

### Q5. Explain VLAN architecture.

---

# Frequently Asked 10 Marks Questions

### Q1. Explain LAN with characteristics.

### Q2. Explain Ethernet and Ethernet standards.

### Q3. Explain WLAN architecture.

### Q4. Explain networking devices used for connecting LANs.

### Q5. Explain VLAN, VLAN tagging, and Inter-VLAN communication.

---

# Important Viva Questions

### Which IEEE standard defines Ethernet?

IEEE 802.3

### Which IEEE standard defines Wi-Fi?

IEEE 802.11

### Which device regenerates signals?

Repeater

### Which device uses IP addresses?

Router

### What is VLAN?

Logical segmentation of LAN.

### Which standard defines VLAN tagging?

IEEE 802.1Q

---

# Important MCQs

### 1. LAN covers:

A. World

B. Country

C. Small Area

D. City

✅ Answer: C

---

### 2. Ethernet standard is:

A. IEEE 802.1

B. IEEE 802.3

C. IEEE 802.11

D. IEEE 802.15

✅ Answer: B

---

### 3. Wi-Fi standard is:

A. IEEE 802.3

B. IEEE 802.11

C. IEEE 802.1Q

D. IEEE 802.15

✅ Answer: B

---

### 4. VLAN tagging standard is:

A. IEEE 802.3

B. IEEE 802.11

C. IEEE 802.1Q

D. IEEE 802.15

✅ Answer: C

---

### 5. Which device operates at Layer 3?

A. Hub

B. Switch

C. Router

D. Bridge

✅ Answer: C

---

### 6. Which device regenerates signals?

A. Router

B. Repeater

C. Gateway

D. Switch

✅ Answer: B

---

# 🚀 One-Page Revision Sheet

### LAN

* Small Area Network
* High Speed
* Private Ownership

### Ethernet

* IEEE 802.3
* Wired LAN

### WLAN

* IEEE 802.11
* Wireless LAN

### Connecting Devices

* Repeater → Layer 1
* Hub → Layer 1
* Bridge → Layer 2
* Switch → Layer 2
* Router → Layer 3
* Gateway → Multiple Layers

### VLAN

* Logical LAN Division
* IEEE 802.1Q Tagging
* Better Security

---

# ⭐ Most Important MAKAUT Questions

1. Define LAN and explain its characteristics.
2. Explain Ethernet and Ethernet standards.
3. Explain WLAN architecture.
4. Explain Access Point and Wi-Fi standards.
5. Compare Wired LAN and WLAN.
6. Explain Repeater, Hub, Bridge, Switch, Router, and Gateway.
7. Explain VLAN architecture.
8. Compare Static VLAN and Dynamic VLAN.
9. Explain VLAN Tagging.
10. Explain Inter-VLAN Communication.

---

# 📝 Last-Minute Revision

### Remember

**Ethernet → IEEE 802.3**

**Wi-Fi → IEEE 802.11**

**VLAN Tagging → IEEE 802.1Q**

### Device Layers

Repeater → L1

Hub → L1

Bridge → L2

Switch → L2

Router → L3

Gateway → Multiple Layers

### VLAN Benefits

Security

Performance

Scalability

Broadcast Control

### Most Repeated MAKAUT Topics

✅ Ethernet Standards

✅ WLAN Architecture

✅ Repeater vs Hub vs Bridge vs Switch vs Router

✅ VLAN Architecture

✅ Static VLAN vs Dynamic VLAN

✅ Inter-VLAN Communication

These are among the most frequently asked questions from the LAN chapter in MAKAUT Computer Networks examinations.
