# COMPUTER NETWORKS (MAKAUT)
# UNIT 2 – LONG ANSWER NOTES (10 MARKS)
# SET 1 (TOPICS 1–5)

---

# 1. FUNCTIONS OF DATA LINK LAYER

## Introduction

The Data Link Layer (DLL) is the second layer of the OSI Reference Model. It lies between the Physical Layer and the Network Layer. The main responsibility of the Data Link Layer is to ensure reliable and efficient transfer of data between two directly connected devices.

The Network Layer passes packets to the Data Link Layer, which converts them into frames and transmits them through the Physical Layer.

---

## Definition

The Data Link Layer is responsible for node-to-node delivery of data and provides error-free communication over a physical link.

---

## Position in OSI Model

```text
Application Layer
Presentation Layer
Session Layer
Transport Layer
Network Layer
------------------
Data Link Layer
------------------
Physical Layer
```

---

## Need for Data Link Layer

Physical Layer only transmits bits.

Problems during transmission:

- Noise
- Data corruption
- Collision
- Receiver overflow
- Frame synchronization issues

DLL solves these problems.

---

# Functions of Data Link Layer

## 1. Framing

### Definition

Framing is the process of dividing the stream of bits into manageable units called frames.

### Working

```text
Network Layer Packet
         ↓
     Framing
         ↓
       Frame
```

### Benefits

- Easy transmission
- Error detection possible
- Synchronization maintained

---

## 2. Physical Addressing

Each frame contains:

```text
Source MAC Address
Destination MAC Address
```

### Example

```text
Source:
00:11:22:33:44:55

Destination:
AA:BB:CC:DD:EE:FF
```

### Purpose

Ensures delivery to the correct device.

---

## 3. Error Control

### Purpose

Detect and correct transmission errors.

### Techniques

- Parity Check
- Checksum
- CRC
- Hamming Code

### Example

```text
Sent Data:
1011001

Received Data:
1010001
```

DLL identifies the error.

---

## 4. Flow Control

### Purpose

Prevents fast sender from overwhelming slow receiver.

### Methods

- Stop-and-Wait
- Sliding Window

---

## 5. Access Control

When multiple devices share a channel, DLL decides who can transmit.

### Examples

- CSMA/CD
- CSMA/CA
- ALOHA

---

## 6. Reliable Delivery

Ensures:

- Correct frame delivery
- No duplicate frames
- Proper sequence

---

# Diagram of DLL Functions

```text
                Data Link Layer

     +-----------------------------+
     |         Framing             |
     |     Physical Addressing     |
     |       Error Control         |
     |       Flow Control          |
     |      Access Control         |
     |     Reliable Delivery       |
     +-----------------------------+
```

---

# Advantages

- Reliable communication
- Error handling
- Efficient transmission
- Proper synchronization

---

# Disadvantages

- Additional overhead
- Processing delay
- Complex implementation

---

# Applications

- Ethernet Networks
- Wireless LAN
- Data Communication Systems

---

# Exam-Oriented Conclusion

The Data Link Layer acts as the backbone of reliable communication by providing framing, addressing, error control, flow control, and medium access control. It ensures efficient node-to-node delivery of data and is one of the most important layers in the OSI model.

---

# 2. FRAMING TECHNIQUES

## Introduction

Data transmitted through the Physical Layer is a continuous stream of bits. The receiver must know where a frame starts and ends. This process is called framing.

---

## Definition

Framing is the process of dividing a stream of bits into identifiable units called frames.

---

## Need for Framing

Without framing:

```text
101101011001110101...
```

Receiver cannot determine frame boundaries.

With framing:

```text
| Frame1 | Frame2 | Frame3 |
```

Communication becomes organized.

---

# Types of Framing

## 1. Character Count Method

### Working

The first field specifies the number of bytes in the frame.

```text
| 5 | A | B | C | D |
```

5 indicates frame length.

### Advantages

- Simple implementation

### Disadvantages

- Length corruption causes synchronization loss

---

## 2. Byte Stuffing

### Working

Special characters indicate frame boundaries.

```text
FLAG DATA FLAG
```

If FLAG appears in data:

```text
ESC FLAG
```

is inserted.

### Example

```text
FLAG ABC ESC FLAG XYZ FLAG
```

---

## 3. Bit Stuffing

### Working

Whenever five consecutive 1s occur:

```text
11111
```

Sender inserts:

```text
0
```

Result:

```text
111110
```

Receiver removes stuffed bit.

### Example

```text
Original:
1111110

Stuffed:
11111010
```

---

## 4. Physical Layer Coding Violations

Unused signal patterns are used as frame delimiters.

### Example

```text
Special Voltage Pattern
```

marks frame boundary.

---

# Comparison Table

| Technique | Advantage | Disadvantage |
|------------|------------|--------------|
| Character Count | Simple | Sensitive to errors |
| Byte Stuffing | Flexible | Additional overhead |
| Bit Stuffing | Reliable | Extra bits added |
| Coding Violation | Efficient | Hardware dependent |

---

# Framing Process Diagram

```text
Packet
   ↓
Framing
   ↓
Frame
   ↓
Transmission
```

---

# Advantages

- Synchronization
- Error detection
- Organized communication

---

# Applications

- Ethernet
- HDLC
- PPP

---

# Exam-Oriented Conclusion

Framing is a fundamental function of the Data Link Layer that identifies frame boundaries and enables reliable communication. Among all techniques, bit stuffing is the most widely used in modern networks.

---

# 3. ERROR DETECTION AND ERROR CORRECTION

## Introduction

During transmission, data may become corrupted due to noise, interference, or hardware faults. Error control techniques ensure accurate communication.

---

## Definition

Error Detection identifies errors in received data, while Error Correction reconstructs the original data.

