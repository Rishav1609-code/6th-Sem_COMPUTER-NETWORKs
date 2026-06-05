# Computer Networks – Unit 1 Notes

# 9. Spread Spectrum (MAKAUT Exam-Oriented Notes)

---

# 📖 Topic Overview

In normal communication systems, data is transmitted using a narrow frequency band. This makes communication vulnerable to:

❌ Noise

❌ Interference

❌ Eavesdropping

❌ Jamming Attacks

To overcome these problems, **Spread Spectrum Technology** was developed.

Spread Spectrum spreads the signal over a much wider bandwidth than actually required, making communication more secure, reliable, and resistant to interference.

It is widely used in:

✅ Bluetooth

✅ GPS

✅ Wi-Fi

✅ Military Communication

---

# 🎯 Learning Objectives

After studying this chapter, you will be able to:

✔ Define Spread Spectrum.

✔ Explain its characteristics and advantages.

✔ Understand FHSS and DSSS.

✔ Differentiate Fast and Slow Frequency Hopping.

✔ Explain Hybrid Spread Spectrum.

✔ Understand practical applications.

✔ Solve MAKAUT theory and MCQ questions confidently.

---

# 9.1 Introduction to Spread Spectrum

---

# Definition

Spread Spectrum is a communication technique in which the transmitted signal is spread over a bandwidth much larger than the minimum bandwidth required.

---

## Simple Explanation

Instead of transmitting data on one fixed frequency, the signal is distributed over many frequencies.

---

## Basic Concept

Normal Communication:

```text
Signal
  │
Single Frequency
```

Spread Spectrum:

```text
Signal
  │
Many Frequencies
```

---

## Why Spread Spectrum?

To improve:

* Security
* Reliability
* Noise Resistance
* Anti-Jamming Capability

---

## Real-Life Analogy

Imagine hiding a message.

### Normal Method

Place the entire message in one box.

Easy to find.

### Spread Spectrum Method

Split the message into many boxes and place them in different locations.

Much harder to intercept.

---

# Working Principle

---

## Sender Side

```text
Data
  │
Spreading Code
  │
Spread Signal
```

---

## Receiver Side

```text
Spread Signal
     │
Despreading Code
     │
Original Data
```

---

## Important Point

Only devices knowing the spreading code can recover the original message.

---

# 9.2 Characteristics of Spread Spectrum

---

# 1. Wide Bandwidth Usage

Uses much larger bandwidth than required.

---

# 2. Low Power Density

Signal power is spread across many frequencies.

---

# 3. Noise Resistance

Less affected by interference.

---

# 4. Security

Difficult for unauthorized users to detect.

---

# 5. Anti-Jamming Capability

Communication continues even under jamming attempts.

---

# 6. Multiple User Support

Many users can share the same channel.

---

# Summary Table

| Characteristic    | Benefit                |
| ----------------- | ---------------------- |
| Wide Bandwidth    | Better Reliability     |
| Low Power Density | Harder Detection       |
| Noise Resistance  | Better Signal Quality  |
| Security          | Privacy                |
| Anti-Jamming      | Reliable Communication |
| Multiple Access   | Supports Many Users    |

---

# 9.3 Advantages of Spread Spectrum

---

# Advantages

---

## 1. High Security

Unauthorized users cannot easily intercept data.

---

## 2. Resistance to Interference

Works even in noisy environments.

---

## 3. Anti-Jamming

Protects communication from deliberate attacks.

---

## 4. Better Reliability

Communication remains stable.

---

## 5. Reduced Signal Detection

Signal appears like background noise.

---

## 6. Supports Multiple Users

Many devices can communicate simultaneously.

---

# Disadvantages

---

❌ Larger Bandwidth Requirement

❌ Complex Hardware

❌ Higher Cost

❌ Synchronization Required

---

# 9.4 Types of Spread Spectrum

---

# Classification

```text
Spread Spectrum
      │
 ┌────┼───────────┐
 │                │
FHSS             DSSS
 │
Hybrid Spread Spectrum
```

---

# 1. Frequency Hopping Spread Spectrum (FHSS)

---

# Definition

FHSS changes the carrier frequency periodically according to a predefined hopping sequence.

---

## Concept

Instead of staying on one frequency:

```text
100 MHz
```

The signal hops:

```text
100 MHz
 ↓
120 MHz
 ↓
140 MHz
 ↓
110 MHz
```

---

## Working Principle

```text
Data
 │
Frequency Hopper
 │
Multiple Frequencies
 │
Receiver follows same sequence
```

