# Computer Networks (Unit 2) – MAKAUT 10 Marks Exam Answers

> These are structured in the style generally expected in MAKAUT semester examinations: **Definition → Explanation → Working → Diagram → Advantages/Disadvantages → Conclusion**.

---

# 1. Functions of Data Link Layer (10 Marks)

## Definition

The Data Link Layer (DLL) is the second layer of the OSI model responsible for reliable node-to-node delivery of data.

## Functions

### 1. Framing

Divides the bit stream received from the Network Layer into frames.

### 2. Physical Addressing

Adds source and destination MAC addresses.

### 3. Error Control

Detects and corrects transmission errors.

### 4. Flow Control

Controls data transmission rate between sender and receiver.

### 5. Access Control

Determines which device can use the shared medium.

### 6. Reliable Delivery

Ensures correct and ordered frame delivery.

## Diagram

```text
Network Layer
      ↓
Data Link Layer
 ├─ Framing
 ├─ Addressing
 ├─ Error Control
 ├─ Flow Control
 └─ Access Control
      ↓
Physical Layer
```

## Conclusion

DLL provides reliable communication between adjacent nodes through framing, addressing, error control, and flow control.

---

# 2. Framing Techniques (10 Marks)

## Definition

Framing is the process of dividing a stream of bits into identifiable data units called frames.

## Types of Framing

### 1. Character Count Method

```text
| Count | Data |
```

First field specifies frame length.

### 2. Byte Stuffing

Special characters mark frame boundaries.

```text
FLAG Data FLAG
```

Extra escape characters are inserted when FLAG appears in data.

### 3. Bit Stuffing

A 0 bit is inserted after five consecutive 1s.

Example:

```text
111110 → 1111100
```

### 4. Physical Layer Coding Violations

Uses unused signal patterns as frame delimiters.

## Comparison

| Method           | Advantage | Disadvantage       |
| ---------------- | --------- | ------------------ |
| Character Count  | Simple    | Error Sensitive    |
| Byte Stuffing    | Flexible  | Overhead           |
| Bit Stuffing     | Reliable  | Extra Bits         |
| Coding Violation | Efficient | Hardware Dependent |

## Conclusion

Bit stuffing is the most commonly used framing technique in modern networks.

---

# 3. Error Detection and Error Correction (10 Marks)

## Definition

Error Detection identifies transmission errors, while Error Correction reconstructs the original data.

## Error Detection Techniques

### Parity Check

Adds one parity bit.

### Checksum

Data divided into segments and summed.

### CRC

Uses polynomial division.

## Error Correction Techniques

### Forward Error Correction (FEC)

Receiver corrects errors without retransmission.

### ARQ

Retransmission requested after error detection.

## Diagram

```text
Sender
   ↓
Add Redundancy
   ↓
Transmit
   ↓
Receiver
   ↓
Detect/Correct Error
```

## Advantages

* Reliable communication
* Data integrity

## Conclusion

Error control is essential for reliable network communication.

---

# 4. Hamming Distance (10 Marks)

## Definition

Hamming Distance is the number of differing bits between two binary strings.

## Formula

```text
Hamming Distance = Number of Different Bits
```

## Example

```text
1011101
1001001
```

Different bits = 2

Therefore:

```text
HD = 2
```

## Error Detection

For detecting d errors:

```text
Minimum Distance = d + 1
```

## Error Correction

For correcting t errors:

```text
Minimum Distance = 2t + 1
```

## Importance

* Determines error detection capability
* Determines error correction capability

## Conclusion

Hamming Distance forms the basis of block coding and Hamming Code.

---

# 5. Hamming Code (10 Marks)

## Definition

Hamming Code is an error-correcting code capable of detecting two-bit errors and correcting one-bit error.

## Formula

Number of parity bits:

2^r\geq m+r+1

Where:

* r = parity bits
* m = data bits

## Steps

### Step 1

Place parity bits at positions:

```text
1,2,4,8...
```

### Step 2

Calculate parity values.

### Step 3

Transmit codeword.

### Step 4

Receiver recalculates parity.

### Step 5

Locate and correct error.

## Diagram

```text
P1 P2 D1 P4 D2 D3 D4
```

## Advantages

* Single-bit correction
* Efficient

## Conclusion

Hamming Code is widely used for error correction in memory systems and communication networks.

---

# 6. Cyclic Redundancy Check (CRC) (10 Marks)

## Definition

CRC is an error detection technique using polynomial division.

## Components

* Dataword
* Generator Polynomial
* Remainder

## Encoding

```text
Data + Zeros
      ↓
Polynomial Division
      ↓
Remainder Added
```

## Decoding

Receiver performs same division.

```text
Remainder = 0
```

No Error

```text
Remainder ≠ 0
```

Error Present

## Diagram

```text
Dataword
    ↓
Divide by Generator
    ↓
CRC Bits
    ↓
Transmission
```

## Advantages

* High detection accuracy
* Detects burst errors

## Conclusion

CRC is the most widely used error detection technique.

---

# 7. Flow Control (10 Marks)

## Definition

Flow Control regulates data transmission speed between sender and receiver.

## Need

Prevents receiver buffer overflow.

## Types

### Stop-and-Wait

Send one frame and wait for ACK.

### Sliding Window

Send multiple frames before ACK.

## Diagram

```text
Sender
   ↓
Flow Control
   ↓
Receiver
```

## Advantages

* Prevents data loss
* Improves reliability

## Conclusion

Flow control ensures efficient data transmission.

