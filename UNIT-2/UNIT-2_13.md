# Computer Networks – Unit 2
# 13. Channelization Protocols

> 🎯 MAKAUT Exam Focus:
> FDMA, TDMA, CDMA, Working Principles, Advantages, Disadvantages, Comparison between FDMA, TDMA and CDMA are frequently asked in semester examinations.

---

# 📖 Topic Overview

In a communication network, multiple users often need to share the same transmission medium.

Instead of competing for the channel (as in Random Access Protocols), **Channelization Protocols** divide the available channel into smaller portions and allocate them to different users.

Channelization helps reduce collisions and improves channel utilization.

---

## 🌍 Real-World Relevance

Channelization techniques are widely used in:

- Mobile Communication Systems
- Cellular Networks
- Satellite Communication
- Wireless Communication
- Radio Broadcasting
- 2G, 3G and Early 4G Systems

---

# 🎯 Learning Objectives

After studying this topic, you will be able to:

✔ Understand Channelization

✔ Explain FDMA

✔ Explain TDMA

✔ Explain CDMA

✔ Compare FDMA, TDMA and CDMA

✔ Understand Real-World Applications

---

# Introduction to Channelization

## Definition

Channelization is a technique in which the available bandwidth is divided among multiple users so that they can communicate simultaneously without significant interference.

---

## Why Channelization is Needed?

Without channelization:

```text
User A
User B
User C
      ↓
Same Channel
      ↓
Collision
```

With channelization:

```text
Channel Divided
      ↓
Separate Resources
      ↓
No Collision
```

---

# Types of Channelization Protocols

```text
Channelization
      |
+-----+-----+-----+
|           |     |
FDMA      TDMA  CDMA
```

---

# 13.1 FDMA (Frequency Division Multiple Access)

⭐⭐⭐⭐⭐ Most Important Topic

---

# Definition

FDMA is a channelization technique in which the available frequency spectrum is divided into multiple frequency bands, and each user is assigned a separate frequency band.

---

# Full Form

```text
FDMA

Frequency Division Multiple Access
```

---

# Basic Concept

```text
Available Frequency Spectrum
```

is divided into:

```text
User A → Frequency F1

User B → Frequency F2

User C → Frequency F3
```

---

# Diagram

```text
Frequency Spectrum

+------+------+------+
| F1   | F2   | F3   |
+------+------+------+

UserA UserB UserC
```

---

# Working Principle

### Step 1

Available bandwidth is divided into frequency channels.

### Step 2

Each user receives a dedicated frequency.

### Step 3

All users can communicate simultaneously.

### Step 4

Guard bands are inserted to prevent interference.

---

# Guard Band

## Definition

A small unused frequency range between adjacent channels.

---

## Purpose

Prevents overlap between neighboring channels.

---

# Diagram

```text
F1 | GB | F2 | GB | F3

GB = Guard Band
```

---

# Real-Life Example

Radio Broadcasting:

```text
Radio Station A → 90 MHz

Radio Station B → 95 MHz

Radio Station C → 100 MHz
```

Each station has its own frequency.

---

# Advantages

✅ Simple implementation

✅ Simultaneous transmission possible

✅ No synchronization required

✅ Continuous communication

---

# Disadvantages

❌ Wastage of bandwidth

❌ Guard bands reduce efficiency

❌ Fixed allocation

❌ Less efficient than CDMA

---

# Applications

- Analog Cellular Networks (1G)
- Radio Broadcasting
- Satellite Communication

---

# Important Exam Point

FDMA divides:

```text
Frequency
```

---

# 13.2 TDMA (Time Division Multiple Access)

⭐⭐⭐⭐⭐ Most Important Topic

---

# Definition

TDMA is a channelization technique in which users share the same frequency but transmit during different time slots.

---

# Full Form

```text
TDMA

Time Division Multiple Access
```

---

# Basic Concept

One frequency channel is divided into multiple time slots.

---

# Diagram

```text
Time Slots

+----+----+----+----+
| U1 | U2 | U3 | U1 |
+----+----+----+----+
```

---

# Working Principle

### Step 1

A single frequency is selected.

### Step 2

Time is divided into slots.

### Step 3

Each user gets a unique slot.

### Step 4

Users transmit only during assigned slots.

---

# Example

```text
Slot 1 → User A

Slot 2 → User B

Slot 3 → User C
```

---

# Real-Life Example

GSM Mobile Networks use TDMA.

---

# Advantages

✅ Better bandwidth utilization

✅ No guard band wastage

✅ Supports many users

✅ Flexible resource allocation

---

# Disadvantages

❌ Requires synchronization

❌ Slot management complexity

❌ Delay possible

❌ Idle slots waste resources

---

# Applications

- GSM Networks
- Satellite Communication
- Digital Telephony

---

# Important Exam Point

TDMA divides:

```text
Time
```

---

# 13.3 CDMA (Code Division Multiple Access)

⭐⭐⭐⭐⭐ Most Important MAKAUT Topic

---

# Definition

CDMA is a channelization technique in which all users share the same frequency and time simultaneously but use different unique codes.

---

# Full Form

```text
CDMA

Code Division Multiple Access
```

---

# Basic Concept

Each user receives a unique code.

---

# Diagram

```text
User A → Code A

User B → Code B

User C → Code C
```

All transmit simultaneously.

---

# Working Principle

### Step 1