---

# Causes of Errors

- Noise
- Electromagnetic interference
- Hardware malfunction
- Signal attenuation

---

# Error Detection Techniques

## 1. Parity Check

### Even Parity

Total number of 1s must be even.

Example:

```text
Data:
1011

Parity:
1

Transmitted:
10111
```

---

## 2. Checksum

Data blocks are added.

Receiver verifies the sum.

---

## 3. CRC

Uses polynomial division.

Most reliable detection technique.

---

# Error Correction Techniques

## 1. Forward Error Correction (FEC)

Receiver corrects errors using redundant bits.

Examples:

- Hamming Code
- Reed-Solomon Code

---

## 2. Automatic Repeat Request (ARQ)

Receiver requests retransmission.

Examples:

- Stop-and-Wait ARQ
- Go-Back-N ARQ
- Selective Repeat ARQ

---

# Error Control Process

```text
Sender
   ↓
Add Redundant Bits
   ↓
Transmission
   ↓
Receiver
   ↓
Detect Error
   ↓
Correct / Retransmit
```

---

# Advantages

- Reliable communication
- Data integrity
- Reduced data loss

---

# Disadvantages

- Extra bandwidth
- Additional processing

---

# Applications

- Computer Networks
- Satellite Systems
- Mobile Communication

---

# Exam-Oriented Conclusion

Error detection and correction are essential for maintaining data integrity and reliability in communication systems.

---

# 4. HAMMING DISTANCE

## Introduction

Hamming Distance is the foundation of error detection and correction techniques.

Developed by Richard Hamming.

---

## Definition

The Hamming Distance between two binary strings is the number of bit positions in which they differ.

---

## Formula

```text
Hamming Distance
=
Number of Different Bits
```

---

# Example

```text
Code 1:
1011101

Code 2:
1001001
```

Comparison:

```text
1011101
1001001
```

Different positions = 2

Therefore:

```text
HD = 2
```

---

# Importance

Determines:

- Error detection capability
- Error correction capability

---

# Error Detection Rule

To detect d errors:

```text
Minimum Distance = d + 1
```

---

# Error Correction Rule

To correct t errors:

```text
Minimum Distance = 2t + 1
```

---

# Example

For correcting 1-bit error:

```text
Minimum Distance
=
3
```

---

# Diagram

```text
Codeword A
     ↓
Compare
     ↓
Codeword B
     ↓
Count Different Bits
     ↓
Hamming Distance
```

---

# Applications

- Hamming Code
- CRC
- Error Control Systems

---

# Advantages

- Simple calculation
- Determines reliability

---

# Disadvantages

- Limited alone
- Requires coding techniques

---

# Exam-Oriented Conclusion

Hamming Distance is a key concept used to measure the error detection and correction capability of coding schemes and forms the basis of Hamming Codes.

---

# 5. HAMMING CODE

## Introduction

Hamming Code is one of the most important error-correcting codes used in computer networks and memory systems.

It can detect two-bit errors and correct one-bit errors.

---

## Definition

Hamming Code is a block coding technique that adds parity bits to data bits to enable error detection and correction.

---

# Need for Hamming Code

Transmission errors may occur because of noise.

Example:

```text
Sent:
1011

Received:
1001
```

The receiver must identify and correct the error.

---

# Principle

```text
Data Bits
     +
Parity Bits
     ↓
Codeword
```

---

# Formula

For m data bits and r parity bits:

:contentReference[oaicite:0]{index=0}

---

# Example

Given:

```text
m = 4
```

Find r:

```text
r = 3

2³ = 8

4+3+1 = 8
```

Hence:

```text
r = 3
```

---

# Position of Parity Bits

```text
1 2 3 4 5 6 7

P1 P2 D1 P4 D2 D3 D4
```

Parity bits are placed at:

```text
1, 2, 4, 8...
```

---

# Hamming Code Generation

Data:

```text
1011
```

Insert parity positions:

```text
P1 P2 1 P4 0 1 1
```

Calculate parity values.

Final Codeword:

```text
0110011
```

---

# Error Detection

Receiver recalculates parity.

Generates syndrome bits:

```text
S4 S2 S1
```

Example:

```text
101
```

Binary 101 = 5

Error at position 5.

---

# Error Correction

Flip erroneous bit.

```text
Received:
0110111

Corrected:
0110011
```

---

# Working Diagram

```text
Data
  ↓
Parity Generation
  ↓
Codeword
  ↓
Transmission
  ↓
Receiver
  ↓
Syndrome Check
  ↓
Correction
```

---

# Advantages

- Corrects single-bit errors
- Detects double-bit errors
- No retransmission required
- Reliable communication

---

# Disadvantages

- Extra parity bits
- Cannot correct multiple-bit errors
- Additional processing overhead

---

# Applications

- RAM Memory Systems
- Satellite Communication
- Wireless Communication
- Networking Equipment

---

# Important Exam Points

★ Hamming Code is a Block Coding Technique

★ Corrects 1-bit Error

★ Detects 2-bit Errors

★ Parity positions:

```text
1, 2, 4, 8, 16...
```

★ Formula:

:contentReference[oaicite:1]{index=1}

---

# Exam-Oriented Conclusion

Hamming Code is one of the most effective and widely used error-correction techniques. By adding parity bits at specific positions, it can identify and correct transmission errors efficiently, making communication systems more reliable.

---
# END OF SET 1
---

# COMPUTER NETWORKS (MAKAUT)
# UNIT 2 – LONG ANSWER NOTES (10 MARKS)
# SET 2 (TOPICS 6–10)

---

# 6. CYCLIC REDUNDANCY CHECK (CRC)

## Introduction

In data communication, errors may occur during transmission due to noise, interference, attenuation, or hardware faults. To ensure reliable communication, error detection techniques are used.

