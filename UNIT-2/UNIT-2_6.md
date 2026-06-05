# Computer Networks – Unit 2
# 6. Piggybacking

> 🎯 MAKAUT Exam Focus:
> Piggybacking concept, ACK Piggybacking, Working Mechanism, Advantages, Limitations, and Comparison with Separate ACK are frequently asked in semester examinations.

---

# 📖 Topic Overview

Piggybacking is a technique used in Data Link Layer protocols to improve communication efficiency.

Instead of sending a separate Acknowledgement (ACK) frame, the receiver attaches the ACK to an outgoing data frame.

This reduces network overhead and improves bandwidth utilization.

---

## 🌍 Real-World Relevance

Piggybacking is used in:

- TCP Communication
- Full-Duplex Networks
- Sliding Window Protocols
- Wireless Communication
- Internet Data Transfer
- Computer Networks

---

# 🎯 Learning Objectives

After studying this topic, you will be able to:

✔ Define Piggybacking

✔ Explain ACK Piggybacking

✔ Understand the Working Mechanism

✔ Explain Advantages and Limitations

✔ Compare Piggybacked ACK and Separate ACK

---

# 6.1 Introduction to Piggybacking

## Definition

Piggybacking is a technique in which an acknowledgement (ACK) is attached to an outgoing data frame rather than being sent as a separate frame.

---

## Easy Explanation

Suppose two computers are communicating.

Normally:

```text
Computer A → Data → Computer B

Computer B → ACK → Computer A
```

Two separate transmissions occur.

With Piggybacking:

```text
Computer A → Data → Computer B

Computer B → Data + ACK → Computer A
```

Only one transmission is needed.

---

## Why Piggybacking is Needed?

Without Piggybacking:

- More ACK frames
- More bandwidth usage
- More overhead

With Piggybacking:

- Fewer frames
- Better bandwidth utilization
- Improved efficiency

---

## Real-Life Example

Imagine two friends talking on the phone.

Friend A asks:

"Did you receive my notes?"

Friend B replies:

"Yes, I received them, and here are your assignments."

The acknowledgement and new information are sent together.

This is similar to Piggybacking.

---

# 6.2 Working Mechanism

## Step-by-Step Process

### Step 1

Sender A sends a data frame.

```text
A → Frame 1 → B
```

---

### Step 2

Receiver B receives the frame successfully.

Now B must send ACK.

---

### Step 3

Instead of sending ACK immediately,

B checks whether it has data to send.

---

### Step 4

If data is available:

```text
B → Data + ACK → A
```

ACK is attached to outgoing data.

---

### Step 5

Sender A receives:

- ACK
- Data

in a single frame.

---

# Flow Diagram

```text
Sender A
    |
    | Data Frame
    V
Receiver B
    |
    | Has Data?
    |
    +---- Yes ----> Send Data + ACK
    |
    +---- No -----> Send Separate ACK
```

---

## Important Exam Point ⭐

Piggybacking works best in:

- Full-Duplex Communication
- Bidirectional Communication

---

# 6.3 ACK Piggybacking

## Definition

ACK Piggybacking means attaching acknowledgement information to an outgoing data frame.

---

## Frame Format

```text
+--------------------------------+
| Header | ACK | Data | Trailer |
+--------------------------------+
```

ACK field is inserted into the frame.

---

## Example

Suppose:

```text
A sends Frame 5
```

Receiver B receives it correctly.

B also has data to send.

Instead of:

```text
ACK5

Data Frame
```

B sends:

```text
Data Frame + ACK5
```

---

## Benefits

- Fewer frames transmitted
- Reduced overhead
- Improved efficiency
- Better bandwidth utilization

---

# 6.4 Advantages

## 1. Reduces Overhead

Separate ACK frames are eliminated.

---

## 2. Saves Bandwidth

Less control traffic is generated.

---

## 3. Improves Throughput

More useful data is transmitted.

---

## 4. Better Channel Utilization

Communication channel remains productive.

---

## 5. Efficient Full-Duplex Communication

Ideal when both sender and receiver exchange data.

---

## Example

Without Piggybacking:

```text
100 Data Frames
100 ACK Frames

Total = 200 Frames
```

With Piggybacking:

```text
100 Combined Frames

Total ≈ 100 Frames
```

Bandwidth usage is significantly reduced.

---

# 6.5 Limitations

## 1. ACK Delay

Receiver may wait before sending ACK.

---

## 2. Requires Bidirectional Traffic

Works best when both sides have data.

---

## 3. Increased Complexity

Protocol implementation becomes more complex.

---

## 4. Timeout Risk

Delayed ACK may trigger unnecessary retransmissions.

---

## 5. Not Suitable for One-Way Communication

If only one side sends data, piggybacking provides little benefit.

---

# Comparison: Separate ACK vs Piggybacked ACK

| Feature | Separate ACK | Piggybacked ACK |
|----------|-------------|----------------|
| ACK Transmission | Separate Frame | Attached with Data |
| Overhead | High | Low |
| Bandwidth Usage | More | Less |
| Efficiency | Lower | Higher |
| Complexity | Simple | More Complex |
| ACK Delay | Minimal | Possible |

