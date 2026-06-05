# Computer Networks – Unit 2
# 8. Random Access Protocols

> 🎯 MAKAUT Exam Focus:
> Random Access, Contention-Based Access, Collision, Collision Resolution Techniques, ALOHA, CSMA, CSMA/CD, and CSMA/CA are among the most frequently asked topics in semester examinations.

---

# 📖 Topic Overview

In a shared communication channel, multiple devices may need to transmit data at any time.

Random Access Protocols allow devices to access the channel whenever they have data to send without obtaining prior permission.

Since multiple devices compete for the same channel, collisions may occur. Therefore, collision detection and resolution mechanisms become important.

---

## 🌍 Real-World Relevance

Random Access Protocols are used in:

- Ethernet Networks
- Wi-Fi Networks
- Wireless LANs
- Mobile Communication
- Sensor Networks
- Internet Communication

---

# 🎯 Learning Objectives

After studying this topic, you will be able to:

✔ Understand Random Access Protocols

✔ Explain Contention-Based Access

✔ Understand Collision Concepts

✔ Explain Collision Resolution Techniques

✔ Compare Different Random Access Methods

✔ Understand Practical Applications

---

# 8.1 Introduction to Random Access

⭐⭐⭐⭐⭐ Most Important Theory Topic

---

## Definition

Random Access is a channel access method in which stations transmit data whenever they have data to send.

No central controller decides transmission order.

---

## Easy Explanation

Imagine a classroom discussion.

Students speak whenever they want.

```text
Student A → Speak

Student B → Speak

Student C → Speak
```

No permission is required.

Similarly:

```text
Device A
Device B
Device C

Transmit Anytime
```

---

## Characteristics

### 1. Decentralized Access

No central authority.

### 2. Shared Medium

All devices share the same channel.

### 3. Possibility of Collision

Multiple transmissions may overlap.

### 4. Simple Implementation

Easy to implement.

---

## General Working

```text
Have Data?
    |
   Yes
    |
Transmit
    |
Collision?
    |
+---+---+
|       |
No     Yes
|       |
Success Retransmit
```

---

## Advantages

✅ Simple

✅ Flexible

✅ No Scheduling Required

✅ Suitable for Dynamic Networks

---

## Disadvantages

❌ Collisions Possible

❌ Reduced Efficiency at High Traffic

❌ Retransmission Overhead

---

# 8.2 Contention-Based Access

⭐⭐⭐⭐ Frequently Asked

---

## Definition

Contention-Based Access is a technique where multiple stations compete for access to the communication channel.

---

## Easy Explanation

Consider a single-door classroom.

```text
Student A
Student B
Student C
```

All attempt to enter simultaneously.

Competition occurs.

Similarly:

```text
Station A
Station B
Station C

Compete for Channel
```

---

## Working

### Step 1

Device wants to transmit.

### Step 2

Checks channel status.

### Step 3

Attempts transmission.

### Step 4

If collision occurs:

```text
Wait
↓
Retry
```

---

## Examples

### ALOHA

Transmit anytime.

### Slotted ALOHA

Transmit only during slots.

### CSMA

Listen before transmitting.

---

## Features

- Shared channel
- Competition among users
- Dynamic access
- Collision handling required

---

# Contention-Based Access Flow

```text
Need to Send Data
        |
        V
 Compete for Channel
        |
        V
  Channel Available?
        |
   +----+----+
   |         |
  Yes       No
   |         |
Transmit   Wait
```

---

# 8.3 Collision Concept

⭐⭐⭐⭐⭐ Very Important Topic

---

## Definition

A collision occurs when two or more stations transmit simultaneously on the same channel.

---

## Example

```text
Station A
      \
       \
        > Channel
       /
      /
Station B
```

Both transmit simultaneously.

Result:

```text
Collision
```

---

## Easy Explanation

Two people speak at the same time.

```text
Voice Overlap
```

No one understands clearly.

Similarly:

```text
Data Overlap
```

Transmission fails.

---

# Causes of Collision

### 1. Simultaneous Transmission

Multiple devices send data together.

### 2. Propagation Delay

Signal takes time to travel.

### 3. Shared Medium

All devices use same channel.

---

# Effects of Collision

### Data Corruption

Frames become unusable.

### Retransmission

Frames must be sent again.

### Bandwidth Waste

Network resources wasted.

### Increased Delay

Communication slows down.

---

# Collision Diagram

```text
Station A ----\
               \
                X Collision
               /
Station B ----/
```

---

## Important Exam Point

Definition, causes, and effects of collision are frequently asked in 2-mark and 5-mark questions.

---

# 8.4 Collision Resolution Techniques

⭐⭐⭐⭐⭐ Most Important MAKAUT Topic

---

## Definition

Collision Resolution Techniques are methods used to detect, avoid, and recover from collisions.

---

# Types of Collision Resolution Techniques

```text
Collision Resolution
        |
   +----+----+
   |         |
Detection  Avoidance
```

---

# 1. Retransmission Technique

## Working

After collision:

```text
Wait
↓
Retransmit
```

Used in:

- ALOHA
- Slotted ALOHA

---

## Advantages

- Simple

---

## Disadvantages

- More delay

---

# 2. Backoff Algorithm

⭐⭐⭐⭐ Important

---

## Definition

After collision, station waits for a random period before retransmission.

---

## Working

```text
Collision
     ↓
Random Wait
     ↓
Retransmit
```

---

## Why Needed?

Prevents repeated collisions.

---

## Example

```text
Station A waits 2 ms

Station B waits 5 ms
```

A transmits first.

Collision avoided.

---

# 3. CSMA/CD

Carrier Sense Multiple Access with Collision Detection

⭐⭐⭐⭐⭐ Frequently Asked

---

## Used In

Ethernet Networks

