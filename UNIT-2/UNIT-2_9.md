# Computer Networks – Unit 2
# 9. ALOHA Protocol

> 🎯 MAKAUT Exam Focus:
> Pure ALOHA, Slotted ALOHA, Vulnerable Time, Throughput, Efficiency, Advantages, Disadvantages, and Pure ALOHA vs Slotted ALOHA are among the most frequently asked topics in semester examinations.

---

# 📖 Topic Overview

ALOHA is one of the earliest Random Access Protocols developed for sharing a common communication channel among multiple users.

In ALOHA, stations transmit data whenever they have data to send. Since multiple stations share the same channel, collisions may occur.

To improve performance, two versions of ALOHA were developed:

1. Pure ALOHA
2. Slotted ALOHA

---

## 🌍 Real-World Relevance

ALOHA concepts are used in:

- Wireless Networks
- Satellite Communication
- Radio Networks
- Sensor Networks
- MAC Protocol Design
- Modern Random Access Techniques

---

# 🎯 Learning Objectives

After studying this topic, you will be able to:

✔ Understand ALOHA Protocol

✔ Explain Pure ALOHA

✔ Explain Slotted ALOHA

✔ Understand Vulnerable Time

✔ Calculate Throughput and Efficiency

✔ Compare Pure and Slotted ALOHA

---

# 9.1 Introduction to ALOHA

⭐⭐⭐⭐ Frequently Asked

---

## Definition

ALOHA is a Random Access Protocol in which stations transmit data whenever they have data to send without checking the channel status.

---

## History

Developed at:

```text
University of Hawaii
```

for wireless communication.

---

## Basic Idea

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

## Characteristics

- No channel sensing
- Simple implementation
- Collision possible
- Retransmission required

---

## Advantages

✅ Easy to implement

✅ No central controller

✅ Suitable for low traffic

---

## Disadvantages

❌ High collision probability

❌ Low efficiency

❌ More retransmissions

---

# 9.2 Pure ALOHA

⭐⭐⭐⭐⭐ Most Important Topic

---

## Definition

In Pure ALOHA, a station transmits whenever data becomes available.

No synchronization is required.

---

## Working Principle

### Step 1

Station gets data.

### Step 2

Immediately transmits.

### Step 3

Waits for ACK.

### Step 4

If collision occurs:

```text
Wait Random Time
↓
Retransmit
```

---

# Flow Diagram

```text
Data Available
      |
      V
Transmit Frame
      |
      V
Receive ACK?
      |
  +---+---+
  |       |
 Yes      No
  |       |
Success Retransmit
```

---

## Example

```text
Station A → Send

Station B → Send

Same Time
      ↓
Collision
```

Both stations retransmit later.

---

# Vulnerable Time

⭐⭐⭐⭐⭐ Frequently Asked Numerical Topic

---

## Definition

Vulnerable Time is the time during which another frame can collide with the current frame.

---

## Pure ALOHA Vulnerable Time

If frame transmission time is:

```text
T
```

then:

```text
Vulnerable Time = 2T
```

---

## Explanation

```text
<---- T ---->
      Frame
<---- T ---->

Total = 2T
```

Any frame transmitted within this interval causes collision.

---

## Throughput

### Formula

Maximum Throughput:


::contentReference[oaicite:0]{index=0}


Where:

- S = Throughput
- G = Offered Load

---

## Maximum Throughput

When:

```text
G = 0.5
```

Maximum:

:contentReference[oaicite:1]{index=1}

---

## Efficiency

```text
18.4%
```

---

# Advantages of Pure ALOHA

✅ Simple

✅ No synchronization needed

✅ Easy implementation

---

# Disadvantages of Pure ALOHA

❌ Very high collision rate

❌ Low efficiency

❌ Poor performance under heavy load

---

# 9.3 Slotted ALOHA

⭐⭐⭐⭐⭐ Most Important MAKAUT Topic

---

## Definition

Slotted ALOHA is an improved version of Pure ALOHA in which time is divided into slots.

Stations can transmit only at the beginning of a slot.

---

# Time Slot Concept

```text
|Slot1|Slot2|Slot3|Slot4|
```

Transmission allowed only at slot boundaries.

---

## Why Introduced?

To reduce collisions.

---

## Working Principle

### Step 1

Time divided into slots.

### Step 2

Station waits for next slot.

### Step 3

Transmits at slot start.

### Step 4

If collision occurs:

```text
Wait Random Slots
↓
Retransmit
```

---

# Flow Diagram

```text
Data Ready
    |
Wait for Slot
    |
Transmit
    |
ACK?
    |
+---+---+
|       |
Yes      No
|       |
Success Retransmit
```

---

# Vulnerable Time

⭐⭐⭐⭐⭐ Frequently Asked

---

## Definition

Time interval during which collision may occur.

---

## Slotted ALOHA Vulnerable Time

```text
Vulnerable Time = T
```

---

## Comparison

Pure ALOHA:

```text
2T
```

Slotted ALOHA:

```text
T
```

---

## Throughput

Maximum Throughput:


::contentReference[oaicite:2]{index=2}


---

## Maximum Throughput

When:

```text
G = 1
```

Maximum:

:contentReference[oaicite:3]{index=3}

---

## Efficiency

```text
36.8%
```

---

# Advantages of Slotted ALOHA

✅ Reduced collisions

✅ Better throughput

✅ Higher efficiency

✅ Better channel utilization

---

# Disadvantages of Slotted ALOHA