---

# Key Features of Piggybacking

- Combines ACK and Data
- Reduces Network Traffic
- Saves Bandwidth
- Improves Throughput
- Used in Full-Duplex Networks

---

# 🎤 Viva Questions

### Q1. What is Piggybacking?

Piggybacking is the process of attaching ACK information to an outgoing data frame.

---

### Q2. Why is Piggybacking used?

To reduce overhead and improve bandwidth utilization.

---

### Q3. What is ACK Piggybacking?

Combining acknowledgement and data into a single frame.

---

### Q4. What is the main advantage of Piggybacking?

Reduced transmission overhead.

---

### Q5. What is the main limitation of Piggybacking?

ACK delay.

---

### Q6. Is Piggybacking useful in one-way communication?

No. It is mainly useful in bidirectional communication.

---

# 📝 2-Mark Questions

### Q1. Define Piggybacking.

Piggybacking is a technique in which ACK is attached to an outgoing data frame.

---

### Q2. What is ACK Piggybacking?

Combining acknowledgement information with data transmission.

---

### Q3. State one advantage of Piggybacking.

It reduces protocol overhead.

---

### Q4. State one limitation of Piggybacking.

ACK delay.

---

### Q5. Why does Piggybacking save bandwidth?

Because separate ACK frames are reduced.

---

# 📝 5-Mark Questions

1. Explain Piggybacking with diagram.
2. Describe the working mechanism of Piggybacking.
3. Explain ACK Piggybacking.
4. Discuss advantages of Piggybacking.
5. Discuss limitations of Piggybacking.

---

# 📝 10-Mark Questions

1. Explain Piggybacking in detail with diagrams.
2. Describe the working mechanism of Piggybacking.
3. Explain ACK Piggybacking with example.
4. Compare Separate ACK and Piggybacked ACK.
5. Discuss advantages and limitations of Piggybacking.

---

# ✅ Important MCQs

### 1. Piggybacking combines:

A. Routing and Switching

B. Data and ACK ✅

C. CRC and Checksum

D. Error and Flow Control

---

### 2. Piggybacking is mainly used to:

A. Encrypt Data

B. Reduce Overhead ✅

C. Detect Errors

D. Route Packets

---

### 3. Piggybacking works best in:

A. Full-Duplex Communication ✅

B. Broadcast Networks

C. Half-Duplex Communication

D. Satellite Networks

---

### 4. Main limitation of Piggybacking:

A. High Throughput

B. ACK Delay ✅

C. Better Utilization

D. Low Overhead

---

### 5. Piggybacking reduces:

A. Window Size

B. Sequence Numbers

C. Number of Frames Transmitted ✅

D. Error Detection

---

# 📌 One-Page Revision Sheet

## Piggybacking

ACK is attached to outgoing data frame.

---

## Working

```text
Receive Frame
      |
      V
Has Data to Send?
      |
  +---+---+
  |       |
 Yes      No
  |       |
Data+ACK  ACK
```

---

## Advantages

- Less Overhead
- Better Bandwidth Utilization
- Higher Throughput
- Efficient Communication

---

## Limitations

- ACK Delay
- Complex Implementation
- Requires Bidirectional Communication
- Timeout Possibility

---

# 🎯 Top 20 Expected MAKAUT Questions

1. Define Piggybacking.
2. Explain ACK Piggybacking.
3. Why is Piggybacking used?
4. Explain Piggybacking with diagram.
5. Describe the working mechanism.
6. State advantages of Piggybacking.
7. State limitations of Piggybacking.
8. Compare Separate ACK and Piggybacking.
9. How does Piggybacking save bandwidth?
10. What is ACK delay?
11. Explain protocol overhead reduction.
12. Why is Piggybacking efficient?
13. Explain bandwidth utilization.
14. Applications of Piggybacking.
15. Explain full-duplex communication in Piggybacking.
16. What happens if ACK is delayed?
17. Explain Piggybacking with example.
18. Why is Piggybacking not suitable for one-way communication?
19. Explain ACK attachment mechanism.
20. Discuss practical uses of Piggybacking.

---

# 🧠 Memory Tricks

## Piggybacking

**PIG**

- P = Put
- I = In
- G = Going Frame

Meaning:

ACK is put inside the outgoing frame.

---

## Advantages

### BHOT

- B = Bandwidth Saving
- H = Higher Throughput
- O = Overhead Reduction
- T = Traffic Reduction

---

## Limitations

### DBC

- D = Delay in ACK
- B = Bidirectional Traffic Required
- C = Complexity

---

# 🚀 1-Day Before Exam Revision Strategy

Revise in this order:

1. Definition of Piggybacking
2. Working Mechanism
3. ACK Piggybacking
4. Advantages
5. Limitations
6. Comparison Table

Most Important Topics:

⭐⭐⭐⭐⭐ Piggybacking Concept

⭐⭐⭐⭐⭐ ACK Piggybacking

⭐⭐⭐⭐ Working Mechanism

⭐⭐⭐⭐ Advantages

⭐⭐⭐⭐ Limitations

⭐⭐⭐ Comparison with Separate ACK