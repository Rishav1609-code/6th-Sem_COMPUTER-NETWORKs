# Computer Networks – Unit 2
# 11. CSMA/CD (Carrier Sense Multiple Access with Collision Detection)

> 🎯 MAKAUT Exam Focus:
> CSMA/CD, Collision Detection, Backoff Algorithm, Binary Exponential Backoff, CSMA/CD Operation, Ethernet and CSMA/CD, Advantages and Limitations are among the most frequently asked topics in semester examinations.

---

# 📖 Topic Overview

CSMA/CD (Carrier Sense Multiple Access with Collision Detection) is an enhancement of CSMA used primarily in traditional Ethernet networks.

Before transmitting data, a station listens to the channel. If the channel is free, it starts transmission. If a collision occurs during transmission, the station detects it, stops transmitting immediately, and retransmits after a random waiting period.

CSMA/CD significantly improves network efficiency by reducing wasted bandwidth due to collisions.

---

## 🌍 Real-World Relevance

CSMA/CD was widely used in:

- Ethernet LANs
- Office Networks
- Campus Networks
- Early Internet Infrastructure
- Shared Bus Networks

---

# 🎯 Learning Objectives

After studying this topic, you will be able to:

✔ Understand CSMA/CD

✔ Explain Carrier Sense

✔ Explain Multiple Access

✔ Understand Collision Detection

✔ Describe Backoff Algorithm

✔ Explain Binary Exponential Backoff

✔ Understand CSMA/CD Operation

✔ Explain Ethernet and CSMA/CD Relationship

---

# 11.1 Introduction to CSMA/CD

⭐⭐⭐⭐⭐ Most Important Topic

---

## Definition

CSMA/CD stands for:

```text
Carrier Sense Multiple Access
with
Collision Detection
```

It is a network access protocol where stations:

1. Sense the channel.
2. Transmit if idle.
3. Detect collisions during transmission.
4. Stop transmission if collision occurs.
5. Retransmit later.

---

## Why CSMA/CD Was Introduced?

Problem in CSMA:

```text
Collisions Still Occur
```

Solution:

```text
Detect Collision Immediately
```

This minimizes bandwidth wastage.

---

## Basic Idea

```text
Listen
   ↓
Transmit
   ↓
Collision?
   ↓
+-----+-----+
|           |
No         Yes
|           |
Success    Stop
             ↓
          Retransmit
```

---

# 11.2 Carrier Sense

⭐⭐⭐⭐ Frequently Asked

---

## Definition

Carrier Sense means checking whether the channel is busy or idle before transmission.

---

## Working

### Channel Idle

```text
Transmit
```

### Channel Busy

```text
Wait
```

---

## Example

Imagine entering a room.

Before speaking:

```text
Check if someone is speaking.
```

If nobody is speaking:

```text
Start Speaking.
```

---

## Benefits

✅ Fewer collisions

✅ Better channel utilization

✅ Higher efficiency

---

# 11.3 Multiple Access

⭐⭐⭐⭐ Frequently Asked

---

## Definition

Multiple Access means multiple devices share the same communication medium.

---

## Example

```text
Computer A
Computer B
Computer C
Computer D
```

All use the same Ethernet cable.

---

## Challenge

If multiple stations transmit together:

```text
Collision
```

occurs.

---

## Role in CSMA/CD

Allows:

```text
Many Stations
        ↓
Share One Channel
```

while minimizing collisions.

---

# 11.4 Collision Detection

⭐⭐⭐⭐⭐ Most Important Topic

---

## Definition

Collision Detection is the ability of a station to detect that another station is transmitting simultaneously.

---

## Collision Example

```text
Station A → Frame

Station B → Frame

Same Time
    ↓
Collision
```

---

## Detection Process

### Step 1

Transmit frame.

### Step 2

Monitor channel while transmitting.

### Step 3

Compare sent signal with received signal.

### Step 4

If mismatch detected:

```text
Collision Found
```

---

## Jam Signal

After collision detection:

```text
Send Jam Signal
```

to notify all stations.

---

## Purpose of Jam Signal

- Inform all stations
- Stop current transmission
- Trigger retransmission process

---

# Collision Detection Diagram