Among all error detection techniques, **Cyclic Redundancy Check (CRC)** is the most widely used because of its high accuracy in detecting transmission errors.

CRC is used in:

- Ethernet
- Wi-Fi
- HDLC
- USB
- Storage Devices
- Data Communication Networks

---

## Definition

Cyclic Redundancy Check (CRC) is an error detection technique in which a binary message is divided by a predefined binary polynomial and the remainder is attached to the message before transmission.

The receiver performs the same division. If the remainder is zero, the data is assumed to be error-free.

---

# Basic Terminology

## Dataword

The original data to be transmitted.

Example:

```text
1011001
```

---

## Generator Polynomial (Divisor)

A predefined binary pattern used for division.

Example:

```text
1101
```

---

## CRC Bits

The remainder obtained after division.

---

## Codeword

```text
Codeword = Dataword + CRC Bits
```

---

# Working Principle of CRC

CRC uses modulo-2 division.

Characteristics:

```text
Addition = XOR

Subtraction = XOR

No Carry

No Borrow
```

---

# CRC Encoding Process

## Step 1

Choose a generator polynomial.

Example:

```text
G = 1101
```

---

## Step 2

Append zeros to data.

If generator length = 4

Append:

```text
3 zeros
```

Example:

```text
Data = 1011001

Modified Data

1011001000
```

---

## Step 3

Perform modulo-2 division.

```text
1011001000 ÷ 1101
```

---

## Step 4

Obtain remainder.

Example:

```text
Remainder = 011
```

---

## Step 5

Attach remainder to original data.

```text
Codeword

1011001 011
```

---

# CRC Encoding Diagram

```text
Dataword
    ↓
Append Zeros
    ↓
Modulo-2 Division
    ↓
CRC Remainder
    ↓
Codeword
```

---

# CRC Decoding Process

At receiver:

## Step 1

Receive codeword.

## Step 2

Perform same division.

## Step 3

Check remainder.

If:

```text
Remainder = 0
```

No Error.

If:

```text
Remainder ≠ 0
```

Error Detected.

---

# CRC Decoding Diagram

```text
Received Frame
      ↓
Modulo-2 Division
      ↓
Remainder Check
      ↓
Accept / Reject
```

---

# Error Detection Capability

CRC can detect:

### Single-Bit Errors

✔ Detects all.

### Double-Bit Errors

✔ Detects most.

### Odd Number of Errors

✔ Detects.

### Burst Errors

✔ Very effective.

---

# Advantages

### High Accuracy

More reliable than parity and checksum.

### Burst Error Detection

Excellent detection capability.

### Fast Hardware Implementation

Easy using shift registers.

### Widely Used

Industry standard.

---

# Disadvantages

### Error Correction Not Possible

Only detects errors.

### Computational Complexity

More complex than parity.

---

# Applications

- Ethernet Frames
- HDLC
- USB Communication
- Storage Systems
- Wireless Networks

---

# Important Exam Points

⭐ CRC uses polynomial division.

⭐ Uses modulo-2 arithmetic.

⭐ Most widely used error detection method.

⭐ Detects burst errors efficiently.

---

# Exam-Oriented Conclusion

CRC is one of the most powerful error detection techniques used in modern communication systems. Its ability to detect burst errors with high accuracy makes it the preferred method in computer networks.

---

# 7. FLOW CONTROL

## Introduction

In a communication system, the sender and receiver often operate at different speeds.

If a fast sender continuously sends data to a slow receiver, the receiver's buffer may overflow, resulting in data loss.

Flow Control solves this problem.

---

## Definition

Flow Control is the technique used to regulate the rate of data transmission between sender and receiver.

---

# Need for Flow Control

Consider:

```text
Sender Speed
=
100 Mbps

Receiver Speed
=
10 Mbps
```

Without flow control:

```text
Receiver Buffer Overflow
```

Data loss occurs.

---

# Objectives

- Prevent buffer overflow
- Improve reliability
- Synchronize communication

---

# Types of Flow Control

```text
Flow Control
     |
+----+----+
|         |
Stop & Wait
Sliding Window
```

---

# 1. Stop-and-Wait Flow Control

## Working

### Step 1

Send one frame.

### Step 2

Wait for ACK.

### Step 3

Receive ACK.

### Step 4

Send next frame.

---

## Diagram

```text
Sender         Receiver

Frame 1 ---->

        <---- ACK

Frame 2 ---->

        <---- ACK
```

---

# 2. Sliding Window Flow Control

Multiple frames can be sent before ACK arrives.

---

## Diagram

```text
Window Size = 4

0 1 2 3
```

All four frames can be transmitted.

---

# Advantages

- Prevents data loss
- Efficient communication
- Reliable transmission

---

# Disadvantages

- Additional overhead
- Complex implementation

---

# Applications

- TCP Protocol
- Data Communication
- Wireless Networks

---

# Exam-Oriented Conclusion

Flow control is essential for matching sender and receiver speeds and ensuring reliable data transmission without buffer overflow.

---

# 8. STOP-AND-WAIT ARQ

## Introduction

ARQ stands for Automatic Repeat reQuest.

It combines:

- Error Detection
- Acknowledgement
- Retransmission

to achieve reliable communication.

---

## Definition

Stop-and-Wait ARQ is an error control protocol in which the sender transmits one frame and waits for acknowledgement before sending the next frame.

---

# Working Principle

## Step 1

Sender sends frame.

```text
Frame 0
```

---

## Step 2

Receiver receives frame.

---

## Step 3

Receiver sends ACK.

```text
ACK 0
```

---

## Step 4

Sender transmits next frame.

---

# Normal Operation

```text
Sender          Receiver

Frame 0 ----->

         <----- ACK 0

Frame 1 ----->

         <----- ACK 1
```

