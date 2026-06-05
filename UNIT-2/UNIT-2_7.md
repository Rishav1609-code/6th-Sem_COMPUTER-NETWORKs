# Computer Networks – Unit 2
# 7. Medium Access Control (MAC) Sublayer

> 🎯 MAKAUT Exam Focus:
> MAC Sublayer, Channel Allocation Problems, Multiple Access Techniques, Random Access Protocols, Controlled Access Protocols, and Channelization Protocols are among the most frequently asked topics in semester examinations.

---

# 📖 Topic Overview

In a network, multiple devices often share the same communication channel. If two or more devices transmit data simultaneously, collisions may occur.

The **Medium Access Control (MAC) Sublayer** is responsible for controlling access to the shared communication medium and ensuring efficient data transmission.

The MAC Sublayer is a part of the **Data Link Layer (DLL)** and acts as an interface between the Logical Link Control (LLC) Sublayer and the Physical Layer.

---

## 🌍 Real-World Relevance

MAC Sublayer is used in:

- Ethernet Networks
- Wi-Fi Networks
- Mobile Networks
- Satellite Communication
- LAN Technologies
- Wireless Sensor Networks

---

# 🎯 Learning Objectives

After studying this topic, you will be able to:

✔ Understand MAC Sublayer

✔ Explain Channel Allocation Problems

✔ Understand Multiple Access Techniques

✔ Describe Random Access Protocols

✔ Explain Controlled Access Protocols

✔ Understand Channelization Protocols

✔ Compare Different Access Methods

---

# 7.1 Introduction to MAC Sublayer

## Definition

The Medium Access Control (MAC) Sublayer is the lower part of the Data Link Layer responsible for controlling access to the transmission medium.

---

## Position of MAC Sublayer

```text
+----------------------+
| Application Layer    |
+----------------------+
| Transport Layer      |
+----------------------+
| Network Layer        |
+----------------------+
| LLC Sublayer         |
+----------------------+
| MAC Sublayer         |
+----------------------+
| Physical Layer       |
+----------------------+
```

---

## Functions of MAC Sublayer

### 1. Medium Access Control

Determines which device can use the channel.

### 2. Collision Handling

Detects and resolves collisions.

### 3. Physical Addressing

Uses MAC Addresses for communication.

### 4. Frame Transmission

Controls frame delivery over the medium.

### 5. Channel Sharing

Allows multiple devices to share a common channel.

---

## Easy Explanation

Imagine a classroom discussion.

If everyone speaks at the same time:

```text
Confusion
```

The teacher decides who can speak.

Similarly:

```text
MAC Sublayer
      ↓
Controls
Channel Access
```

---

# 7.2 Channel Allocation Problems

⭐⭐⭐⭐ Frequently Asked Theory Topic

---

## Definition

Channel Allocation refers to assigning communication channels to multiple users efficiently.

---

## Problem

Suppose:

```text
Computer A
Computer B
Computer C
Computer D
```

All want to transmit simultaneously.

Result:

```text
Collision
```

---

## Main Challenges

### 1. Collision

Two devices transmit simultaneously.

### 2. Fairness

Every user should get a chance to transmit.

### 3. Efficiency

Channel utilization should be high.

### 4. Delay

Waiting time should be minimized.

---

## Example

```text
A → Send Data

B → Send Data

Same Time
      ↓
Collision
```

---

## Important Exam Point

"Channel Allocation Problems" is a common 5-mark question.

---

# 7.3 Multiple Access Techniques

⭐⭐⭐⭐⭐ Most Important Topic

---

## Definition

Multiple Access Techniques are methods that allow multiple users to share the same communication channel.

---

## Classification

```text
Multiple Access Techniques
            |
    +-------+-------+
    |       |       |
 Random  Controlled Channelization
 Access    Access
```

---

# Types of Multiple Access Techniques

## 1. Random Access

Users transmit whenever they want.

Examples:

- ALOHA
- Slotted ALOHA
- CSMA
- CSMA/CD
- CSMA/CA

---

## 2. Controlled Access

Transmission permission is controlled.

Examples:

- Reservation
- Polling
- Token Passing