Assign unique spreading code.

### Step 2

Encode data using the code.

### Step 3

Transmit simultaneously.

### Step 4

Receiver uses matching code to recover data.

---

# Example

```text
User A → Code 1010

User B → Code 1100

User C → Code 0110
```

Receiver identifies each user using the code.

---

# Real-Life Example

3G Mobile Networks use CDMA technology.

---

# Advantages

✅ High capacity

✅ Better bandwidth efficiency

✅ Strong security

✅ Resistant to interference

✅ No strict synchronization

---

# Disadvantages

❌ Complex implementation

❌ Expensive hardware

❌ Complex receiver design

❌ Near-Far Problem

---

# Near-Far Problem

## Definition

A strong nearby signal may overpower a weaker distant signal.

---

# Applications

- 3G Networks
- GPS Systems
- Military Communication
- Wireless Communication

---

# Important Exam Point

CDMA divides:

```text
Code
```

---

# FDMA vs TDMA vs CDMA

⭐⭐⭐⭐⭐ Most Important Comparison Table

| Feature | FDMA | TDMA | CDMA |
|----------|------|------|------|
| Full Form | Frequency Division Multiple Access | Time Division Multiple Access | Code Division Multiple Access |
| Resource Divided By | Frequency | Time | Code |
| Synchronization | Not Required | Required | Minimal |
| Complexity | Low | Medium | High |
| Efficiency | Low | Medium | High |
| Security | Low | Medium | High |
| Capacity | Low | Medium | High |
| Interference Resistance | Low | Medium | High |
| Example | 1G | GSM (2G) | 3G |

---

# Memory Tricks

## FDMA

### F → Frequency

---

## TDMA

### T → Time

---

## CDMA

### C → Code

---

## Easy Shortcut

```text
F → Frequency

T → Time

C → Code
```

---

# Channelization Comparison Diagram

```text
FDMA

|F1|F2|F3|


TDMA

|T1|T2|T3|


CDMA

All Users
Same Time
Same Frequency
Different Codes
```

---

# 🎤 Viva Questions

1. What is Channelization?
2. What is FDMA?
3. What is TDMA?
4. What is CDMA?
5. What is a Guard Band?
6. Why is synchronization required in TDMA?
7. What is a spreading code?
8. What is the Near-Far Problem?
9. Which technique provides highest security?
10. Compare FDMA and TDMA.

---

# 📝 2-Mark Questions

### Q1. Define FDMA.

FDMA divides bandwidth into separate frequency channels.

---

### Q2. Define TDMA.

TDMA divides communication time into slots.

---

### Q3. Define CDMA.

CDMA allows users to share the same frequency using unique codes.

---

### Q4. What is a Guard Band?

Unused frequency space between adjacent channels.

---

### Q5. What is Near-Far Problem?

Strong nearby signals overpower weak distant signals.

---

# 📝 5-Mark Questions

1. Explain FDMA.
2. Explain TDMA.
3. Explain CDMA.
4. Discuss advantages of CDMA.
5. Compare FDMA and TDMA.

---

# 📝 10-Mark Questions

1. Explain Channelization Protocols.
2. Explain FDMA with diagram.
3. Explain TDMA with diagram.
4. Explain CDMA with diagram.
5. Compare FDMA, TDMA and CDMA.

---

# ✅ Important MCQs

### 1. FDMA divides:

A. Time

B. Code

C. Frequency ✅

D. Frames

---

### 2. TDMA divides:

A. Frequency

B. Time ✅

C. Code

D. Data

---

### 3. CDMA divides:

A. Time

B. Frequency

C. Code ✅

D. Frames

---

### 4. Guard Band is used in:

A. TDMA

B. CDMA

C. FDMA ✅

D. Ethernet

---

### 5. GSM primarily uses:

A. CDMA

B. FDMA

C. TDMA ✅

D. CSMA/CD

---

### 6. 3G technology primarily uses:

A. FDMA

B. TDMA

C. CDMA ✅

D. ALOHA

---

### 7. Which technique offers highest security?

A. FDMA

B. TDMA

C. CDMA ✅

D. ALOHA

---

# 📌 One-Page Revision Sheet

## Channelization Protocols

### FDMA

- Frequency Division
- Uses Guard Bands
- 1G Networks

### TDMA

- Time Division
- Uses Time Slots
- GSM Networks

### CDMA

- Code Division
- Uses Unique Codes
- 3G Networks

---

## Quick Comparison

| Protocol | Division |
|-----------|-----------|
| FDMA | Frequency |
| TDMA | Time |
| CDMA | Code |

---

## Most Important Points

- FDMA → Frequency
- TDMA → Time
- CDMA → Code
- CDMA provides highest efficiency
- TDMA requires synchronization
- FDMA requires guard bands

---

# 🚀 Highest Priority MAKAUT Topics

⭐⭐⭐⭐⭐ FDMA Working Principle

⭐⭐⭐⭐⭐ TDMA Working Principle

⭐⭐⭐⭐⭐ CDMA Working Principle

⭐⭐⭐⭐⭐ Guard Band

⭐⭐⭐⭐⭐ Near-Far Problem

⭐⭐⭐⭐⭐ FDMA vs TDMA vs CDMA

⭐⭐⭐⭐ Applications of Channelization

These topics are extremely important for MAKAUT semester examinations, internal assessments, viva examinations, and university theory papers.