---

# Lost Frame Scenario

```text
Frame Lost
```

Sender waits.

Timeout occurs.

Retransmission starts.

---

# Timeout Mechanism

If ACK not received within a specified time:

```text
Timeout
      ↓
Retransmit Frame
```

---

# Advantages

- Simple
- Easy implementation
- Reliable

---

# Disadvantages

- Low throughput
- Poor channel utilization
- Large waiting time

---

# Applications

- Low-speed communication
- Simple communication systems

---

# Exam-Oriented Conclusion

Stop-and-Wait ARQ provides reliable communication through acknowledgements and retransmissions, although its efficiency is limited due to waiting delays.

---

# 9. GO-BACK-N ARQ

## Introduction

Stop-and-Wait ARQ wastes bandwidth because only one frame can be transmitted at a time.

Go-Back-N improves efficiency using sliding windows.

---

## Definition

Go-Back-N ARQ is an error control protocol that allows multiple frames to be sent before acknowledgement is received.

---

# Basic Concept

Sender maintains a window.

Example:

```text
Window Size = 4
```

Sender can send:

```text
0 1 2 3
```

without waiting.

---

# Working

## Step 1

Send multiple frames.

```text
0 1 2 3
```

---

## Step 2

Receiver receives frames.

---

## Step 3

Suppose Frame 2 is lost.

---

## Step 4

Receiver discards:

```text
2 3
```

---

## Step 5

Sender retransmits:

```text
2 3
```

---

# Diagram

```text
0 ✓
1 ✓
2 ✗
3 Received but Discarded

Retransmit:
2 3
```

---

# Sender Window

Contains frames allowed for transmission.

---

# Receiver Window

Size = 1

Only next expected frame accepted.

---

# Advantages

- Better throughput
- Improved efficiency
- Continuous transmission

---

# Disadvantages

- Wastes bandwidth
- Retransmits correct frames
- Receiver complexity

---

# Applications

- Data Communication
- Transport Protocols

---

# Exam-Oriented Conclusion

Go-Back-N ARQ significantly improves throughput compared to Stop-and-Wait but may waste bandwidth due to retransmission of correctly received frames.

---

# 10. SELECTIVE REPEAT ARQ

## Introduction

Go-Back-N retransmits all frames after an error.

Selective Repeat improves efficiency by retransmitting only the erroneous frame.

---

## Definition

Selective Repeat ARQ is an error control protocol in which only lost or corrupted frames are retransmitted.

---

# Working Principle

## Step 1

Sender transmits:

```text
0 1 2 3
```

---

## Step 2

Frame 2 is lost.

---

## Step 3

Receiver stores:

```text
3
```

in buffer.

---

## Step 4

Receiver requests:

```text
Frame 2
```

only.

---

## Step 5

Sender retransmits Frame 2.

---

# Diagram

```text
0 ✓
1 ✓
2 ✗
3 ✓ Stored

Retransmit:
2 Only
```

---

# Sender Window

Multiple outstanding frames allowed.

---

# Receiver Window

Can accept out-of-order frames.

---

# Buffering

Receiver stores correctly received frames until missing frame arrives.

---

# Advantages

### High Efficiency

Only erroneous frames retransmitted.

### Better Bandwidth Utilization

No unnecessary retransmissions.

### High Throughput

Suitable for long-distance communication.

---

# Disadvantages

### Complex Implementation

Requires buffering.

### More Memory Required

Stores out-of-order frames.

### Complex Window Management

Additional processing needed.

---

# Comparison: Stop-and-Wait vs Go-Back-N vs Selective Repeat

| Feature | Stop-and-Wait | Go-Back-N | Selective Repeat |
|----------|---------------|------------|------------------|
| Frames Sent | One | Multiple | Multiple |
| Retransmission | One Frame | All Following Frames | Only Error Frame |
| Efficiency | Low | Medium | High |
| Complexity | Low | Medium | High |
| Buffering | No | No | Yes |

---

# Applications

- TCP Communication
- Satellite Networks
- Wireless Communication
- High-Speed Networks

---

# Important Exam Points

⭐ Most efficient ARQ protocol.

⭐ Receiver accepts out-of-order frames.

⭐ Uses buffering.

⭐ Retransmits only erroneous frames.

---

# Exam-Oriented Conclusion

Selective Repeat ARQ is the most efficient ARQ protocol because it retransmits only the lost or corrupted frames. Although it is more complex and requires buffering, it provides excellent bandwidth utilization and high throughput, making it suitable for modern communication systems.

---
# END OF SET 2
---

# COMPUTER NETWORKS (MAKAUT)
# UNIT 2 – LONG ANSWER NOTES (10 MARKS)
# SET 3 (TOPICS 11–15)

---

# 11. SLIDING WINDOW PROTOCOL

## Introduction

In Stop-and-Wait protocol, the sender waits for an acknowledgement after sending each frame. This leads to poor utilization of bandwidth, especially in high-speed networks.

To overcome this limitation, the Sliding Window Protocol was introduced.

It allows multiple frames to be transmitted before receiving acknowledgements, thereby increasing network efficiency and throughput.

---

## Definition

Sliding Window Protocol is a flow control protocol that allows the sender to transmit multiple frames before receiving acknowledgements.

The sender and receiver maintain windows that determine which frames can be sent or received.

---

# Need for Sliding Window Protocol

Problems with Stop-and-Wait:

- Low throughput
- High waiting time
- Poor channel utilization
- Increased transmission delay

Solution:

```text
Send Multiple Frames
Without Waiting
For Every ACK
```

---

# Basic Concept

A "window" represents the set of frames that can be transmitted or received at a given time.

---

# Components of Sliding Window Protocol

## 1. Sender Window

