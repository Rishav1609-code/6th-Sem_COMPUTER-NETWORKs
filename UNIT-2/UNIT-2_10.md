# Computer Networks – Unit 2
# 10. Carrier Sense Multiple Access (CSMA)

> 🎯 MAKAUT Exam Focus:
> CSMA, Carrier Sensing, 1-Persistent CSMA, Non-Persistent CSMA, P-Persistent CSMA, Comparison of Persistence Methods, and CSMA Performance are among the most frequently asked topics in semester examinations.

---

# 📖 Topic Overview

Carrier Sense Multiple Access (CSMA) is an improvement over ALOHA Protocol.

In ALOHA, stations transmit whenever they have data, leading to frequent collisions.

CSMA reduces collisions by first checking (sensing) whether the communication channel is busy or idle before transmission.

This technique significantly improves network efficiency and throughput.

---

## 🌍 Real-World Relevance

CSMA concepts are used in:

- Ethernet Networks
- Wireless LANs
- Local Area Networks
- Internet Communication
- Network Protocol Design

---

# 🎯 Learning Objectives

After studying this topic, you will be able to:

✔ Understand CSMA

✔ Explain Carrier Sensing

✔ Describe Persistence Methods

✔ Compare 1-Persistent, Non-Persistent and P-Persistent CSMA

✔ Analyze CSMA Performance

✔ Understand Collision Reduction Techniques

---

# 10.1 Introduction to CSMA

⭐⭐⭐⭐⭐ Most Important Topic

---

## Definition

Carrier Sense Multiple Access (CSMA) is a Random Access Protocol in which a station senses the channel before transmitting data.

---

## Basic Idea

Before transmission:

```text
Listen First
     ↓
If Idle → Transmit
If Busy → Wait
```

---

## Why CSMA Was Introduced?

Problem in ALOHA:

```text
Transmit Anytime
      ↓
High Collision Rate
```

Solution:

```text
Check Channel First
      ↓
Fewer Collisions
```

---

## Working Principle

### Step 1

Station has data to send.

### Step 2

Sense the channel.

### Step 3

If channel is idle:

```text
Transmit
```

### Step 4

If channel is busy:

```text
Wait
```

### Step 5

Retry later.

---

# General Flow Diagram

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
Send     Wait
```

---

## Advantages

✅ Reduced collisions

✅ Better throughput

✅ Efficient channel utilization

✅ Improved performance

---

## Disadvantages

❌ Collision still possible

❌ Propagation delay affects performance

❌ More complex than ALOHA

---

# 10.2 Carrier Sensing

⭐⭐⭐⭐ Frequently Asked

---

## Definition

Carrier Sensing is the process of checking whether the transmission medium is busy or idle before sending data.

---

## Easy Explanation

Imagine entering a classroom.

Before speaking:

```text
Check if someone is speaking.
```

If yes:

```text
Wait
```

If no:

```text
Speak
```

Similarly in CSMA:

```text
Check Channel
      ↓
Transmit Only If Free
```

---

## Types of Channel States

### Idle Channel

```text
No Transmission
```

Safe to transmit.

---

### Busy Channel

```text
Another Station Transmitting
```

Must wait.

---

## Importance of Carrier Sensing

- Reduces collisions
- Improves throughput
- Better bandwidth utilization

---

# 10.3 Persistence Methods

⭐⭐⭐⭐⭐ Very Important MAKAUT Topic

---

## Definition

Persistence Methods define how a station behaves when it senses a busy channel.

---

# Types of Persistence Methods

```text
Persistence Methods
         |
   +-----+-----+
   |     |     |
 1-P   Non-P   P-P
```

---

# 1-Persistent CSMA

⭐⭐⭐⭐⭐ Frequently Asked

---

## Definition

When the channel becomes idle, the station transmits immediately with probability 1.

---

## Working

### Step 1

Sense channel.

### Step 2

If idle:

```text
Transmit Immediately
```

### Step 3

If busy:

```text
Keep Listening
```

### Step 4

Transmit as soon as channel becomes free.

---

# Flow Diagram

```text
Sense Channel
      |