```text
Station A ----\
               \
                X Collision
               /
Station B ----/

      ↓

Jam Signal
```

---

# 11.5 Backoff Algorithm

⭐⭐⭐⭐⭐ Frequently Asked

---

## Definition

Backoff Algorithm determines how long a station should wait before retransmitting after a collision.

---

## Why Needed?

Without waiting:

```text
Collision
     ↓
Immediate Retransmission
     ↓
Another Collision
```

---

## Solution

```text
Collision
     ↓
Random Wait
     ↓
Retransmit
```

---

## Working

### Step 1

Collision occurs.

### Step 2

Choose random waiting time.

### Step 3

Wait.

### Step 4

Retransmit.

---

# Example

```text
Station A waits 2 ms

Station B waits 5 ms
```

A transmits first.

Collision avoided.

---

# 11.6 Binary Exponential Backoff

⭐⭐⭐⭐⭐ Extremely Important MAKAUT Topic

---

## Definition

Binary Exponential Backoff is the collision recovery algorithm used in Ethernet CSMA/CD.

After every collision, the waiting range doubles.

---

## Working Principle

After:

### 1st Collision

Choose random number:

```text
0 or 1
```

---

### 2nd Collision

Choose random number:

```text
0 to 3
```

---

### 3rd Collision

Choose random number:

```text
0 to 7
```

---

### nth Collision

Choose random number:

```text
0 to (2ⁿ − 1)
```

---

## Formula

:contentReference[oaicite:0]{index=0}

Where:

- K = Random Number
- n = Number of Collisions

---

## Advantages

✅ Reduces repeated collisions

✅ Fair retransmission

✅ Improves network stability

---

## Memory Trick

### Binary Exponential Backoff

```text
1 Collision → 2 Choices

2 Collisions → 4 Choices

3 Collisions → 8 Choices
```

"Doubles Every Time"

---

# 11.7 CSMA/CD Operation

⭐⭐⭐⭐⭐ Most Important Long Question

---

# Step-by-Step Operation

### Step 1

Station has data.

---

### Step 2

Sense channel.

---

### Step 3

If idle:

```text
Transmit
```

---

### Step 4

Monitor channel.

---

### Step 5

Collision occurs?

```text
Yes
```

---

### Step 6

Send Jam Signal.

---

### Step 7

Apply Binary Exponential Backoff.

---

### Step 8

Retransmit.

---

# Complete Flow Diagram

```text
Data Ready
     |
Sense Channel
     |
Idle?
     |
+----+----+
|         |
Yes       No
|         |
Transmit Wait
    |
Collision?
    |
+---+---+
|       |
No     Yes
|       |
Done   Jam Signal
          |
      Backoff
          |
     Retransmit
```

---

# 11.8 Ethernet and CSMA/CD

⭐⭐⭐⭐⭐ Frequently Asked

---

## Relationship

Traditional Ethernet uses CSMA/CD.

---

## Why Ethernet Uses CSMA/CD?

Because:

```text
Multiple Devices
       ↓
Shared Cable
```

Collisions are possible.

---

## Ethernet Operation

```text
Sense
  ↓
Transmit
  ↓
Detect Collision
  ↓
Backoff
  ↓
Retransmit
```

---

## Modern Ethernet

Modern switched Ethernet uses:

```text
Full Duplex
```

Therefore:

```text
No Collisions
```

Hence:

```text
CSMA/CD Not Required
```

---

## Important Exam Point

### Traditional Ethernet

Uses CSMA/CD

### Modern Switched Ethernet

Does Not Use CSMA/CD

---

# 11.9 Advantages and Limitations

---

# Advantages of CSMA/CD

✅ Reduces bandwidth wastage

✅ Detects collisions quickly

✅ Efficient channel utilization

✅ Fair access mechanism

✅ Better than Pure CSMA

✅ Widely used in Ethernet

---

# Limitations of CSMA/CD

❌ Collision still occurs

❌ Performance degrades under heavy load

❌ Not suitable for wireless networks

❌ Requires collision detection hardware

❌ Not used in modern switched Ethernet

---

# CSMA vs CSMA/CD