---

## 3. Channelization

Channel divided among users.

Examples:

- FDMA
- TDMA
- CDMA

---

# Comparison

| Technique | Access Method |
|------------|--------------|
| Random Access | Compete for Channel |
| Controlled Access | Permission-Based |
| Channelization | Divide Channel |

---

# 7.4 Random Access Protocols

⭐⭐⭐⭐⭐ Very Important MAKAUT Topic

---

## Definition

Random Access Protocols allow devices to transmit whenever they have data.

---

## Characteristics

- No central controller
- Devices compete for channel
- Collision may occur

---

# ALOHA

## Definition

A simple protocol where stations transmit whenever data is available.

---

## Working

```text
Send Data
    ↓
Collision?
    ↓
Yes → Retransmit
```

---

## Advantages

- Simple
- Easy implementation

---

## Disadvantages

- High collision probability

---

# Slotted ALOHA

## Definition

Improved version of ALOHA.

Transmission allowed only at slot boundaries.

---

## Advantages

- Fewer collisions
- Better efficiency

---

# CSMA

Carrier Sense Multiple Access

---

## Working

```text
Listen Channel
      ↓
Idle?
      ↓
Yes → Transmit
No  → Wait
```

---

## Advantage

Reduces collisions.

---

# CSMA/CD

Carrier Sense Multiple Access with Collision Detection

Used in Ethernet.

---

## Working

```text
Listen
   ↓
Transmit
   ↓
Collision?
   ↓
Yes
   ↓
Stop Transmission
```

---

# CSMA/CA

Carrier Sense Multiple Access with Collision Avoidance

Used in Wi-Fi.

---

## Working

```text
Listen
   ↓
Wait
   ↓
Transmit
```

---

# Comparison of Random Access Protocols

| Protocol | Collision Handling |
|-----------|-------------------|
| ALOHA | Retransmission |
| Slotted ALOHA | Time Slots |
| CSMA | Listen Before Send |
| CSMA/CD | Detect Collision |
| CSMA/CA | Avoid Collision |

---

# 7.5 Controlled Access Protocols

⭐⭐⭐⭐ Important Topic

---

## Definition

Controlled Access Protocols allow transmission only after obtaining permission.

---

## Types

### 1. Reservation

Users reserve transmission slots.

---

### Working

```text
Reserve Slot
      ↓
Transmit Data
```

---

### Advantages

- No collisions
- Predictable performance

---

# 2. Polling

## Definition

A central controller asks each station whether it wants to transmit.

---

## Working

```text
Controller
      ↓
Station A?
      ↓
Station B?
      ↓
Station C?
```

---

## Advantages

- No collision

---

## Disadvantages

- Polling overhead

---

# 3. Token Passing

⭐⭐⭐⭐ Frequently Asked

---

## Definition

A special frame called Token circulates among stations.

Only the token holder can transmit.

---

## Working

```text
Token
  ↓
Station A
  ↓
Station B
  ↓
Station C
```

---

## Advantages

- No collision
- Fair access

---

## Disadvantages

- Token loss problem

---

# Controlled Access Comparison

| Protocol | Key Idea |
|-----------|----------|
| Reservation | Reserve Slot |
| Polling | Central Control |
| Token Passing | Token Based |

---

# 7.6 Channelization Protocols

⭐⭐⭐⭐⭐ Most Important Topic

---

## Definition

Channelization divides a channel into smaller portions and assigns them to users.

---

## Types

```text
Channelization
      |
  +---+---+---+
  |   |   |
 FDMA TDMA CDMA
```

---

# FDMA

Frequency Division Multiple Access

---

## Working

```text
Frequency Spectrum

|User1|User2|User3|
```

Each user gets a separate frequency band.

---

## Advantages

- Simple
- Continuous transmission

---

## Disadvantages

- Wastes bandwidth

---

# TDMA

Time Division Multiple Access

---

## Working

```text
Time Slots

User1
User2
User3
User1
```

Each user gets a time slot.

---

## Advantages

- Efficient bandwidth use

---

## Disadvantages

- Synchronization required

---

# CDMA

Code Division Multiple Access

