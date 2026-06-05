# Computer Networks – Unit 1 Notes

# 8. Bandwidth Utilization Techniques (MAKAUT Exam-Oriented Notes)

---

# 📖 Topic Overview

In a communication network, bandwidth is a valuable resource. To maximize the efficient use of available bandwidth, various techniques are used to allow multiple users or signals to share the same communication channel.

These techniques are known as **Bandwidth Utilization Techniques**.

The three major multiplexing techniques are:

✅ Frequency Division Multiplexing (FDM)

✅ Time Division Multiplexing (TDM)

✅ Wavelength Division Multiplexing (WDM)

These topics are among the most frequently asked questions in MAKAUT Computer Networks examinations.

---

# 🎯 Learning Objectives

After studying this chapter, you will be able to:

✔ Define Bandwidth, Throughput, and Data Rate.

✔ Explain Multiplexing and its components.

✔ Understand FDM, TDM, and WDM.

✔ Compare different multiplexing techniques.

✔ Solve MAKAUT theory and MCQ questions confidently.

---

# 8.1 Introduction to Bandwidth

---

# What is Bandwidth?

---

## Definition

Bandwidth is the maximum amount of data that can be transmitted through a communication channel in a given time.

---

## Simple Explanation

Bandwidth represents the capacity of a communication link.

Think of it as the width of a highway.

* Wider highway → More vehicles
* Higher bandwidth → More data

---

## Unit

Bandwidth is measured in:

* Hertz (Hz) (Analog Signals)
* Bits per second (bps) (Digital Communication)

---

## Example

```text
10 Mbps Internet Connection
```

Means up to 10 million bits can be transmitted per second.

---

# Real-Life Analogy

```text
Narrow Road  → Less Traffic
Wide Road    → More Traffic
```

Similarly,

```text
Low Bandwidth  → Less Data
High Bandwidth → More Data
```

---

# Throughput

---

## Definition

Throughput is the actual amount of data successfully transmitted through a network per unit time.

---

## Important Point

Bandwidth = Maximum Capacity

Throughput = Actual Performance

---

## Example

Suppose:

```text
Bandwidth = 100 Mbps
Actual Data Transfer = 80 Mbps
```

Then:

```text
Throughput = 80 Mbps
```

---

## Why Throughput is Lower?

Because of:

* Network Congestion
* Errors
* Delays
* Packet Loss

---

# Bandwidth vs Throughput

| Feature      | Bandwidth        | Throughput           |
| ------------ | ---------------- | -------------------- |
| Meaning      | Maximum Capacity | Actual Data Transfer |
| Value        | Theoretical      | Practical            |
| Unit         | bps              | bps                  |
| Always Same? | No               | Usually Lower        |

---

# Data Rate

---

## Definition

Data Rate is the number of bits transmitted per second.

---

## Formula

\text{Data Rate} = \frac{\text{Number of Bits}}{\text{Time}}

---

## Unit

* bps
* Kbps
* Mbps
* Gbps

---

## Example

If 1,000,000 bits are transmitted in 1 second:

```text
Data Rate = 1 Mbps
```

---

# Memory Trick

### BTD

B → Bandwidth (Capacity)

T → Throughput (Actual Transfer)

D → Data Rate (Speed)

---

# 8.2 Multiplexing

---

# Concept of Multiplexing

---

## Definition

Multiplexing is a technique that combines multiple signals and transmits them through a single communication channel.

---

## Why Multiplexing?

Without Multiplexing:

```text
User A → Separate Channel
User B → Separate Channel
User C → Separate Channel
```

Expensive and inefficient.

---

With Multiplexing:

```text
User A
User B
User C
   │
 Multiplexer
   │
Single Channel
```

Efficient bandwidth utilization.

---

# Components of Multiplexing

---

## Multiplexer (MUX)

---

### Definition

A Multiplexer combines multiple input signals into a single output signal.

---

### Function

```text
Many Inputs
      ↓
     MUX
      ↓
 Single Output
```

---

## Demultiplexer (DEMUX)

---

### Definition

A Demultiplexer separates received signals back into original signals.

---

### Function

```text
Single Input
      ↓
    DEMUX
      ↓
Multiple Outputs
```

---

# Overall Multiplexing Process

```text
Signal A
Signal B
Signal C
     │
    MUX
     │
Communication Channel
     │
   DEMUX
     │
A   B   C
```

---

# Advantages of Multiplexing

✅ Efficient Bandwidth Usage

✅ Reduced Cost

✅ Supports Multiple Users

✅ Better Resource Utilization

---

# 8.3 Frequency Division Multiplexing (FDM)

---

# Definition

FDM divides the total bandwidth into multiple frequency bands.

