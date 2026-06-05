# Computer Networks – Unit 2
# 14. CDMA (Code Division Multiple Access)

> 🎯 MAKAUT Exam Focus:
> CDMA, Spread Spectrum, Orthogonal Codes, Chip Sequence, Encoding Process, Decoding Process, Advantages, Disadvantages, and Applications of CDMA are among the most frequently asked topics in semester examinations.

---

# 📖 Topic Overview

CDMA (Code Division Multiple Access) is an advanced channelization technique that allows multiple users to transmit data simultaneously over the same frequency band and at the same time.

Unlike FDMA and TDMA, CDMA separates users using unique codes instead of frequencies or time slots.

Each user is assigned a unique code sequence, allowing the receiver to identify and recover the intended signal even when many users transmit together.

---

## 🌍 Real-World Relevance

CDMA is used in:

- 3G Mobile Networks
- GPS Systems
- Satellite Communication
- Military Communication
- Wireless Communication
- Secure Data Transmission

---

# 🎯 Learning Objectives

After studying this topic, you will be able to:

✔ Understand CDMA

✔ Explain Spread Spectrum

✔ Understand Orthogonal Codes

✔ Explain Chip Sequences

✔ Describe Encoding Process

✔ Describe Decoding Process

✔ Analyze Advantages and Limitations

✔ Understand Real-World Applications

---

# 14.1 Introduction to CDMA

⭐⭐⭐⭐⭐ Most Important Topic

---

## Definition

CDMA (Code Division Multiple Access) is a multiple access technique in which all users share the same frequency spectrum and transmit simultaneously using unique codes.

---

## Full Form

```text
CDMA

Code Division Multiple Access
```

---

## Basic Concept

Instead of dividing:

```text
Frequency → FDMA

Time → TDMA
```

CDMA divides:

```text
Code
```

---

## Working Idea

```text
User A → Code A

User B → Code B

User C → Code C
```

All users transmit at the same time.

Receiver identifies data using the corresponding code.

---

# CDMA Concept Diagram

```text
Shared Channel

User A → Code A
User B → Code B
User C → Code C

        ↓

Same Frequency
Same Time

        ↓

Receiver Uses Codes
```

---

## Why CDMA?

Problems in FDMA and TDMA:

- Limited capacity
- Bandwidth wastage
- Fixed allocation

CDMA solves these issues by allowing multiple simultaneous transmissions.

---

# Key Features

✅ Same Frequency

✅ Same Time

✅ Different Codes

✅ High Capacity

✅ Better Security

---

# 14.2 Spread Spectrum Concept

⭐⭐⭐⭐⭐ Extremely Important

---

## Definition

Spread Spectrum is a transmission technique in which the original signal is spread over a much wider bandwidth than required.

---

## Purpose

- Reduce interference
- Improve security
- Increase reliability
- Support multiple users

---

## Basic Principle

Original Signal:

```text
Narrow Band
```

After Spreading:

```text
Wide Band
```

---

# Diagram

```text
Original Signal

|----|


Spread Spectrum

|------------------------|
```

---

## Types of Spread Spectrum

```text
Spread Spectrum
      |
+-----+-----+
|           |
DSSS      FHSS
```

---

### DSSS (Direct Sequence Spread Spectrum)

Used in CDMA.

Each bit is replaced by multiple chips.

---

### FHSS (Frequency Hopping Spread Spectrum)

Frequency changes rapidly according to a pattern.

---

## Advantages

✅ Better noise resistance

✅ Improved security

✅ Multiple user support

---

# 14.3 Orthogonal Codes

⭐⭐⭐⭐⭐ Frequently Asked

---

## Definition

Orthogonal Codes are code sequences that do not interfere with each other.

---

## Meaning

When two orthogonal codes are compared:

```text
Result = 0
```

---

## Example

```text
Code A = +1 +1 -1 -1

Code B = +1 -1 +1 -1
```

Multiply and add:

```text
(+1)(+1)
(+1)(-1)
(-1)(+1)
(-1)(-1)

= 1 -1 -1 +1

= 0
```

Therefore:

```text
Orthogonal
```

---

## Importance

Orthogonal codes allow:

```text
Many Users
     ↓
Same Channel
     ↓
No Interference
```

---

# Important Exam Point

