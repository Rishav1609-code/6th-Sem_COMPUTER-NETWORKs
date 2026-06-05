# Computer Networks – Unit 1 Notes

# Data Communication (MAKAUT Exam-Oriented Notes)

---

# 📖 Topic Overview

Data Communication is the process of exchanging data between two or more devices through a transmission medium. It forms the foundation of all computer networks, including the Internet, mobile communication, cloud computing, IoT, and distributed systems.

### Why is it Important?

* Enables communication between computers and devices.
* Supports Internet services.
* Facilitates resource sharing.
* Forms the basis of networking technologies.

### Real-World Applications

* Email
* Video conferencing
* Online banking
* Social media
* Cloud computing
* E-commerce
* IoT devices

---

# 🎯 Learning Objectives

After studying this chapter, you will be able to:

✔ Understand data communication fundamentals.

✔ Identify components of a communication system.

✔ Explain different data representations.

✔ Distinguish between simplex, half-duplex, and full-duplex communication.

✔ Answer MAKAUT exam questions confidently.

---

# 1.1 Introduction to Data Communication

---

## Definition of Data Communication

### Textbook Definition

Data Communication is the exchange of data between two or more devices through a transmission medium such as cables, optical fibers, or wireless channels.

### Simple Definition

Whenever information travels from one device to another, it is called data communication.

### Example

* Sending a WhatsApp message
* Downloading a file
* Watching YouTube videos

---

## Communication Process

```text
Sender
   │
   ▼
Transmission Medium
   │
   ▼
Receiver
```

Example:

```text
Laptop ──Wi-Fi──► Router ──Internet──► Server
```

---

# Characteristics of Effective Data Communication

For communication to be effective, four conditions must be satisfied.

---

## 1. Delivery

Data must reach the correct destination.

### Example

An email intended for Alice should not be delivered to Bob.

---

## 2. Accuracy

Data should arrive without errors.

### Example

File sent = File received

No corruption should occur.

---

## 3. Timeliness

Data must arrive on time.

### Example

Live video conferencing requires real-time transmission.

---

## 4. Jitter

Variation in packet arrival times should be minimal.

### Example

Voice calls become choppy when jitter is high.

---

### Memory Trick

👉 DAJT

D → Delivery

A → Accuracy

J → Jitter

T → Timeliness

---

# Applications of Data Communication

---

## 1. Business Communication

* Email
* Online meetings
* File sharing

---

## 2. Banking

* ATM networks
* Online transactions
* Mobile banking

---

## 3. Education

* Online classes
* Digital libraries
* E-learning platforms

---

## 4. Healthcare

* Telemedicine
* Electronic health records

---

## 5. Entertainment

* Netflix
* YouTube
* Online gaming

---

# 1.2 Components of Data Communication

A data communication system consists of five components.

---

```text
Sender
   │
Message
   │
Transmission Medium
   │
Receiver
   │
Protocol
```

---

## 1. Message

### Definition

The information being communicated.

### Examples

* Text
* Images
* Audio
* Video
* Documents

---

## 2. Sender

### Definition

Device that sends data.

### Examples

* Computer
* Smartphone
* Server

---

## 3. Receiver

### Definition

Device that receives data.

### Examples

* Laptop
* Mobile phone
* Printer

---

## 4. Transmission Medium

### Definition

Path through which data travels.

### Types

#### Guided Media

* Twisted Pair Cable
* Coaxial Cable
* Optical Fiber

#### Unguided Media

* Radio Waves
* Microwaves
* Infrared

---

## 5. Protocol

### Definition

A set of rules governing communication.

### Functions

* Error control
* Flow control
* Addressing
* Synchronization

### Examples

* TCP/IP
* HTTP
* FTP
* SMTP

---

# Quick Table

| Component | Function               |
| --------- | ---------------------- |
| Message   | Information            |
| Sender    | Sends data             |
| Receiver  | Receives data          |
| Medium    | Carries data           |
| Protocol  | Rules of communication |

---