Contains frames that can be transmitted.

---

## 2. Receiver Window

Contains frames that can be accepted.

---

## 3. Window Size

Maximum number of outstanding frames allowed.

---

## 4. Sequence Numbers

Used to uniquely identify frames.

---

# Working Principle

Assume:

```text
Window Size = 4
```

Sender can send:

```text
0 1 2 3
```

without waiting.

---

## Step 1

Transmit frames.

```text
0 1 2 3
```

---

## Step 2

Receiver sends ACK.

```text
ACK 0
```

---

## Step 3

Window slides forward.

```text
Before:

0 1 2 3

After ACK 0:

1 2 3 4
```

---

## Step 4

Sender sends new frame.

```text
Frame 4
```

---

# Sliding Window Diagram

```text
Initial Window

+---+---+---+---+
| 0 | 1 | 2 | 3 |
+---+---+---+---+

ACK 0 Received

+---+---+---+---+
| 1 | 2 | 3 | 4 |
+---+---+---+---+
```

---

# Window Movement

```text
Send Frame
      ↓
Receive ACK
      ↓
Window Slides
      ↓
Send New Frame
```

---

# Sequence Numbering

Frames are numbered:

```text
0,1,2,3,4...
```

Used for:

- Frame identification
- Duplicate detection
- Error control

---

# Advantages

### High Throughput

Multiple frames transmitted simultaneously.

### Better Bandwidth Utilization

Channel remains busy.

### Reduced Waiting Time

Improves efficiency.

### Supports Long Distance Communication

Ideal for large-delay networks.

---

# Disadvantages

### Complex Implementation

Requires window management.

### Buffer Requirement

Frames must be stored.

### Sequence Number Management

Additional processing needed.

---

# Applications

- TCP Protocol
- ARQ Protocols
- Wireless Networks
- Satellite Communication

---

# Important Exam Points

⭐ Sender Window

⭐ Receiver Window

⭐ Sequence Numbers

⭐ Window Sliding Mechanism

⭐ Flow Control Improvement

---

# Exam-Oriented Conclusion

The Sliding Window Protocol is an efficient flow control mechanism that significantly improves network performance by allowing multiple frames to be transmitted before acknowledgement. It forms the foundation of modern transport protocols such as TCP.

---

# 12. PIGGYBACKING

## Introduction

In bidirectional communication, both sender and receiver may have data to transmit.

Sending separate acknowledgements consumes bandwidth.

Piggybacking improves efficiency by combining acknowledgements with outgoing data frames.

---

## Definition

Piggybacking is a technique in which the acknowledgement for a received frame is attached to the outgoing data frame instead of being sent separately.

---

# Need for Piggybacking

Without Piggybacking:

```text
Data
ACK
Data
ACK
```

Large number of control frames.

---

With Piggybacking:

```text
Data + ACK
```

Single transmission.

---

# Working Principle

## Step 1

Station A sends data to Station B.

---

## Step 2

Station B receives data.

---

## Step 3

Instead of sending ACK immediately, B waits.

---

## Step 4

When B has data to send, it attaches ACK.

---

## Step 5

Combined frame transmitted.

---

# Diagram

```text
Station A                 Station B

Data -------------------->

      Data + ACK <--------
```

---

# Normal Communication

Without Piggybacking:

```text
A → Data

B → ACK

B → Data

A → ACK
```

---

# With Piggybacking

```text
A → Data

B → Data + ACK
```

---

# Advantages

### Better Bandwidth Utilization

Fewer control frames.

### Reduced Overhead

Less ACK traffic.

### Improved Efficiency

More useful data transmitted.

### Reduced Network Congestion

Fewer packets.

---

# Disadvantages

### ACK Delay

Receiver may wait too long.

### Increased Complexity

Additional processing required.

### Not Suitable for Unidirectional Traffic

Works best in bidirectional communication.

---

# Applications

- Sliding Window Protocol
- TCP Communication
- Data Link Layer Protocols

---

# Important Exam Points

⭐ ACK attached with outgoing data.

⭐ Saves bandwidth.

⭐ Reduces overhead.

⭐ Used in full-duplex communication.

---

# Exam-Oriented Conclusion

Piggybacking is an efficient technique that improves channel utilization by combining acknowledgements with outgoing data frames. It reduces overhead and enhances communication efficiency.

---

# 13. PURE ALOHA

## Introduction

ALOHA was one of the earliest random access protocols developed for wireless communication.

In Pure ALOHA, a station transmits whenever it has data to send without checking the channel.

---

## Definition

Pure ALOHA is a random access protocol in which a station transmits data immediately whenever data becomes available.

---

# Working Principle

## Step 1

Station generates data.

---

## Step 2

Transmit immediately.

---

## Step 3

Wait for acknowledgement.

---

## Step 4

If ACK received:

```text
Success
```

---

## Step 5

If ACK not received:

```text
Collision Occurred
```

Retransmit after random delay.

---

# Pure ALOHA Diagram

```text
Station A --->

Station B --->

Collision
```

---

# Vulnerable Time

The period during which a collision may occur.

For Pure ALOHA:

```text
Vulnerable Time = 2T
```

Where:

```text
T = Frame Transmission Time
```

---

# Throughput

Formula:


::contentReference[oaicite:0]{index=0}


Maximum Throughput:

```text
18.4%
```

---

# Advantages

### Simple Implementation

No synchronization required.

### Easy to Understand

Straightforward operation.

### Low Cost

Minimal hardware requirements.

---

# Disadvantages

### High Collision Rate

Frequent collisions occur.

### Poor Efficiency

Only 18.4%.

### Bandwidth Wastage

Retransmissions consume resources.

---

# Applications

- Early Wireless Networks
- Satellite Communication

---

# Important Exam Points