Idle?
      |
+-----+-----+
|           |
Yes         No
|           |
Send     Keep Listening
              |
         Channel Free?
              |
             Send
```

---

## Advantages

✅ Simple

✅ Low waiting time

---

## Disadvantages

❌ High collision probability

❌ Multiple stations may transmit together

---

# 1-Persistent Example

```text
A waiting

B waiting

Channel Free
     ↓

A and B transmit
     ↓

Collision
```

---

# Non-Persistent CSMA

⭐⭐⭐⭐⭐ Most Important

---

## Definition

If the channel is busy, the station waits for a random time before sensing again.

---

## Working

### Step 1

Sense channel.

### Step 2

If idle:

```text
Transmit
```

### Step 3

If busy:

```text
Wait Random Time
```

### Step 4

Sense again.

---

# Flow Diagram

```text
Sense Channel
      |
Idle?
      |
+-----+-----+
|           |
Yes         No
|           |
Send     Random Wait
              |
         Sense Again
```

---

## Advantages

✅ Fewer collisions

✅ Better efficiency

---

## Disadvantages

❌ Increased delay

❌ Longer waiting time

---

# P-Persistent CSMA

⭐⭐⭐⭐ Frequently Asked

---

## Definition

When the channel becomes idle:

- Transmit with probability p
- Wait with probability (1-p)

---

## Working

### Step 1

Sense channel.

### Step 2

If idle:

```text
Transmit with Probability p
```

or

```text
Wait with Probability (1-p)
```

### Step 3

Repeat process.

---

# Example

Let:

```text
p = 0.5
```

Then:

```text
50% chance → Transmit

50% chance → Wait
```

---

## Advantages

✅ Balanced performance

✅ Lower collision probability

✅ Better channel utilization

---

## Disadvantages

❌ Complex implementation

❌ Requires probability calculations

---

# Comparison of Persistence Methods

⭐⭐⭐⭐⭐ Important Exam Table

| Feature | 1-Persistent | Non-Persistent | P-Persistent |
|----------|-------------|---------------|-------------|
| Idle Channel | Transmit Immediately | Transmit Immediately | Transmit with Probability p |
| Busy Channel | Keep Listening | Random Wait | Wait According to p |
| Collision Probability | High | Low | Moderate |
| Delay | Low | High | Moderate |
| Throughput | Moderate | High | High |
| Complexity | Low | Low | High |

---

# Memory Trick

### Persistence Order

```text
1-P → Fastest

P-P → Balanced

Non-P → Safest
```

---

# 10.4 CSMA Performance

⭐⭐⭐⭐⭐ Most Important Theory Topic

---

## Definition

CSMA Performance measures how efficiently the protocol utilizes the channel.

---

## Factors Affecting Performance

### 1. Propagation Delay

Signal travel time affects collision probability.

---

### 2. Traffic Load

Higher load increases collisions.

---

### 3. Number of Stations

More users increase contention.

---

### 4. Persistence Method

Different methods provide different performance levels.

---

# Performance Comparison

| Protocol | Efficiency |
|-----------|-----------|
| Pure ALOHA | Low |
| Slotted ALOHA | Better |
| CSMA | High |

---

# Why CSMA Performs Better?

Because:

```text
Listen Before Transmit
```

reduces unnecessary collisions.

---

# CSMA Efficiency Trend

```text
ALOHA
   ↓
Slotted ALOHA
   ↓
CSMA
   ↓