Orthogonal Codes are the foundation of CDMA.

---

# 14.4 Chip Sequence

⭐⭐⭐⭐⭐ Most Important Topic

---

## Definition

A Chip is the smallest unit of spread-spectrum coding.

A Chip Sequence is the code pattern assigned to a user.

---

## Difference Between Bit and Chip

| Bit | Chip |
|-------|-------|
| Original Data | Encoded Data |
| Larger Unit | Smaller Unit |
| Information Unit | Spreading Unit |

---

## Example

Data Bit:

```text
1
```

Chip Sequence:

```text
+1 +1 -1 -1
```

---

## Purpose

- Spread data
- Increase security
- Differentiate users

---

# Chip Sequence Diagram

```text
Bit

1

↓

Chip Sequence

+1 +1 -1 -1
```

---

# 14.5 Encoding Process

⭐⭐⭐⭐⭐ Frequently Asked Long Question

---

## Definition

Encoding is the process of converting data bits into spread-spectrum signals using chip sequences.

---

## Encoding Rules

### Data Bit = 1

Transmit chip sequence directly.

---

### Data Bit = 0

Transmit complement of chip sequence.

---

## Example

User Code:

```text
+1 +1 -1 -1
```

Data:

```text
1
```

Encoded Signal:

```text
+1 +1 -1 -1
```

---

Data:

```text
0
```

Encoded Signal:

```text
-1 -1 +1 +1
```

---

# Encoding Flow

```text
Data Bit
     |
Assign Code
     |
Multiply
     |
Spread Signal
```

---

## Advantages

✅ Supports multiple users

✅ Improves reliability

✅ Enhances security

---

# 14.6 Decoding Process

⭐⭐⭐⭐⭐ Very Important

---

## Definition

Decoding is the process of recovering the original data using the same code sequence.

---

## Working Principle

Receiver:

1. Receives combined signal.
2. Uses corresponding user code.
3. Performs correlation.
4. Recovers original data.

---

# Decoding Steps

### Step 1

Receive signal.

### Step 2

Multiply by user code.

### Step 3

Add results.

### Step 4

Determine bit value.

---

# Example

Received Signal:

```text
+1 +1 -1 -1
```

User Code:

```text
+1 +1 -1 -1
```

Multiplication:

```text
1 +1 +1 +1
```

Sum:

```text
4
```

Positive result:

```text
Bit = 1
```

---

# Decoding Diagram

```text
Received Signal
       |
Multiply By Code
       |
Correlation
       |
Original Data
```

---

# Important Exam Point

Encoding uses:

```text
Chip Sequence
```

Decoding uses:

```text
Correlation
```

---

# 14.7 Advantages of CDMA

⭐⭐⭐⭐ Frequently Asked

---

## Advantages

✅ High Capacity

✅ Better Spectrum Utilization

✅ Strong Security

✅ Resistance to Noise

✅ Supports Simultaneous Users

✅ Better Voice Quality

✅ Soft Handoff Support

✅ Less Interference

---

## Industry Benefits

- Efficient mobile communication
- Secure communication
- High user density support

---

# 14.8 Disadvantages of CDMA

⭐⭐⭐⭐ Frequently Asked

---

## Disadvantages

❌ Complex System Design

❌ Expensive Implementation

❌ Difficult Synchronization

❌ Near-Far Problem

❌ Complex Receivers

❌ Power Control Required

---

# Near-Far Problem

⭐⭐⭐⭐⭐ Very Important

---

## Definition

A nearby transmitter may overpower signals from distant transmitters.

---

# Example

```text
User A (Near)

User B (Far)
```

Signal from User A may dominate User B.

---

## Solution

```text
Power Control
```

---

# 14.9 Applications of CDMA

⭐⭐⭐⭐ Frequently Asked

---

## 1. Mobile Communication

3G Networks

---

## 2. GPS Systems

Satellite navigation.

---

## 3. Military Communication

Secure communication channels.

---

## 4. Satellite Communication

Multiple user access.

---

## 5. Wireless Networks

Efficient bandwidth utilization.

---

## 6. Secure Communication Systems

Protection against interception.

---

# FDMA vs TDMA vs CDMA

⭐⭐⭐⭐⭐ Most Important Comparison