⭐ Vulnerable Time = 2T

⭐ Throughput = 18.4%

⭐ No Channel Sensing

---

# Exam-Oriented Conclusion

Pure ALOHA is a simple random access protocol but suffers from high collision rates and low efficiency, making it unsuitable for modern high-speed networks.

---

# 14. SLOTTED ALOHA

## Introduction

Slotted ALOHA is an improved version of Pure ALOHA designed to reduce collisions and improve throughput.

Time is divided into equal slots.

Stations can transmit only at slot boundaries.

---

## Definition

Slotted ALOHA is a random access protocol in which transmission is allowed only at the beginning of predefined time slots.

---

# Working Principle

## Step 1

Time divided into slots.

---

## Step 2

Station waits for next slot.

---

## Step 3

Transmit at slot boundary.

---

## Step 4

Receive ACK.

---

## Step 5

Retransmit if collision occurs.

---

# Diagram

```text
| Slot 1 | Slot 2 | Slot 3 |

      ↑
Transmit Here
```

---

# Vulnerable Time

For Slotted ALOHA:

```text
Vulnerable Time = T
```

Half of Pure ALOHA.

---

# Throughput

Formula:


::contentReference[oaicite:1]{index=1}


Maximum Throughput:

```text
36.8%
```

---

# Comparison with Pure ALOHA

| Feature | Pure ALOHA | Slotted ALOHA |
|----------|------------|---------------|
| Synchronization | Not Required | Required |
| Vulnerable Time | 2T | T |
| Efficiency | 18.4% | 36.8% |
| Collision Rate | High | Lower |

---

# Advantages

### Better Efficiency

Twice Pure ALOHA.

### Reduced Collision

Transmission occurs at slots.

### Improved Throughput

Higher performance.

---

# Disadvantages

### Synchronization Required

All stations must be synchronized.

### Slot Wastage

Unused slots waste bandwidth.

---

# Applications

- Satellite Networks
- Wireless Communication

---

# Important Exam Points

⭐ Vulnerable Time = T

⭐ Throughput = 36.8%

⭐ Time Slot Concept

---

# Exam-Oriented Conclusion

Slotted ALOHA significantly improves the performance of Pure ALOHA by reducing vulnerable time and increasing throughput, making it a more efficient random access protocol.

---

# 15. CSMA (CARRIER SENSE MULTIPLE ACCESS)

## Introduction

ALOHA protocols suffer from excessive collisions because stations transmit without checking the channel.

CSMA improves performance by sensing the channel before transmission.

---

## Definition

Carrier Sense Multiple Access (CSMA) is a random access protocol in which a station listens to the channel before transmitting.

---

# Basic Principle

```text
Listen Before Talk
```

---

# Working Principle

## Step 1

Station wants to transmit.

---

## Step 2

Sense the channel.

---

## Step 3

If channel idle:

```text
Transmit
```

---

## Step 4

If channel busy:

```text
Wait
```

---

# CSMA Diagram

```text
Station
    ↓
Sense Channel
    ↓
Idle?
   / \
 Yes  No
  |    |
Transmit Wait
```

---

# Persistence Methods

## 1. 1-Persistent CSMA

### Working

If channel becomes free:

```text
Transmit Immediately
```

### Advantage

Simple.

### Disadvantage

High collision probability.

---

## 2. Non-Persistent CSMA

### Working

If channel busy:

```text
Wait Random Time
```

before sensing again.

### Advantage

Lower collision rate.

### Disadvantage

Higher delay.

---

## 3. P-Persistent CSMA

### Working

When channel becomes idle:

Transmit with probability P.

Wait with probability:

```text
1 - P
```

### Advantage

Balanced performance.

---

# Performance

CSMA performs better than:

```text
Pure ALOHA
Slotted ALOHA
```

because collisions are reduced.

---

# Advantages

### Reduced Collisions

Channel checked before transmission.

### Better Throughput

Improved performance.

### Efficient Channel Usage

Less bandwidth waste.

---

# Disadvantages

### Collision Still Possible

Propagation delay may cause collisions.

### Not Perfect

Cannot completely eliminate collisions.

---

# Applications

- Ethernet Networks
- LAN Technologies
- Wireless Communication

---

# Important Exam Points

⭐ Listen Before Talk

⭐ Carrier Sensing

⭐ Persistence Methods

⭐ Better than ALOHA

---

# Exam-Oriented Conclusion

CSMA is a significant improvement over ALOHA protocols because it reduces collisions through carrier sensing. It forms the basis for advanced protocols such as CSMA/CD and CSMA/CA used in modern networks.

---
# END OF SET 3
---

# COMPUTER NETWORKS (MAKAUT)
# UNIT 2 – LONG ANSWER NOTES (10 MARKS)
# SET 4 (TOPICS 16–20)

---

# 16. CSMA/CD (Carrier Sense Multiple Access with Collision Detection)

## Introduction

Although CSMA reduces collisions by sensing the channel before transmission, collisions can still occur due to propagation delay. To overcome this issue, Ethernet networks use CSMA/CD.

CSMA/CD is one of the most important MAC protocols and is frequently asked in MAKAUT examinations.

---

## Definition

CSMA/CD (Carrier Sense Multiple Access with Collision Detection) is a medium access control protocol in which a station senses the channel before transmitting and continuously monitors the channel to detect collisions during transmission.

---

# Need for CSMA/CD

Consider two stations:

```text
A ---------------- B
```

Both sense the channel at nearly the same time.

Both find it idle.

Both transmit simultaneously.

Result:

```text
Collision
```

Therefore collision detection becomes necessary.

---

# Basic Principles

## 1. Carrier Sense

Listen before transmission.

## 2. Multiple Access

Many devices share the same medium.

## 3. Collision Detection