---

## Benefits

* Difficult to intercept
* Resistant to interference
* Resistant to jamming

---

# Frequency Hopping Example

```text
Time 1 → 100 MHz

Time 2 → 120 MHz

Time 3 → 140 MHz

Time 4 → 110 MHz
```

---

# Types of FHSS

---

# A. Fast Frequency Hopping

---

## Definition

Frequency changes multiple times during transmission of one data bit.

---

## Example

```text
1 Bit
 │
100 MHz
120 MHz
140 MHz
160 MHz
```

Multiple hops per bit.

---

## Characteristics

✅ Higher Security

✅ Better Anti-Jamming

❌ More Complex

---

# B. Slow Frequency Hopping

---

## Definition

Frequency changes after transmitting multiple bits.

---

## Example

```text
100 MHz
│
Several Bits

Then

120 MHz
│
Several Bits
```

---

## Characteristics

✅ Simpler

✅ Lower Cost

❌ Less Secure

---

# Fast FHSS vs Slow FHSS

| Feature      | Fast FHSS | Slow FHSS |
| ------------ | --------- | --------- |
| Hopping Rate | High      | Low       |
| Security     | Higher    | Lower     |
| Complexity   | Higher    | Lower     |
| Anti-Jamming | Better    | Moderate  |

---

# 2. Direct Sequence Spread Spectrum (DSSS)

---

# Definition

DSSS spreads data using a high-speed spreading code called a chip sequence.

---

## Working Principle

Each data bit is replaced by multiple chips.

---

## Example

Original Data:

```text
1
```

Spreading Code:

```text
10110101
```

Transmitted Signal:

```text
10110101
```

---

# Benefits

✅ High Noise Immunity

✅ Better Security

✅ Strong Signal Recovery

---

# Characteristics

* Uses Chip Sequences
* Wider Bandwidth
* Better Performance in Noisy Environments

---

# DSSS Block Diagram

```text
Data
 │
PN Code
 │
Spread Signal
 │
Transmission
```

---

# FHSS vs DSSS

| Feature          | FHSS              | DSSS           |
| ---------------- | ----------------- | -------------- |
| Technique        | Frequency Changes | Code Spreading |
| Security         | High              | Very High      |
| Complexity       | Lower             | Higher         |
| Noise Resistance | Good              | Excellent      |
| Bandwidth Usage  | Moderate          | Higher         |

---

# 3. Hybrid Spread Spectrum

---

# Definition

Hybrid Spread Spectrum combines FHSS and DSSS techniques.

---

## Purpose

To obtain benefits of both methods.

---

## Working

```text
FHSS
 +
DSSS
 =
Hybrid System
```

---

## Advantages

✅ Maximum Security

✅ Better Reliability

✅ Excellent Anti-Jamming

---

## Disadvantages

❌ Very Complex

❌ Expensive

---

# 9.5 Applications of Spread Spectrum

---

# 1. Bluetooth

---

## Usage

Bluetooth uses FHSS.

---

## Reason

Frequency hopping reduces interference from nearby devices.

---

## Benefits

✅ Reliable Device Communication

✅ Less Interference

---

# 2. GPS (Global Positioning System)

---

## Entity

Global Positioning System

---

## Usage

GPS primarily uses DSSS.

---

## Benefits

✅ Accurate Positioning

✅ Noise Resistance

---

# 3. Military Communication

---

## Usage

Military systems heavily use Spread Spectrum.

---

## Reasons

* Anti-Jamming
* Secure Communication
* Resistance to Interception

---

## Benefits

✅ High Security

✅ Reliable Communication

---

# 4. Wi-Fi

---

## Usage

Early Wi-Fi standards used DSSS.

Modern Wi-Fi technologies use advanced spread spectrum-related techniques.

---

## Benefits

✅ Reliable Wireless Networking

✅ Better Signal Quality

---

# Application Summary

| Application            | Technique Used          |
| ---------------------- | ----------------------- |
| Bluetooth              | FHSS                    |
| GPS                    | DSSS                    |
| Military Communication | FHSS + DSSS             |
| Wi-Fi                  | DSSS-Based Technologies |

---

# Frequently Asked 2 Marks Questions

### Q1. What is Spread Spectrum?

A technique that spreads a signal over a wider bandwidth than required.

---

### Q2. What is FHSS?

A technique in which transmission frequency changes continuously according to a hopping sequence.

---

### Q3. What is DSSS?

A technique that spreads data using chip sequences.