# 1.3 Representation of Data

Computers understand only binary digits (0 and 1).

Therefore all forms of data must be converted into binary.

---

# Text Representation

---

## ASCII

### Full Form

American Standard Code for Information Interchange

### Features

* 7-bit code
* Represents 128 characters

Example:

```text
A = 65
B = 66
```

---

## Unicode

### Need

ASCII cannot represent all world languages.

### Features

* Supports almost all languages.
* Variable-length encoding.

Examples

* English
* Hindi
* Bengali
* Chinese

---

## ASCII vs Unicode

| Feature    | ASCII        | Unicode    |
| ---------- | ------------ | ---------- |
| Bits       | 7            | Variable   |
| Characters | 128          | Millions   |
| Languages  | English only | Almost all |

---

# Number Representation

Numbers are represented using binary digits.

---

## Decimal to Binary Example

25₁₀

```text
25 = 11001₂
```

---

## Types

### Integer Representation

Stores whole numbers.

Examples:

```text
5
100
-10
```

---

### Floating Point Representation

Stores decimal numbers.

Examples:

```text
3.14
5.67
```

---

# Image Representation

Images consist of pixels.

---

## Pixel

Smallest element of an image.

---

### Example

```text
Image
 ┌────────┐
 │■ ■ □ □│
 │□ ■ ■ □│
 └────────┘
```

Each pixel is stored in binary.

---

## Color Representation

Common formats:

* RGB
* CMYK

RGB Example:

```text
Red
Green
Blue
```

---

# Audio Representation

Sound is analog.

Computers convert it into digital form.

---

## Steps

```text
Sound
   ↓
Sampling
   ↓
Quantization
   ↓
Binary Data
```

---

### Examples

* MP3
* WAV
* AAC

---

# Video Representation

Video is a sequence of images called frames.

---

## Structure

```text
Video
 = Frames + Audio
```

Example:

30 FPS

Means:

```text
30 Frames/Second
```

---

### Common Formats

* MP4
* AVI
* MKV

---

# Representation Summary Table

| Data Type | Representation  |
| --------- | --------------- |
| Text      | ASCII, Unicode  |
| Number    | Binary          |
| Image     | Pixels          |
| Audio     | Sampled Signals |
| Video     | Frames + Audio  |

---

# 1.4 Data Flow

Data flow refers to the direction of data transmission.

There are three modes.

---

# 1. Simplex Mode

Communication occurs in only one direction.

---

## Diagram

```text
Sender ─────► Receiver
```

No reverse communication.

---

## Examples

* Television Broadcast
* Radio Broadcast
* Keyboard → Computer

---

## Advantages

* Simple
* Low cost

---

## Disadvantages

* No feedback

---

# 2. Half-Duplex Mode

Communication occurs in both directions but one at a time.

---

## Diagram

```text
Device A ◄────► Device B

(One direction at a time)
```

---

## Examples

* Walkie-Talkie
* CB Radio

---

## Advantages

* Bidirectional communication

---

## Disadvantages

* Waiting time required

---

# 3. Full-Duplex Mode

Communication occurs in both directions simultaneously.

---

## Diagram

```text
Device A ◄════► Device B
```

---

## Examples

* Mobile Phone Calls
* Video Conferencing
* Telephone Network

---

## Advantages

* Fast communication
* No waiting

---

## Disadvantages

* More expensive

---

# Comparison Table (Very Important for Exams)

| Feature                    | Simplex | Half-Duplex   | Full-Duplex |
| -------------------------- | ------- | ------------- | ----------- |
| Direction                  | One-way | Two-way       | Two-way     |
| Simultaneous Communication | No      | No            | Yes         |
| Speed                      | Low     | Medium        | High        |
| Cost                       | Low     | Medium        | High        |
| Example                    | TV      | Walkie-Talkie | Telephone   |

### Memory Trick

👉 S-H-F

Simplex → Send Only

Half Duplex → Both but Hold

Full Duplex → Full Communication

---

# Frequently Asked 2 Marks Questions