Detect collision during transmission.

---

# Working Principle

## Step 1

Station senses channel.

---

## Step 2

If channel idle:

```text
Transmit Frame
```

---

## Step 3

While transmitting:

```text
Monitor Channel
```

---

## Step 4

If collision detected:

```text
Stop Transmission
```

---

## Step 5

Send Jam Signal.

---

## Step 6

Apply Backoff Algorithm.

---

## Step 7

Retransmit later.

---

# CSMA/CD Operation Diagram

```text
Station
    ↓
Sense Channel
    ↓
Idle?
   / \
 Yes  No
  |    |
Transmit Wait
  |
Collision?
  |
Yes
  |
Send Jam Signal
  |
Backoff
  |
Retransmit
```

---

# Jam Signal

A special signal transmitted after collision detection.

Purpose:

- Inform all stations
- Ensure collision awareness

---

# Backoff Algorithm

After collision:

```text
Wait Random Time
```

before retransmission.

This reduces future collisions.

---

# Binary Exponential Backoff

Most important MAKAUT topic.

### Working

After nth collision:

Choose random number:

:contentReference[oaicite:0]{index=0}

Wait:

```text
K × Slot Time
```

before retransmitting.

---

## Example

### First Collision

```text
n = 1

K = 0 or 1
```

---

### Second Collision

```text
n = 2

K = 0,1,2,3
```

---

### Third Collision

```text
n = 3

K = 0 to 7
```

---

# Advantages

### Collision Detection

Detects collisions immediately.

### Better Throughput

Compared to ALOHA.

### Efficient Medium Utilization

Bandwidth is used effectively.

### Reduced Retransmissions

Backoff algorithm minimizes repeated collisions.

---

# Disadvantages

### Not Suitable for Wireless Networks

Collision detection difficult in wireless media.

### Performance Decreases Under Heavy Load

Frequent collisions reduce efficiency.

### Requires Shared Medium

Cannot be used in switched Ethernet.

---

# Applications

- Traditional Ethernet
- LAN Networks
- Shared Bus Networks

---

# Important Exam Points

⭐ Carrier Sense

⭐ Multiple Access

⭐ Collision Detection

⭐ Jam Signal

⭐ Binary Exponential Backoff

⭐ Ethernet Protocol

---

# Exam-Oriented Conclusion

CSMA/CD is an important MAC protocol used in traditional Ethernet networks. By detecting collisions and applying binary exponential backoff, it improves network efficiency and throughput significantly.

---

# 17. CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)

## Introduction

In wireless networks, collision detection is difficult because a station cannot transmit and listen simultaneously.

Therefore, collision avoidance is used instead of collision detection.

This protocol is known as CSMA/CA.

---

## Definition

CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance) is a MAC protocol that attempts to avoid collisions before transmission using carrier sensing, waiting periods, random backoff, and RTS/CTS mechanisms.

---

# Need for CSMA/CA

Problems in wireless communication:

- Hidden Terminal Problem
- Exposed Terminal Problem
- Difficult collision detection

Solution:

```text
Avoid Collision
Instead of
Detecting Collision
```

---

# Working Principle

## Step 1

Sense the channel.

---

## Step 2

If channel busy:

```text
Wait
```

---

## Step 3

If channel idle:

Wait for IFS.

---

## Step 4

Generate random backoff.

---

## Step 5

Transmit RTS.

---

## Step 6

Receive CTS.

---

## Step 7

Send Data.

---

## Step 8

Receive ACK.

---

# CSMA/CA Flow Diagram

```text
Sense Channel
      ↓
Idle?
      ↓
IFS Wait
      ↓
Random Backoff
      ↓
RTS
      ↓
CTS
      ↓
DATA
      ↓
ACK
```

---

# Interframe Space (IFS)

A waiting period before transmission.

Purpose:

- Reduce collisions
- Prioritize traffic

---

# Random Backoff

Random waiting time before transmission.

Benefits:

- Prevent simultaneous transmissions
- Reduce collision probability

---

# Advantages

### Collision Avoidance

Reduces collision occurrence.

### Suitable for Wireless Networks

Designed specifically for WLANs.

### Better Reliability

Improves communication quality.

---

# Disadvantages

### Additional Overhead

RTS/CTS adds control packets.

### Increased Delay

Waiting periods introduce latency.

### Complex Implementation

Requires more processing.

---

# Applications

- Wi-Fi Networks
- IEEE 802.11
- Wireless LANs

---

# Important Exam Points

⭐ Collision Avoidance

⭐ IFS

⭐ Random Backoff

⭐ RTS/CTS

⭐ Wi-Fi Protocol

---

# Exam-Oriented Conclusion

CSMA/CA is the fundamental access protocol used in wireless networks. By avoiding collisions through RTS/CTS and backoff mechanisms, it ensures reliable wireless communication.

---

# 18. RTS/CTS MECHANISM

## Introduction

The RTS/CTS mechanism is used in CSMA/CA to reduce collisions and solve hidden terminal problems.

It reserves the channel before actual data transmission.

---

## Full Form

RTS = Request To Send

CTS = Clear To Send

---

# Purpose

- Avoid collisions
- Reserve medium
- Solve hidden terminal problem

---

# Working Principle

## Step 1

Sender sends RTS.

---

## Step 2

Receiver receives RTS.

---

## Step 3

Receiver replies with CTS.

---

## Step 4

Other stations hearing CTS remain silent.

---

## Step 5

Sender transmits data.

---

## Step 6

Receiver sends ACK.

---

# RTS/CTS Diagram

```text
Sender                Receiver

RTS ---------------->

      <-------------- CTS

DATA --------------->

      <-------------- ACK
```

---

# Channel Reservation Process