---

## Working

### Step 1

Listen to channel.

### Step 2

If idle:

```text
Transmit
```

### Step 3

Detect collision.

### Step 4

Stop transmission.

### Step 5

Apply Backoff Algorithm.

### Step 6

Retransmit.

---

## Flow Diagram

```text
Listen
   |
Idle?
   |
+--+--+
|     |
Yes   No
|     |
Tx   Wait
|
Collision?
|
+--+--+
|     |
No   Yes
|     |
Done Stop
      |
 Backoff
      |
 Retransmit
```

---

# Advantages

✅ Efficient

✅ Reduces repeated collisions

✅ Widely used in Ethernet

---

# Disadvantages

❌ Not suitable for wireless networks

❌ Collision still possible

---

# 4. CSMA/CA

Carrier Sense Multiple Access with Collision Avoidance

⭐⭐⭐⭐⭐ Very Important

---

## Used In

Wi-Fi Networks

---

## Working

Instead of detecting collisions:

```text
Avoid Collisions
```

before transmission.

---

## Steps

1. Listen to channel.
2. Wait if busy.
3. Use random delay.
4. Transmit data.

---

## Advantages

✅ Suitable for wireless communication

✅ Reduces collision probability

---

## Disadvantages

❌ Additional overhead

❌ More complex

---

# Comparison of Collision Resolution Techniques

| Technique | Method |
|------------|---------|
| Retransmission | Send Again |
| Backoff Algorithm | Random Wait |
| CSMA/CD | Detect Collision |
| CSMA/CA | Avoid Collision |

---

# ALOHA vs CSMA

| Feature | ALOHA | CSMA |
|----------|--------|--------|
| Channel Sensing | No | Yes |
| Collision Rate | High | Lower |
| Efficiency | Low | Higher |
| Complexity | Simple | More Complex |

---

# CSMA/CD vs CSMA/CA

| Feature | CSMA/CD | CSMA/CA |
|----------|----------|----------|
| Full Form | Collision Detection | Collision Avoidance |
| Used In | Ethernet | Wi-Fi |
| Collision Handling | Detects | Avoids |
| Efficiency | High | High |
| Wireless Support | No | Yes |

---

# 🎤 Viva Questions

1. What is Random Access?
2. What is Contention-Based Access?
3. Define collision.
4. Why do collisions occur?
5. What is CSMA?
6. What is CSMA/CD?
7. What is CSMA/CA?
8. What is a Backoff Algorithm?
9. Difference between CSMA/CD and CSMA/CA?
10. What is retransmission?

---

# 📝 2-Mark Questions

### Q1. Define Random Access.

Random Access allows devices to transmit whenever they have data.

---

### Q2. What is Contention-Based Access?

A method where stations compete for channel access.

---

### Q3. What is Collision?

Simultaneous transmission by multiple stations causing data corruption.

---

### Q4. Define CSMA/CD.

Carrier Sense Multiple Access with Collision Detection.

---

### Q5. What is Backoff Algorithm?

A random waiting technique used after collision.

---

# 📝 5-Mark Questions

1. Explain Random Access Protocols.
2. Explain Contention-Based Access.
3. Describe collision and its causes.
4. Explain collision resolution techniques.
5. Compare CSMA/CD and CSMA/CA.

---

# 📝 10-Mark Questions

1. Explain Random Access Protocols in detail.
2. Discuss Contention-Based Access and collision handling.
3. Explain collision resolution techniques with diagrams.
4. Compare ALOHA, CSMA, CSMA/CD, and CSMA/CA.
5. Explain CSMA/CD and CSMA/CA with examples.

---

# ✅ Important MCQs

### 1. Random Access allows:

A. Scheduled Transmission

B. Transmission Anytime ✅

C. Reserved Transmission

D. Controlled Transmission

---

### 2. Collision occurs when:

A. One Station Transmits

B. Two Stations Transmit Simultaneously ✅

C. ACK Received

D. Frame Stored

---

### 3. CSMA/CD is used in:

A. Wi-Fi

B. Ethernet ✅

C. Bluetooth

D. Satellite

---

### 4. CSMA/CA is used in:

A. Ethernet

B. Wi-Fi ✅

C. Token Ring

D. ATM

---

### 5. Backoff Algorithm is used to:

A. Increase Collisions

B. Detect Errors

C. Delay Retransmission Randomly ✅

D. Compress Data

---

# 📌 One-Page Revision Sheet

## Random Access

- Transmit Anytime
- No Central Controller
- Shared Medium

## Contention-Based Access

- Users Compete
- Collision Possible

## Collision

- Simultaneous Transmission
- Data Corruption
- Retransmission Required

## Resolution Techniques

- Retransmission
- Backoff Algorithm
- CSMA/CD
- CSMA/CA

---

# 🧠 Memory Tricks

## Random Access Protocols

### ACCC

- A = ALOHA
- C = CSMA
- C = CSMA/CD
- C = CSMA/CA

---

## Collision Resolution

### RBCC

- R = Retransmission
- B = Backoff
- C = CSMA/CD
- C = CSMA/CA

---

## CSMA/CD vs CSMA/CA

### D → Ethernet

Collision Detection

### A → Wi-Fi

Collision Avoidance

---

# 🚀 Highest Priority MAKAUT Topics

⭐⭐⭐⭐⭐ Random Access

⭐⭐⭐⭐⭐ Collision Concept

⭐⭐⭐⭐⭐ Collision Resolution Techniques

⭐⭐⭐⭐⭐ CSMA/CD

⭐⭐⭐⭐⭐ CSMA/CA

⭐⭐⭐⭐ Backoff Algorithm

⭐⭐⭐⭐ Contention-Based Access

These topics should be prepared thoroughly for theory examinations, viva examinations, and university semester papers.