### Q1. Define Data Communication.

Exchange of data between devices through a transmission medium.

### Q2. What are the characteristics of effective data communication?

Delivery, Accuracy, Timeliness, Jitter.

### Q3. What is a Protocol?

A set of rules governing communication.

### Q4. What is ASCII?

A 7-bit character encoding standard.

### Q5. Define Pixel.

Smallest unit of a digital image.

---

# Frequently Asked 5 Marks Questions

### Q1. Explain components of data communication.

Explain:

* Message
* Sender
* Receiver
* Medium
* Protocol

---

### Q2. Compare ASCII and Unicode.

Write comparison table.

---

### Q3. Explain image, audio and video representation.

---

### Q4. Explain characteristics of effective data communication.

---

# Frequently Asked 10 Marks Questions

### Q1. Explain Data Communication System with neat diagram.

### Q2. Explain all components of Data Communication in detail.

### Q3. Compare Simplex, Half-Duplex and Full-Duplex communication.

### Q4. Discuss various forms of data representation in computer networks.

---

# Important Viva Questions

### What is data communication?

Transfer of data between devices.

### Why is protocol necessary?

To establish standard communication rules.

### Which coding scheme supports multiple languages?

Unicode.

### What is jitter?

Variation in packet arrival time.

### What is a pixel?

Smallest image element.

---

# MCQs

### 1. Data communication means:

A. Data storage

B. Data processing

C. Exchange of data between devices

D. Data deletion

✅ Answer: C

---

### 2. Which is NOT a component of data communication?

A. Sender

B. Receiver

C. Compiler

D. Protocol

✅ Answer: C

---

### 3. ASCII uses:

A. 5 bits

B. 6 bits

C. 7 bits

D. 16 bits

✅ Answer: C

---

### 4. Unicode was developed to:

A. Reduce memory

B. Support multiple languages

C. Increase CPU speed

D. Improve storage

✅ Answer: B

---

### 5. Smallest image unit is:

A. Byte

B. Pixel

C. Frame

D. Sample

✅ Answer: B

---

### 6. Walkie-Talkie uses:

A. Simplex

B. Half-Duplex

C. Full-Duplex

D. None

✅ Answer: B

---

### 7. Telephone communication uses:

A. Simplex

B. Half-Duplex

C. Full-Duplex

D. Broadcast

✅ Answer: C

---

### 8. Television transmission is:

A. Simplex

B. Half-Duplex

C. Full-Duplex

D. Hybrid

✅ Answer: A

---

# 🚀 One-Page Revision Sheet

### Components

Message, Sender, Receiver, Medium, Protocol

### Characteristics

Delivery, Accuracy, Timeliness, Jitter

### Text Representation

ASCII, Unicode

### Image Representation

Pixels

### Audio Representation

Sampling + Quantization

### Video Representation

Frames + Audio

### Data Flow Modes

Simplex → One Way

Half Duplex → Both Ways One at a Time

Full Duplex → Both Ways Simultaneously

---

# ⭐ Most Important MAKAUT Exam Questions

1. Define Data Communication and explain its characteristics.
2. Explain components of Data Communication.
3. Compare ASCII and Unicode.
4. Explain representation of Text, Image, Audio and Video.
5. Differentiate between Simplex, Half-Duplex and Full-Duplex communication.
6. Explain Protocol and its functions.
7. Draw and explain Data Communication System.
8. Discuss applications of Data Communication.

---

# 📝 Last Minute Revision

Remember:

**DAJT** → Delivery, Accuracy, Jitter, Timeliness

**5 Components** → Message, Sender, Receiver, Medium, Protocol

**ASCII = 128 Characters**

**Unicode = All Languages**

**Image = Pixels**

**Audio = Samples**

**Video = Frames + Audio**

**Simplex → One Way**

**Half Duplex → One at a Time**

**Full Duplex → Simultaneous**

These points alone can help you answer most short and medium questions from Unit 1 in MAKAUT Computer Networks examinations.