| Feature | CSMA | CSMA/CD |
|----------|--------|----------|
| Carrier Sense | Yes | Yes |
| Collision Detection | No | Yes |
| Efficiency | Lower | Higher |
| Retransmission Control | Basic | Better |
| Ethernet Support | Limited | Full |

---

# 🎤 Viva Questions

1. What is CSMA/CD?
2. What does CD stand for?
3. What is carrier sensing?
4. What is collision detection?
5. What is a Jam Signal?
6. Why is Backoff Algorithm used?
7. Define Binary Exponential Backoff.
8. Why was CSMA/CD used in Ethernet?
9. Why is CSMA/CD not used in modern Ethernet?
10. State one limitation of CSMA/CD.

---

# 📝 2-Mark Questions

### Q1. Define CSMA/CD.

CSMA/CD is a protocol that senses the channel, detects collisions, and retransmits data after a backoff period.

---

### Q2. What is Collision Detection?

The process of identifying simultaneous transmissions.

---

### Q3. What is a Jam Signal?

A signal transmitted after collision detection to notify all stations.

---

### Q4. Define Backoff Algorithm.

A waiting mechanism used before retransmission.

---

### Q5. What is Binary Exponential Backoff?

A collision recovery algorithm where the waiting range doubles after each collision.

---

# 📝 5-Mark Questions

1. Explain CSMA/CD.
2. Explain collision detection process.
3. Describe Backoff Algorithm.
4. Explain Binary Exponential Backoff.
5. Explain Ethernet and CSMA/CD relationship.

---

# 📝 10-Mark Questions

1. Explain CSMA/CD operation with diagram.
2. Explain collision detection and recovery.
3. Discuss Binary Exponential Backoff with examples.
4. Explain Ethernet working using CSMA/CD.
5. Discuss advantages and limitations of CSMA/CD.

---

# ✅ Important MCQs

### 1. CSMA/CD stands for:

A. Carrier Sense Multiple Access with Collision Detection ✅

B. Carrier Signal Multiple Access with Collision Division

C. Central Switching Multiple Access

D. Collision Sense Multiple Access

---

### 2. CSMA/CD is primarily associated with:

A. Ethernet ✅

B. Wi-Fi

C. Bluetooth

D. ATM

---

### 3. After collision detection, a station sends:

A. ACK

B. CRC

C. Jam Signal ✅

D. Token

---

### 4. Binary Exponential Backoff is used for:

A. Error Detection

B. Routing

C. Collision Recovery ✅

D. Encryption

---

### 5. Modern Switched Ethernet uses CSMA/CD.

A. True

B. False ✅

---

### 6. CSMA/CD is not suitable for:

A. Ethernet

B. Shared Bus LAN

C. Wireless Networks ✅

D. LAN Communication

---

# 📌 One-Page Revision Sheet

## CSMA/CD

- Sense Channel
- Transmit
- Detect Collision
- Send Jam Signal
- Backoff
- Retransmit

---

## Key Concepts

### Carrier Sense

Check Channel First

### Multiple Access

Many Devices Share Channel

### Collision Detection

Detect Simultaneous Transmission

### Jam Signal

Notify All Stations

### Binary Exponential Backoff

Waiting Range Doubles After Every Collision

---

## Formula

Binary Exponential Backoff:

:contentReference[oaicite:1]{index=1}

---

# 🧠 Memory Tricks

## CSMA/CD Steps

### S-T-D-J-B-R

- S = Sense
- T = Transmit
- D = Detect Collision
- J = Jam Signal
- B = Backoff
- R = Retransmit

---

## Binary Exponential Backoff

### DDD Rule

"Doubles Delay Dynamically"

---

# 🚀 Highest Priority MAKAUT Topics

⭐⭐⭐⭐⭐ CSMA/CD Concept

⭐⭐⭐⭐⭐ Collision Detection

⭐⭐⭐⭐⭐ Jam Signal

⭐⭐⭐⭐⭐ Backoff Algorithm

⭐⭐⭐⭐⭐ Binary Exponential Backoff

⭐⭐⭐⭐⭐ CSMA/CD Operation

⭐⭐⭐⭐⭐ Ethernet and CSMA/CD

⭐⭐⭐⭐ Advantages and Limitations

These topics are extremely important for MAKAUT semester examinations, internal assessments, viva examinations, and university theory papers.