```text
RTS
 ↓
CTS
 ↓
Reserve Channel
 ↓
Data Transmission
 ↓
ACK
```

---

# Advantages

### Collision Reduction

Avoids data packet collisions.

### Hidden Terminal Solution

Improves wireless communication.

### Better Channel Utilization

Medium reserved before use.

---

# Disadvantages

### Additional Overhead

Extra control packets.

### Reduced Efficiency for Small Frames

Control packets may exceed data size.

### Increased Delay

Extra communication required.

---

# Applications

- IEEE 802.11
- Wi-Fi Networks
- Wireless LANs

---

# Important Exam Points

⭐ RTS = Request To Send

⭐ CTS = Clear To Send

⭐ Channel Reservation

⭐ Hidden Terminal Solution

---

# Exam-Oriented Conclusion

RTS/CTS is an important collision avoidance mechanism used in wireless networks. It reserves the channel before transmission and significantly reduces collisions.

---

# 19. HIDDEN TERMINAL PROBLEM

## Introduction

The Hidden Terminal Problem is one of the most important issues in wireless communication systems.

It occurs when two stations cannot hear each other but attempt to communicate with the same receiver.

---

## Definition

A Hidden Terminal Problem occurs when two transmitting stations are outside each other's communication range but within range of a common receiver.

---

# Scenario

Consider:

```text
A -------- B -------- C
```

A and C cannot hear each other.

Both communicate with B.

---

# Problem

A senses channel.

Finds it idle.

Transmits.

At same time:

C senses channel.

Also finds it idle.

Transmits.

---

# Result

```text
Collision at B
```

---

# Diagram

```text
A ----->

       B

<----- C

Collision at B
```

---

# Why It Occurs

Wireless stations cannot always detect all nearby transmissions.

Physical obstacles and distance create hidden nodes.

---

# Effects

### Increased Collisions

Many packets collide.

### Reduced Throughput

Network performance decreases.

### Packet Loss

Data retransmissions increase.

### Higher Delay

Communication becomes slower.

---

# Solution

Use RTS/CTS.

### Working

A sends RTS.

B sends CTS.

C hears CTS.

C remains silent.

Collision avoided.

---

# Solution Diagram

```text
A → RTS

B → CTS

C Hears CTS
↓
Remain Silent
```

---

# Advantages of RTS/CTS Solution

- Collision reduction
- Improved throughput
- Better reliability

---

# Applications

- Wi-Fi Networks
- Wireless LANs
- Mobile Communication

---

# Important Exam Points

⭐ Hidden Nodes

⭐ Common Receiver

⭐ Collision at Receiver

⭐ RTS/CTS Solution

---

# Exam-Oriented Conclusion

The Hidden Terminal Problem is a major challenge in wireless communication. The RTS/CTS mechanism effectively minimizes collisions and improves overall network performance.

---

# 20. CDMA (Code Division Multiple Access)

## Introduction

Traditional multiple access techniques divide resources using frequency or time.

CDMA uses a different approach.

All users share:

- Same Frequency
- Same Time

but use different codes.

This makes CDMA one of the most advanced multiple access techniques.

---

## Definition

Code Division Multiple Access (CDMA) is a channel access method in which multiple users simultaneously share the same frequency spectrum using unique code sequences.

---

# Spread Spectrum Concept

CDMA uses Spread Spectrum Technology.

Data is spread over a wide bandwidth.

Benefits:

- Security
- Noise resistance
- Multiple user support

---

# Basic Principle

```text
Same Frequency
Same Time
Different Codes
```

---

# Orthogonal Codes

Each user receives a unique code.

Example:

```text
User A = 1010

User B = 1100

User C = 0110
```

Codes are orthogonal.

---

# Chip Sequence

Each bit is represented by multiple chips.

Example:

```text
Bit 1

↓

1 1 -1 -1
```

---

# CDMA Encoding Process

## Step 1

Generate user code.

---

## Step 2

Multiply data by code.

---

## Step 3

Transmit encoded signal.

---

# Encoding Diagram

```text
Data
  ↓
User Code
  ↓
Spread Signal
  ↓
Transmission
```

---

# CDMA Decoding Process

## Step 1

Receive combined signal.

---

## Step 2

Apply same code.

---

## Step 3

Recover original data.

---

# Decoding Diagram

```text
Received Signal
       ↓
Apply User Code
       ↓
Original Data
```

---

# Advantages

### High Capacity

Many users simultaneously supported.

### Better Security

Codes provide privacy.

### Resistance to Interference

Spread spectrum improves reliability.

### Efficient Spectrum Usage

Bandwidth shared effectively.

---

# Disadvantages

### Complex Implementation

Requires sophisticated hardware.

### Near-Far Problem

Strong signals may dominate weak signals.

### Power Control Requirement

Precise control necessary.

---

# Applications

- 3G Mobile Networks
- GPS Systems
- Satellite Communication
- Military Communication
- Wireless Networks

---

# Comparison: FDMA vs TDMA vs CDMA

| Feature | FDMA | TDMA | CDMA |
|----------|------|------|------|
| Resource Division | Frequency | Time | Code |
| Synchronization | Low | High | Moderate |
| Capacity | Medium | High | Very High |
| Security | Low | Medium | High |
| Interference Resistance | Low | Medium | High |

---

# Important Exam Points

⭐ Spread Spectrum

⭐ Orthogonal Codes

⭐ Chip Sequence

⭐ Encoding Process

⭐ Decoding Process

⭐ Same Frequency + Same Time + Different Codes

---

# Exam-Oriented Conclusion

CDMA is a highly efficient multiple access technique that allows multiple users to share the same frequency band simultaneously using unique codes. Due to its high capacity, security, and interference resistance, CDMA has been widely used in modern wireless communication systems.

---
# END OF SET 4