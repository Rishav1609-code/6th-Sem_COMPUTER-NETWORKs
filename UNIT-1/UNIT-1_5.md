# Computer Networks – Unit 1 Notes

# 5. OSI Reference Model (MAKAUT Exam-Oriented Notes)

---

# 📖 Topic Overview

The **OSI (Open Systems Interconnection) Reference Model** is a conceptual framework developed by the International Organization for Standardization (ISO) to standardize network communication.

It divides network communication into **7 layers**, where each layer performs a specific function and communicates with adjacent layers.

The OSI model helps:

✅ Understand network communication

✅ Troubleshoot network problems

✅ Design network protocols

✅ Ensure interoperability between different systems

---

# 🎯 Learning Objectives

After studying this chapter, you will be able to:

✔ Explain the OSI model.

✔ Describe all 7 layers and their functions.

✔ Understand encapsulation and decapsulation.

✔ Identify devices operating at different layers.

✔ Compare OSI and TCP/IP models.

✔ Answer MAKAUT examination questions.

---

# 5.1 Introduction to OSI Model

---

## Definition

The OSI Reference Model is a seven-layer conceptual framework that describes how data is transmitted from one computer to another over a network.

---

## Why OSI Model Was Needed?

Before OSI:

❌ Different vendors used different communication methods.

❌ Systems were incompatible.

❌ Troubleshooting was difficult.

OSI introduced a standardized architecture.

---

## Basic Structure

```text
+------------------+
| Application (7)  |
+------------------+
| Presentation (6) |
+------------------+
| Session (5)      |
+------------------+
| Transport (4)    |
+------------------+
| Network (3)      |
+------------------+
| Data Link (2)    |
+------------------+
| Physical (1)     |
+------------------+
```

---

# Memory Trick for OSI Layers

### Top to Bottom

👉 **All People Seem To Need Data Processing**

| Layer        | Word       |
| ------------ | ---------- |
| Application  | All        |
| Presentation | People     |
| Session      | Seem       |
| Transport    | To         |
| Network      | Need       |
| Data Link    | Data       |
| Physical     | Processing |

---

# 5.2 Seven Layers of OSI Model

---

# Layer 7 – Application Layer

---

## Definition

The Application Layer provides services directly to end users and application programs.

---

## Functions

✅ User Interface

✅ Network Services

✅ File Transfer

✅ Email Services

✅ Web Services

---

## Common Protocols

* HTTP
* HTTPS
* FTP
* SMTP
* DNS
* DHCP

---

## Examples

* Web Browser
* Email Client
* File Transfer Application

---

## Real-Life Analogy

Customer interacting with a bank clerk.

---

# Layer 6 – Presentation Layer

---

## Definition

Responsible for data representation and formatting.

---

## Main Functions

### 1. Translation

Converts data formats.

Example:

```text
ASCII ↔ Unicode
```

---

### 2. Compression

Reduces data size.

Benefits:

* Faster transmission
* Reduced bandwidth usage

---

### 3. Encryption

Protects data from unauthorized access.

Example:

```text
HELLO
 ↓
XJ8A92#
```

---

## Real-Life Analogy

Translator converting one language into another.

---

# Layer 5 – Session Layer

---

## Definition

Responsible for establishing, managing, and terminating communication sessions.

---

# Functions

---

## 1. Session Establishment

Creates connection between devices.

---

## 2. Session Maintenance

Keeps communication active.

---

## 3. Session Termination

Closes communication session.

---

## Example

Video conference session.

```text
Start Meeting
      ↓
Communication
      ↓
End Meeting
```

---

## Real-Life Analogy

Telephone call process.

---

# Layer 4 – Transport Layer

---

## Definition

Provides reliable end-to-end communication.

---

# Functions

---

## 1. Segmentation

Large data is divided into smaller segments.

---

## 2. Flow Control

Controls transmission rate.

Prevents receiver overload.

---

## 3. Error Control

Detects and corrects errors.

---

## Protocols

* TCP
* UDP

---

# TCP vs UDP

| Feature        | TCP      | UDP            |
| -------------- | -------- | -------------- |
| Connection     | Oriented | Connectionless |
| Reliability    | High     | Low            |
| Speed          | Slower   | Faster         |
| Error Recovery | Yes      | No             |
| Acknowledgment | Yes      | No             |

---

## Transport Layer PDU

```text
Segment
```

---