❌ Synchronization required

❌ Slot management overhead

❌ Idle slots waste bandwidth

---

# Throughput Comparison

| Protocol | Maximum Throughput |
|-----------|-------------------|
| Pure ALOHA | 18.4% |
| Slotted ALOHA | 36.8% |

---

# Efficiency Comparison

| Protocol | Efficiency |
|-----------|-----------|
| Pure ALOHA | 18.4% |
| Slotted ALOHA | 36.8% |

---

# 9.4 Pure ALOHA vs Slotted ALOHA

⭐⭐⭐⭐⭐ Very Important Comparison

---

| Feature | Pure ALOHA | Slotted ALOHA |
|----------|------------|---------------|
| Synchronization | Not Required | Required |
| Transmission Time | Anytime | Slot Boundaries Only |
| Vulnerable Time | 2T | T |
| Throughput | Lower | Higher |
| Efficiency | 18.4% | 36.8% |
| Collision Probability | Higher | Lower |
| Complexity | Simple | More Complex |
| Channel Utilization | Poor | Better |

---

# Memory Trick

## Pure ALOHA

### P = Poor Performance

- Vulnerable Time = 2T
- Efficiency = 18.4%

---

## Slotted ALOHA

### S = Superior Performance

- Vulnerable Time = T
- Efficiency = 36.8%

---

# Important Numerical Formulas

## Pure ALOHA

Throughput:


::contentReference[oaicite:4]{index=4}


Maximum Throughput:

:contentReference[oaicite:5]{index=5}

Vulnerable Time:

```text
2T
```

---

## Slotted ALOHA

Throughput:


::contentReference[oaicite:6]{index=6}


Maximum Throughput:

:contentReference[oaicite:7]{index=7}

Vulnerable Time:

```text
T
```

---

# 🎤 Viva Questions

1. What is ALOHA Protocol?
2. Who developed ALOHA?
3. What is Pure ALOHA?
4. What is Slotted ALOHA?
5. What is Vulnerable Time?
6. Why is Slotted ALOHA better?
7. State throughput formula of Pure ALOHA.
8. State throughput formula of Slotted ALOHA.
9. What is the efficiency of Pure ALOHA?
10. What is the efficiency of Slotted ALOHA?

---

# 📝 2-Mark Questions

### Q1. Define ALOHA.

ALOHA is a Random Access Protocol where stations transmit whenever data is available.

---

### Q2. What is Pure ALOHA?

Transmission can occur at any time.

---

### Q3. What is Slotted ALOHA?

Transmission occurs only at slot boundaries.

---

### Q4. Define Vulnerable Time.

The period during which a collision can occur.

---

### Q5. State the vulnerable time of Pure ALOHA.

```text
2T
```

---

# 📝 5-Mark Questions

1. Explain Pure ALOHA.
2. Explain Slotted ALOHA.
3. Discuss vulnerable time.
4. Explain throughput and efficiency.
5. Compare Pure and Slotted ALOHA.

---

# 📝 10-Mark Questions

1. Explain ALOHA Protocol in detail.
2. Explain Pure ALOHA with vulnerable time and throughput.
3. Explain Slotted ALOHA with vulnerable time and throughput.
4. Compare Pure ALOHA and Slotted ALOHA.
5. Discuss advantages and disadvantages of ALOHA protocols.

---

# ✅ Important MCQs

### 1. ALOHA belongs to:

A. Routing Protocol

B. Random Access Protocol ✅

C. Transport Protocol

D. Network Layer

---

### 2. Pure ALOHA allows transmission:

A. Only in slots

B. Anytime ✅

C. After polling

D. After reservation

---

### 3. Vulnerable Time in Pure ALOHA is:

A. T

B. 2T ✅

C. 3T

D. 4T

---

### 4. Vulnerable Time in Slotted ALOHA is:

A. T ✅

B. 2T

C. 3T

D. 4T

---

### 5. Maximum Efficiency of Pure ALOHA:

A. 18.4% ✅

B. 36.8%

C. 50%

D. 100%

---

### 6. Maximum Efficiency of Slotted ALOHA:

A. 18.4%

B. 36.8% ✅

C. 50%

D. 100%

---

### 7. Slotted ALOHA requires:

A. Routing

B. Synchronization ✅

C. Encryption

D. Multiplexing

---

# 📌 One-Page Revision Sheet

## ALOHA

- Random Access Protocol
- Developed at University of Hawaii

### Pure ALOHA

- Transmit Anytime
- Vulnerable Time = 2T
- Efficiency = 18.4%

### Slotted ALOHA

- Time Slots Used
- Vulnerable Time = T
- Efficiency = 36.8%

### Key Formulas

Pure ALOHA:


::contentReference[oaicite:8]{index=8}


Slotted ALOHA:


::contentReference[oaicite:9]{index=9}


---

# 🚀 Highest Priority MAKAUT Topics

⭐⭐⭐⭐⭐ Pure ALOHA

⭐⭐⭐⭐⭐ Slotted ALOHA

⭐⭐⭐⭐⭐ Vulnerable Time

⭐⭐⭐⭐⭐ Throughput Formula

⭐⭐⭐⭐⭐ Efficiency Calculation

⭐⭐⭐⭐⭐ Pure ALOHA vs Slotted ALOHA

⭐⭐⭐⭐ Numerical Problems

These topics are extremely important for MAKAUT semester examinations, viva examinations, internal assessments, and university theory papers.