| Feature | FDMA | TDMA | CDMA |
|----------|------|------|------|
| Resource Shared By | Frequency | Time | Code |
| Capacity | Low | Medium | High |
| Efficiency | Low | Medium | High |
| Security | Low | Medium | High |
| Complexity | Low | Medium | High |
| Synchronization | No | Yes | Minimal |
| Interference Resistance | Low | Medium | High |

---

# Memory Tricks

## CDMA

### C = Code

### D = Different Users

### M = Multiple Access

### A = All Together

---

## Spread Spectrum

### Spread = Wider Bandwidth

---

## Encoding Rule

```text
1 → Same Code

0 → Complement Code
```

---

# 🎤 Viva Questions

1. What is CDMA?
2. What is Spread Spectrum?
3. What are Orthogonal Codes?
4. Define Chip Sequence.
5. What is Encoding?
6. What is Decoding?
7. What is Correlation?
8. What is Near-Far Problem?
9. Why is CDMA more secure?
10. State one application of CDMA.

---

# 📝 2-Mark Questions

### Q1. Define CDMA.

CDMA is a multiple access technique where users share the same channel using unique codes.

---

### Q2. What is Spread Spectrum?

A technique that spreads a signal over a wider bandwidth.

---

### Q3. Define Orthogonal Codes.

Codes whose correlation value is zero.

---

### Q4. What is a Chip?

The smallest unit of a spread-spectrum code.

---

### Q5. What is Near-Far Problem?

A nearby strong signal overpowering a distant weak signal.

---

# 📝 5-Mark Questions

1. Explain Spread Spectrum.
2. Explain Orthogonal Codes.
3. Explain Chip Sequence.
4. Discuss Advantages of CDMA.
5. Explain Near-Far Problem.

---

# 📝 10-Mark Questions

1. Explain CDMA with diagram.
2. Explain Encoding and Decoding in CDMA.
3. Discuss Spread Spectrum and Orthogonal Codes.
4. Explain Advantages and Disadvantages of CDMA.
5. Compare FDMA, TDMA and CDMA.

---

# ✅ Important MCQs

### 1. CDMA stands for:

A. Code Division Multiple Access ✅

B. Channel Division Multiple Access

C. Central Data Multiple Access

D. Code Data Management Access

---

### 2. CDMA separates users using:

A. Frequency

B. Time

C. Code ✅

D. Frames

---

### 3. CDMA commonly uses:

A. DSSS ✅

B. CSMA/CD

C. Token Ring

D. ALOHA

---

### 4. Orthogonal codes have correlation value:

A. 1

B. -1

C. 0 ✅

D. 2

---

### 5. A Chip is:

A. Data Packet

B. Frame

C. Smallest Coding Unit ✅

D. Header

---

### 6. Near-Far Problem occurs in:

A. FDMA

B. TDMA

C. CDMA ✅

D. Ethernet

---

### 7. Which technology offers highest capacity?

A. FDMA

B. TDMA

C. CDMA ✅

D. ALOHA

---

# 📌 One-Page Revision Sheet

## CDMA

- Same Frequency
- Same Time
- Different Codes

---

## Important Concepts

### Spread Spectrum

Signal spread over wide bandwidth

### Orthogonal Codes

Correlation = 0

### Chip Sequence

User Identification Code

### Encoding

Bit × Chip Sequence

### Decoding

Correlation Process

---

## Key Rules

```text
Bit 1 → Same Code

Bit 0 → Complement Code
```

---

## Important Problems

- Near-Far Problem
- Power Control Requirement

---

# 🚀 Highest Priority MAKAUT Topics

⭐⭐⭐⭐⭐ CDMA Concept

⭐⭐⭐⭐⭐ Spread Spectrum

⭐⭐⭐⭐⭐ Orthogonal Codes

⭐⭐⭐⭐⭐ Chip Sequence

⭐⭐⭐⭐⭐ Encoding Process

⭐⭐⭐⭐⭐ Decoding Process

⭐⭐⭐⭐⭐ Near-Far Problem

⭐⭐⭐⭐⭐ FDMA vs TDMA vs CDMA

⭐⭐⭐⭐ Applications of CDMA

These topics are extremely important for MAKAUT semester examinations, internal assessments, viva examinations, and university theory papers.