## Real-Life Analogy

Courier service delivering parcels safely.

---

# Layer 3 – Network Layer

---

## Definition

Responsible for routing packets from source to destination.

---

# Functions

---

## 1. Routing

Determines best path.

---

## 2. Logical Addressing

Uses IP addresses.

---

## 3. Packet Forwarding

Transfers packets between networks.

---

## IP Addressing

Example:

```text
192.168.1.1
```

---

## Protocols

* IP
* ICMP
* ARP

---

## PDU

```text
Packet
```

---

## Real-Life Analogy

GPS finding shortest route.

---

# Layer 2 – Data Link Layer

---

## Definition

Provides node-to-node communication.

---

# Functions

---

## 1. Framing

Converts packets into frames.

---

## 2. MAC Addressing

Uses physical hardware addresses.

Example:

```text
00:1A:2B:3C:4D:5E
```

---

## 3. Error Detection

Detects transmission errors.

---

## Sublayers

### LLC

Logical Link Control

### MAC

Media Access Control

---

## PDU

```text
Frame
```

---

## Real-Life Analogy

Postal envelope carrying address information.

---

# Layer 1 – Physical Layer

---

## Definition

Responsible for transmitting raw bits over communication media.

---

# Functions

---

## 1. Bit Transmission

Transmits 0s and 1s.

---

## 2. Signaling

Converts bits into electrical, optical, or radio signals.

---

## Examples

* Cables
* Connectors
* Hubs

---

## PDU

```text
Bits
```

---

## Real-Life Analogy

Road carrying vehicles.

---

# Complete OSI Layer Summary

| Layer        | Function                             | PDU     |
| ------------ | ------------------------------------ | ------- |
| Application  | User Services                        | Data    |
| Presentation | Translation, Compression, Encryption | Data    |
| Session      | Session Management                   | Data    |
| Transport    | Reliable Communication               | Segment |
| Network      | Routing                              | Packet  |
| Data Link    | Framing                              | Frame   |
| Physical     | Bit Transmission                     | Bits    |

---

# 5.3 Encapsulation and Decapsulation

---

# Encapsulation

Process of adding headers while data moves down the OSI layers.

---

## Sender Side

```text
Data
 ↓
Segment
 ↓
Packet
 ↓
Frame
 ↓
Bits
```

---

## Encapsulation Flow

```text
Application Data
        ↓
Transport Header Added
        ↓
Network Header Added
        ↓
Data Link Header Added
        ↓
Transmission
```

---

# Decapsulation

Process of removing headers at the receiver.

---

## Receiver Side

```text
Bits
 ↓
Frame
 ↓
Packet
 ↓
Segment
 ↓
Data
```

---

## Easy Memory Trick

Encapsulation → Add Information

Decapsulation → Remove Information

---

# 5.4 OSI Layer Devices

---

# 1. Hub

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

# 2. Switch

---

## Layer

Data Link Layer (Layer 2)

---

## Function

Uses MAC addresses to forward frames.

---

## Advantages

* Reduces collisions
* Improves efficiency

---

# 3. Router

---

## Layer

Network Layer (Layer 3)

---

## Function

Routes packets using IP addresses.

---

## Example

Connects different networks.

---

# 4. Gateway

---

## Layer

Operates across all layers

---

## Function

Protocol conversion between different systems.

---

# Device Comparison Table

| Device  | Layer           | Address Used        |
| ------- | --------------- | ------------------- |
| Hub     | Layer 1         | None                |
| Switch  | Layer 2         | MAC Address         |
| Router  | Layer 3         | IP Address          |
| Gateway | Multiple Layers | Protocol Conversion |

---

# Memory Trick

👉 HSRG

Hub → Switch → Router → Gateway

Layer:

1 → 2 → 3 → All

---

# 5.5 OSI vs TCP/IP Model

---

# TCP/IP Model

Developed for practical Internet communication.

---

## TCP/IP Layers

```text
Application
Transport
Internet
Network Access
```

---

# Mapping

| OSI Model    | TCP/IP Model   |
| ------------ | -------------- |
| Application  | Application    |
| Presentation | Application    |
| Session      | Application    |
| Transport    | Transport      |
| Network      | Internet       |
| Data Link    | Network Access |
| Physical     | Network Access |

---

# OSI vs TCP/IP Comparison