CSMA/CD
```

Efficiency improves progressively.

---

# Advantages of CSMA

✅ Reduced collision rate

✅ Better bandwidth utilization

✅ Higher throughput

✅ More efficient than ALOHA

---

# Disadvantages of CSMA

❌ Collision still possible

❌ Performance affected by propagation delay

❌ Not perfect under heavy load

---

# 🎤 Viva Questions

1. What is CSMA?
2. Why was CSMA introduced?
3. What is carrier sensing?
4. What is an idle channel?
5. What is a busy channel?
6. Define 1-Persistent CSMA.
7. Define Non-Persistent CSMA.
8. Define P-Persistent CSMA.
9. Which persistence method has the lowest collision rate?
10. Why is CSMA better than ALOHA?

---

# 📝 2-Mark Questions

### Q1. Define CSMA.

CSMA is a protocol that senses the channel before transmitting.

---

### Q2. What is carrier sensing?

Checking whether the channel is busy or idle before transmission.

---

### Q3. What is 1-Persistent CSMA?

Transmission occurs immediately when the channel becomes idle.

---

### Q4. What is Non-Persistent CSMA?

A station waits randomly when the channel is busy.

---

### Q5. What is P-Persistent CSMA?

A station transmits with probability p when the channel is idle.

---

# 📝 5-Mark Questions

1. Explain CSMA with diagram.
2. Explain carrier sensing.
3. Describe 1-Persistent CSMA.
4. Explain Non-Persistent CSMA.
5. Compare persistence methods.

---

# 📝 10-Mark Questions

1. Explain CSMA in detail.
2. Discuss carrier sensing and its importance.
3. Explain persistence methods with diagrams.
4. Compare 1-Persistent, Non-Persistent and P-Persistent CSMA.
5. Discuss CSMA performance and advantages.

---

# ✅ Important MCQs

### 1. CSMA stands for:

A. Carrier Sense Multiple Access ✅

B. Channel Sense Multiple Access

C. Carrier Sharing Medium Access

D. Central Switching Multiple Access

---

### 2. CSMA improves upon:

A. TCP

B. ALOHA ✅

C. UDP

D. IP

---

### 3. Carrier sensing means:

A. Error Detection

B. Checking Channel Status ✅

C. Routing

D. Encryption

---

### 4. Which CSMA method waits randomly?

A. 1-Persistent

B. Non-Persistent ✅

C. P-Persistent

D. Slotted

---

### 5. P-Persistent CSMA uses:

A. Frequency

B. Probability ✅

C. CRC

D. Hamming Code

---

### 6. Collision probability is highest in:

A. Non-Persistent

B. P-Persistent

C. 1-Persistent ✅

D. Token Passing

---

### 7. CSMA is more efficient than:

A. Ethernet

B. Routing

C. Pure ALOHA ✅

D. MAC Addressing

---

# 📌 One-Page Revision Sheet

## CSMA

- Listen Before Transmit
- Reduces Collisions
- Better Than ALOHA

---

## Carrier Sensing

Check Channel:

- Idle → Send
- Busy → Wait

---

## Persistence Methods

### 1-Persistent

Transmit Immediately

### Non-Persistent

Random Wait

### P-Persistent

Probability-Based

---

## Best Comparison

| Method | Collision |
|----------|-----------|
| 1-Persistent | High |
| Non-Persistent | Low |
| P-Persistent | Moderate |

---

# 🧠 Memory Tricks

## Persistence Methods

### 1NP Rule

1 → Immediate

N → Random Wait

P → Probability

---

## Collision Order

Highest → Lowest

```text
1-Persistent
      ↓
P-Persistent
      ↓
Non-Persistent
```

---

# 🚀 Highest Priority MAKAUT Topics

⭐⭐⭐⭐⭐ CSMA Concept

⭐⭐⭐⭐⭐ Carrier Sensing

⭐⭐⭐⭐⭐ 1-Persistent CSMA

⭐⭐⭐⭐⭐ Non-Persistent CSMA

⭐⭐⭐⭐⭐ P-Persistent CSMA

⭐⭐⭐⭐⭐ Comparison of Persistence Methods

⭐⭐⭐⭐ CSMA Performance

These topics are highly important for MAKAUT semester examinations, viva examinations, internal assessments, and university theory papers.