---

### Q4. What is a spreading code?

A special code used to spread and recover signals.

---

### Q5. Which spread spectrum technique is used in Bluetooth?

FHSS.

---

# Frequently Asked 5 Marks Questions

### Q1. Explain Spread Spectrum.

### Q2. Explain FHSS with working principle.

### Q3. Explain DSSS with example.

### Q4. Differentiate FHSS and DSSS.

### Q5. Explain applications of Spread Spectrum.

---

# Frequently Asked 10 Marks Questions

### Q1. Explain Spread Spectrum and its characteristics.

### Q2. Discuss FHSS and DSSS in detail.

### Q3. Compare FHSS, DSSS, and Hybrid Spread Spectrum.

### Q4. Explain the advantages and applications of Spread Spectrum.

### Q5. Explain Fast and Slow Frequency Hopping.

---

# Important Viva Questions

### What is Spread Spectrum?

Signal spreading over a wider bandwidth.

### Why is Spread Spectrum used?

To improve security and reliability.

### What does FHSS stand for?

Frequency Hopping Spread Spectrum.

### What does DSSS stand for?

Direct Sequence Spread Spectrum.

### Which technique uses chip sequences?

DSSS.

### Which technique is used in Bluetooth?

FHSS.

### Which technique is used in GPS?

DSSS.

### Which technique provides maximum security?

Hybrid Spread Spectrum.

---

# Important MCQs

### 1. Spread Spectrum uses:

A. Narrow Bandwidth

B. Wider Bandwidth

C. No Bandwidth

D. Fixed Frequency

✅ Answer: B

---

### 2. FHSS stands for:

A. Fast Hopping Signal System

B. Frequency Hopping Spread Spectrum

C. Frequency Handling Signal System

D. Frequency Hybrid Spread Spectrum

✅ Answer: B

---

### 3. DSSS uses:

A. Time Slots

B. Frequency Bands

C. Chip Sequences

D. VLAN Tags

✅ Answer: C

---

### 4. Bluetooth primarily uses:

A. DSSS

B. FHSS

C. TDM

D. FDM

✅ Answer: B

---

### 5. GPS primarily uses:

A. FHSS

B. TDM

C. DSSS

D. FDM

✅ Answer: C

---

### 6. Which offers the highest security?

A. FDM

B. FHSS

C. DSSS

D. Hybrid Spread Spectrum

✅ Answer: D

---

### 7. Fast FHSS changes frequency:

A. Once per frame

B. Multiple times per bit

C. Once per packet

D. Never

✅ Answer: B

---

# 🚀 One-Page Revision Sheet

### Spread Spectrum

Signal spread over wider bandwidth.

---

### Characteristics

* Security
* Noise Resistance
* Anti-Jamming
* Reliability

---

### Types

FHSS

DSSS

Hybrid Spread Spectrum

---

### FHSS Types

Fast FHSS

Slow FHSS

---

### Applications

Bluetooth → FHSS

GPS → DSSS

Military → FHSS + DSSS

Wi-Fi → DSSS-Based

---

### Most Important Comparisons

✅ FHSS vs DSSS

✅ Fast FHSS vs Slow FHSS

✅ Advantages of Spread Spectrum

---

# ⭐ Most Important MAKAUT Questions

1. Define Spread Spectrum and explain its characteristics.
2. Explain FHSS with working principle.
3. Differentiate Fast FHSS and Slow FHSS.
4. Explain DSSS with suitable example.
5. Compare FHSS and DSSS.
6. Explain Hybrid Spread Spectrum.
7. Discuss advantages of Spread Spectrum.
8. Explain applications of Spread Spectrum.
9. Why is Spread Spectrum resistant to jamming?
10. Write short notes on Bluetooth and GPS in relation to Spread Spectrum.

---

# 📝 Last-Minute Revision

### Remember

**FHSS → Frequency Changes**

**DSSS → Chip Sequences**

**Hybrid → FHSS + DSSS**

### Applications

Bluetooth → FHSS

GPS → DSSS

Military → Hybrid

Wi-Fi → DSSS-Based

### High-Probability MAKAUT Questions

✅ Spread Spectrum Characteristics

✅ Advantages of Spread Spectrum

✅ FHSS Working Principle

✅ Fast vs Slow FHSS

✅ DSSS Working Principle

✅ FHSS vs DSSS

✅ Applications of Spread Spectrum

These are among the most frequently repeated and examination-important topics from Unit-1 of Computer Networks under the MAKAUT syllabus.