| Feature              | OSI             | TCP/IP         |
| -------------------- | --------------- | -------------- |
| Layers               | 7               | 4              |
| Developed By         | ISO             | DARPA          |
| Nature               | Reference Model | Protocol Suite |
| Usage                | Conceptual      | Practical      |
| Protocol Independent | Yes             | No             |

---

# Frequently Asked 2 Marks Questions

### Q1. What is OSI Model?

A seven-layer framework for network communication.

---

### Q2. Which layer performs routing?

Network Layer.

---

### Q3. Which layer performs encryption?

Presentation Layer.

---

### Q4. Which layer uses MAC addresses?

Data Link Layer.

---

### Q5. Which device operates at Layer 3?

Router.

---

# Frequently Asked 5 Marks Questions

### Q1. Explain the functions of Presentation Layer.

### Q2. Explain the functions of Transport Layer.

### Q3. Explain Network Layer.

### Q4. Explain Data Link Layer.

### Q5. Differentiate TCP and UDP.

---

# Frequently Asked 10 Marks Questions

### Q1. Explain all seven layers of OSI model.

### Q2. Draw and explain OSI Reference Model.

### Q3. Explain encapsulation and decapsulation.

### Q4. Compare OSI and TCP/IP models.

### Q5. Explain networking devices and their OSI layers.

---

# Important Viva Questions

### How many layers are in OSI?

7 Layers.

### Which layer interacts with users?

Application Layer.

### Which layer performs encryption?

Presentation Layer.

### Which layer establishes sessions?

Session Layer.

### Which layer performs routing?

Network Layer.

### Which layer handles MAC addressing?

Data Link Layer.

### Which layer transmits bits?

Physical Layer.

---

# Important MCQs

### 1. OSI model contains:

A. 4 Layers

B. 5 Layers

C. 7 Layers

D. 8 Layers

✅ Answer: C

---

### 2. Routing is performed by:

A. Physical Layer

B. Data Link Layer

C. Network Layer

D. Session Layer

✅ Answer: C

---

### 3. Encryption is performed at:

A. Application

B. Presentation

C. Session

D. Transport

✅ Answer: B

---

### 4. Which device operates at Layer 2?

A. Hub

B. Router

C. Switch

D. Gateway

✅ Answer: C

---

### 5. Which device uses IP addresses?

A. Hub

B. Switch

C. Router

D. Repeater

✅ Answer: C

---

### 6. Encapsulation occurs at:

A. Sender

B. Receiver

C. Both

D. None

✅ Answer: A

---

### 7. TCP/IP model contains:

A. 7 Layers

B. 5 Layers

C. 4 Layers

D. 3 Layers

✅ Answer: C

---

# 🚀 One-Page Revision Sheet

### OSI Layers

Application

Presentation

Session

Transport

Network

Data Link

Physical

---

### Layer Functions

Application → User Services

Presentation → Translation, Compression, Encryption

Session → Session Management

Transport → Reliability

Network → Routing

Data Link → Framing

Physical → Bit Transmission

---

### Devices

Hub → Layer 1

Switch → Layer 2

Router → Layer 3

Gateway → All Layers

---

### Encapsulation

Data → Segment → Packet → Frame → Bits

---

### TCP/IP Layers

Application

Transport

Internet

Network Access

---

# ⭐ Most Important MAKAUT Questions

1. Draw and explain the OSI model.
2. Explain functions of all seven layers.
3. Explain encapsulation and decapsulation.
4. Compare TCP and UDP.
5. Compare OSI and TCP/IP models.
6. Explain Hub, Switch, Router and Gateway.
7. Explain routing and logical addressing.
8. Explain MAC addressing and framing.
9. Explain Presentation Layer functions.
10. Write short notes on Session Layer.

---

# 📝 Last-Minute Revision

### Memory Trick

**All People Seem To Need Data Processing**

Application

Presentation

Session

Transport

Network

Data Link

Physical

### Device Layers

Hub → 1

Switch → 2

Router → 3

Gateway → All

### PDU Order

Data → Segment → Packet → Frame → Bits

### Most Repeated MAKAUT Topics

✅ Functions of all 7 layers

✅ Encapsulation & Decapsulation

✅ TCP vs UDP

✅ OSI vs TCP/IP

✅ Hub, Switch, Router, Gateway

✅ Routing, MAC Addressing, IP Addressing

Master these topics and you can answer the majority of OSI-model questions asked in MAKAUT semester examinations.