⭐⭐⭐⭐⭐ Very Important

---

## Working

All users transmit simultaneously using unique codes.

---

```text
User1 → Code A

User2 → Code B

User3 → Code C
```

---

## Advantages

- High capacity
- Secure communication

---

## Disadvantages

- Complex implementation

---

# FDMA vs TDMA vs CDMA

| Feature | FDMA | TDMA | CDMA |
|----------|------|------|------|
| Division Basis | Frequency | Time | Code |
| Synchronization | No | Yes | No |
| Complexity | Low | Medium | High |
| Efficiency | Medium | High | Very High |
| Security | Low | Low | High |

---

# 🎤 Viva Questions

1. What is MAC Sublayer?
2. What are the functions of MAC Sublayer?
3. What is channel allocation?
4. What is collision?
5. Define Random Access Protocol.
6. What is ALOHA?
7. What is CSMA?
8. Difference between CSMA/CD and CSMA/CA?
9. What is Token Passing?
10. What is FDMA?

---

# 📝 2-Mark Questions

### Q1. Define MAC Sublayer.

MAC Sublayer controls access to the transmission medium.

---

### Q2. What is channel allocation?

Assigning communication channels to users.

---

### Q3. Define CSMA.

Carrier Sense Multiple Access is a protocol that senses the channel before transmitting.

---

### Q4. What is Token Passing?

A controlled access technique using a circulating token.

---

### Q5. What is FDMA?

Frequency Division Multiple Access divides frequency spectrum among users.

---

# 📝 5-Mark Questions

1. Explain MAC Sublayer functions.
2. Explain channel allocation problems.
3. Describe Random Access Protocols.
4. Explain Controlled Access Protocols.
5. Explain FDMA, TDMA, and CDMA.

---

# 📝 10-Mark Questions

1. Explain MAC Sublayer in detail.
2. Discuss Multiple Access Techniques.
3. Explain Random Access Protocols with examples.
4. Explain Controlled Access Protocols with examples.
5. Compare FDMA, TDMA, and CDMA.

---

# ✅ Important MCQs

### 1. MAC stands for:

A. Multiple Access Channel

B. Medium Access Control ✅

C. Media Allocation Control

D. Multi Access Communication

---

### 2. CSMA/CD is used in:

A. Wi-Fi

B. Ethernet ✅

C. Bluetooth

D. Satellite

---

### 3. CSMA/CA is used in:

A. Ethernet

B. Wi-Fi ✅

C. Token Ring

D. FDDI

---

### 4. Token Passing belongs to:

A. Random Access

B. Controlled Access ✅

C. Channelization

D. Routing

---

### 5. FDMA divides channel by:

A. Code

B. Time

C. Frequency ✅

D. Frame

---

# 📌 One-Page Revision Sheet

## MAC Sublayer

- Controls channel access
- Handles collisions
- Uses MAC addresses

## Access Techniques

### Random Access

- ALOHA
- Slotted ALOHA
- CSMA
- CSMA/CD
- CSMA/CA

### Controlled Access

- Reservation
- Polling
- Token Passing

### Channelization

- FDMA
- TDMA
- CDMA

---

# 🧠 Memory Tricks

## Random Access

**A-S-C-C-C**

ALOHA

Slotted ALOHA

CSMA

CSMA/CD

CSMA/CA

---

## Controlled Access

**RPT**

Reservation

Polling

Token Passing

---

## Channelization

**FTC**

Frequency → FDMA

Time → TDMA

Code → CDMA

---

# 🚀 Highest Priority MAKAUT Topics

⭐⭐⭐⭐⭐ MAC Sublayer Functions

⭐⭐⭐⭐⭐ Multiple Access Techniques

⭐⭐⭐⭐⭐ Random Access Protocols

⭐⭐⭐⭐⭐ CSMA/CD vs CSMA/CA

⭐⭐⭐⭐⭐ FDMA vs TDMA vs CDMA

⭐⭐⭐⭐ Token Passing

⭐⭐⭐⭐ Channel Allocation Problems

These topics should be prepared thoroughly for theory exams, viva examinations, and internal assessments.