---

# 8. Stop-and-Wait ARQ (10 Marks)

## Definition

A protocol where the sender transmits one frame and waits for ACK.

## Working

1. Send frame
2. Wait for ACK
3. Receive ACK
4. Send next frame

If timeout occurs:

```text
Retransmit
```

## Diagram

```text
Sender      Receiver
Frame ---->
      <---- ACK
```

## Advantages

* Simple
* Reliable

## Disadvantages

* Low efficiency

## Conclusion

Suitable for low-speed communication.

---

# 9. Go-Back-N ARQ (10 Marks)

## Definition

Allows multiple frames to be sent before receiving ACK.

## Working

If frame i is lost:

```text
Retransmit Frame i
and all subsequent frames
```

## Diagram

```text
0 1 2 3 4

Error at 2

Retransmit:
2 3 4
```

## Advantages

* Better throughput

## Disadvantages

* Wastes bandwidth

## Conclusion

Efficient but retransmits unnecessary frames.

---

# 10. Selective Repeat ARQ (10 Marks)

## Definition

Only erroneous frames are retransmitted.

## Working

```text
0 1 2 3 4

Error at 2

Retransmit only 2
```

## Advantages

* High efficiency
* Less retransmission

## Disadvantages

* Complex
* Requires buffering

## Conclusion

Most efficient ARQ protocol.

---

# 11. Sliding Window Protocol (10 Marks)

## Definition

A protocol that allows multiple frames to be transmitted before receiving ACK.

## Components

* Sender Window
* Receiver Window
* Sequence Numbers

## Working

```text
Window Size = 4

Send:
0 1 2 3

ACK Received

Window Slides
```

## Diagram

```text
|0|1|2|3|
      ↓
|4|5|6|7|
```

## Advantages

* High throughput
* Better utilization

## Conclusion

Foundation of modern transport protocols.

---

# 12. Piggybacking (10 Marks)

## Definition

Combining ACK with outgoing data frame.

## Working

Instead of:

```text
Data
ACK
```

Use:

```text
Data + ACK
```

## Diagram

```text
A ---- Data ----> B

A <--- Data+ACK-- B
```

## Advantages

* Saves bandwidth
* Improves efficiency

## Disadvantages

* ACK delay possible

## Conclusion

Piggybacking improves channel utilization.

---

# 13. Pure ALOHA (10 Marks)

## Definition

Users transmit whenever data is available.

## Vulnerable Time

```text
2T
```

## Throughput

genui{"math_block_widget_always_prefetch_v2":{"content":"S=Ge^{-2G}"}}

Maximum:

```text
18.4%
```

## Advantages

* Simple

## Disadvantages

* High collisions

## Conclusion

Simple but inefficient protocol.

---

# 14. Slotted ALOHA (10 Marks)

## Definition

Transmission allowed only at slot boundaries.

## Vulnerable Time

```text
T
```

## Throughput

genui{"math_block_widget_always_prefetch_v2":{"content":"S=Ge^{-G}"}}

Maximum:

```text
36.8%
```

## Advantages

* Better efficiency

## Conclusion

Improved version of Pure ALOHA.

---

# 15. CSMA (10 Marks)

## Definition

Carrier Sense Multiple Access senses the channel before transmission.

## Working

```text
Listen
  ↓
Idle?
  ↓
Transmit
```

## Types

* 1-Persistent
* Non-Persistent
* P-Persistent

## Advantages

* Reduced collisions

## Conclusion

CSMA performs better than ALOHA.

---

# 16. CSMA/CD (10 Marks)

## Definition

Carrier Sense Multiple Access with Collision Detection.

## Steps

```text
Sense
↓
Transmit
↓
Detect Collision
↓
Jam Signal
↓
Backoff
↓
Retransmit
```

## Binary Exponential Backoff

0\leq K\leq (2^n-1)

## Applications

Traditional Ethernet

## Conclusion

Used for collision detection in Ethernet.

---

# 17. CSMA/CA (10 Marks)

## Definition

Carrier Sense Multiple Access with Collision Avoidance.

## Working

```text
Sense
↓
IFS
↓
Backoff
↓
RTS
↓
CTS
↓
Data
↓
ACK
```

## Application

Wi-Fi Networks

## Conclusion

Most important protocol for wireless LANs.

---

# 18. RTS/CTS Mechanism (10 Marks)

## Full Form

* RTS = Request To Send
* CTS = Clear To Send

## Working

```text
RTS
 ↓
CTS
 ↓
DATA
 ↓
ACK
```

## Advantages

* Avoids collisions
* Solves hidden terminal problem

## Conclusion

Important collision avoidance mechanism in Wi-Fi.

---

# 19. Hidden Terminal Problem (10 Marks)

## Definition

Occurs when two stations cannot hear each other but transmit to the same receiver.

## Diagram

```text
A ---- B ---- C

A and C
cannot hear
each other
```

## Result

```text
Collision at B
```

## Solution

RTS/CTS

## Conclusion

Major issue in wireless communication.

---

# 20. CDMA (10 Marks)

## Definition

A multiple access technique using unique codes.

## Principle

```text
Same Frequency
Same Time
Different Codes
```

## Components

* Spread Spectrum
* Orthogonal Codes
* Chip Sequence

## Advantages

* High capacity
* Better security

## Disadvantages

* Complex implementation
* Near-Far Problem

## Applications

* 3G Networks
* GPS
* Military Communication

## Conclusion

CDMA provides high capacity and secure communication through code-based multiple access.