Each signal is assigned a unique frequency range.

---

# Working Principle

```text
Total Bandwidth
────────────────────

Ch1  Ch2  Ch3  Ch4

Each uses different frequency
```

---

## Concept

Multiple signals are transmitted simultaneously but at different frequencies.

---

# Frequency Bands

Each user receives a separate frequency band.

Example:

| Channel | Frequency   |
| ------- | ----------- |
| Ch1     | 100–120 kHz |
| Ch2     | 130–150 kHz |
| Ch3     | 160–180 kHz |

---

# Guard Bands

---

## Definition

Unused frequency spaces between channels.

---

## Purpose

Prevent overlap and interference.

---

## Diagram

```text
Ch1 | Guard | Ch2 | Guard | Ch3
```

---

# Applications of FDM

✅ Radio Broadcasting

✅ Television Broadcasting

✅ Cable TV

✅ Satellite Communication

---

# Advantages of FDM

✅ Simultaneous Transmission

✅ No Time Delay

✅ Continuous Communication

---

# Disadvantages of FDM

❌ Requires Guard Bands

❌ Bandwidth Wastage

❌ Crosstalk Possibility

❌ Expensive Hardware

---

# 8.4 Time Division Multiplexing (TDM)

---

# Definition

TDM divides a communication channel into different time slots.

Each user transmits data during an assigned time slot.

---

# Working Principle

```text
Time
──────────────────────

A B C D A B C D
```

Each user gets a turn.

---

# Time Slots

---

## Definition

Small intervals of time allocated to users.

---

## Example

```text
Slot 1 → User A
Slot 2 → User B
Slot 3 → User C
```

---

# Types of TDM

---

# 1. Synchronous TDM

---

## Definition

Each device gets a fixed time slot whether data exists or not.

---

## Example

```text
A B C D
A B C D
A B C D
```

Even if C has no data.

---

## Advantages

✅ Simple

✅ Predictable

---

## Disadvantages

❌ Bandwidth Waste

---

# 2. Statistical TDM

---

## Definition

Time slots are assigned only to devices that have data.

---

## Example

```text
A B D A B D
```

C is skipped because it has no data.

---

## Advantages

✅ Better Efficiency

✅ Less Bandwidth Waste

---

## Disadvantages

❌ More Complex

---

# Applications of TDM

✅ Telephone Networks

✅ Digital Communication

✅ Cellular Networks

---

# Advantages of TDM

✅ Efficient Channel Sharing

✅ No Guard Bands

✅ Better Digital Communication

---

# Disadvantages of TDM

❌ Synchronization Required

❌ Delay Possible

---

# Synchronous vs Statistical TDM

| Feature         | Synchronous | Statistical |
| --------------- | ----------- | ----------- |
| Slot Allocation | Fixed       | Dynamic     |
| Efficiency      | Lower       | Higher      |
| Complexity      | Low         | High        |
| Bandwidth Waste | More        | Less        |

---

# 8.5 Wavelength Division Multiplexing (WDM)

---

# Definition

WDM is a multiplexing technique used in optical fiber communication.

Multiple optical signals are transmitted simultaneously using different wavelengths of light.

---

# Working Principle

```text
λ1
λ2
λ3
λ4
  │
 WDM
  │
Optical Fiber
```

---

## Concept

Different wavelengths carry different data streams through the same fiber.

---

# Types of WDM

---

# 1. CWDM (Coarse WDM)

---

## Definition

Uses wider spacing between wavelengths.

---

## Characteristics

* Lower Cost
* Fewer Channels
* Shorter Distance

---

# 2. DWDM (Dense WDM)

---

## Definition

Uses closely spaced wavelengths.

---

## Characteristics

* Higher Capacity
* More Channels
* Long-Distance Communication

---

# CWDM vs DWDM

| Feature         | CWDM    | DWDM   |
| --------------- | ------- | ------ |
| Channel Density | Low     | High   |
| Cost            | Lower   | Higher |
| Capacity        | Lower   | Higher |
| Distance        | Shorter | Longer |

---

# Applications of WDM

✅ Optical Fiber Networks

✅ Internet Backbone

✅ Data Centers

✅ Telecommunication Systems

✅ Long-Distance Communication

---

# Advantages of WDM

✅ Extremely High Capacity

✅ Efficient Fiber Utilization

✅ Long-Distance Transmission

✅ High Bandwidth

---

# Disadvantages of WDM

❌ Expensive

❌ Complex Technology

❌ Difficult Maintenance

---

# FDM vs TDM vs WDM

| Feature                   | FDM         | TDM              | WDM           |
| ------------------------- | ----------- | ---------------- | ------------- |
| Division Basis            | Frequency   | Time             | Wavelength    |
| Medium                    | Radio/Cable | Digital Networks | Optical Fiber |
| Simultaneous Transmission | Yes         | No               | Yes           |
| Guard Bands Needed        | Yes         | No               | No            |
| Cost                      | Medium      | Low              | High          |

---

# Frequently Asked 2 Marks Questions

### Q1. What is bandwidth?

Maximum capacity of a communication channel.

---

### Q2. What is throughput?

Actual data transmitted successfully.

---

### Q3. What is multiplexing?

Combining multiple signals into one communication channel.

---

### Q4. What is a guard band?

Unused frequency range between channels.

---

### Q5. What is WDM?

Multiplexing using different light wavelengths.

---

# Frequently Asked 5 Marks Questions

### Q1. Explain multiplexing.

### Q2. Explain FDM with advantages and disadvantages.

### Q3. Explain TDM and its types.

### Q4. Differentiate synchronous and statistical TDM.

### Q5. Explain WDM and its applications.

---

# Frequently Asked 10 Marks Questions

### Q1. Explain bandwidth utilization techniques.

### Q2. Explain FDM, TDM, and WDM.

### Q3. Compare FDM, TDM, and WDM.

### Q4. Explain multiplexing with block diagram.

### Q5. Discuss WDM, CWDM, and DWDM.

---

# Important Viva Questions

### What is bandwidth?

Channel capacity.

### What is throughput?

Actual transmitted data.

### What is a MUX?

Combines signals.

### What is a DEMUX?

Separates signals.

### Which multiplexing uses frequency?

FDM.

### Which multiplexing uses time slots?

TDM.

### Which multiplexing uses optical wavelengths?

WDM.

### What is the purpose of guard bands?

Prevent interference.

---

# Important MCQs

### 1. Bandwidth represents:

A. Actual Speed

B. Maximum Capacity

C. Delay

D. Error Rate

✅ Answer: B

---

### 2. Throughput is:

A. Maximum Capacity

B. Actual Transfer Rate

C. Frequency

D. Time Slot

✅ Answer: B

---

### 3. Multiplexing combines:

A. One Signal

B. Multiple Signals

C. Packets

D. Frames

✅ Answer: B

---

### 4. Guard Bands are used in:

A. TDM

B. WDM

C. FDM

D. VLAN

✅ Answer: C

---

### 5. Time slots are used in:

A. FDM

B. TDM

C. WDM

D. Ethernet

✅ Answer: B

---

### 6. WDM is mainly used in:

A. Copper Cable

B. Radio Communication

C. Optical Fiber

D. Bluetooth

✅ Answer: C

---

### 7. DWDM provides:

A. Lower Capacity

B. Higher Capacity

C. Lower Bandwidth

D. Lower Speed

✅ Answer: B

---

# 🚀 One-Page Revision Sheet

### BTD

Bandwidth → Capacity

Throughput → Actual Transfer

Data Rate → Transmission Speed

---

### Multiplexing Components

MUX → Combine Signals

DEMUX → Separate Signals

---

### Multiplexing Types

FDM → Frequency Division

TDM → Time Division

WDM → Wavelength Division

---

### TDM Types

Synchronous TDM

Statistical TDM

---

### WDM Types

CWDM

DWDM

---

### Most Important Comparisons

✅ Bandwidth vs Throughput

✅ FDM vs TDM vs WDM

✅ Synchronous vs Statistical TDM

✅ CWDM vs DWDM

---

# ⭐ Most Important MAKAUT Questions

1. Define bandwidth, throughput, and data rate.
2. Explain multiplexing with MUX and DEMUX.
3. Explain FDM with guard bands.
4. Explain TDM and its types.
5. Differentiate synchronous and statistical TDM.
6. Explain WDM and its working principle.
7. Differentiate CWDM and DWDM.
8. Compare FDM, TDM, and WDM.
9. Explain applications of multiplexing.
10. Discuss advantages and disadvantages of FDM, TDM, and WDM.

---

# 📝 Last-Minute Revision

### Remember

**FDM → Frequency**

**TDM → Time Slots**

**WDM → Wavelengths**

**MUX → Combines**

**DEMUX → Separates**

**Bandwidth → Maximum Capacity**

**Throughput → Actual Performance**

### High-Probability MAKAUT Questions

✅ Multiplexing Concept

✅ FDM with Guard Bands

✅ TDM Types

✅ WDM Working Principle

✅ FDM vs TDM vs WDM

✅ CWDM vs DWDM

These are among the most frequently repeated and exam-important topics from Unit-1 of Computer Networks in MAKAUT examinations.
