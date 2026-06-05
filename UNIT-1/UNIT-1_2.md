# Computer Networks – Unit 1 Notes

# 2. Computer Networks (MAKAUT Exam-Oriented)

---

# 📖 Topic Overview

A Computer Network is a collection of interconnected devices that communicate and share resources using communication links and protocols.

Computer networks have become the backbone of modern communication systems, enabling Internet access, cloud computing, online banking, social media, e-commerce, and many other services.

---

# 🎯 Learning Objectives

After studying this chapter, you will be able to:

✔ Define Computer Networks.

✔ Explain goals, advantages, and disadvantages of networking.

✔ Differentiate between PAN, LAN, CAN, MAN, WAN, and Internet.

✔ Understand network performance, reliability, and security.

✔ Solve MAKAUT examination questions related to network fundamentals.

---

# 2.1 Introduction to Computer Networks

---

# Definition of Computer Network

### Textbook Definition

A Computer Network is a set of interconnected computers and devices that communicate and share resources through communication channels.

### Simple Definition

When two or more computers are connected to exchange information and resources, they form a computer network.

---

## Basic Network Structure

```text
Computer A
     │
     │
 Network
     │
     │
Computer B
```

---

## Real-Life Examples

* Internet
* College Computer Lab
* Office Network
* ATM Network
* Mobile Network

---

# Goals of Networking

Networking was developed to achieve several important objectives.

---

## 1. Resource Sharing

Users can share:

* Printers
* Files
* Software
* Storage Devices

### Example

Many computers using one printer.

---

## 2. Communication

Allows users to exchange information.

### Examples

* Email
* Video Calls
* Messaging

---

## 3. High Reliability

If one system fails, another system may continue working.

### Example

Cloud Servers

---

## 4. Cost Reduction

Sharing resources reduces hardware costs.

### Example

One printer for an entire office.

---

## 5. Scalability

New devices can easily be added.

### Example

Adding computers in a laboratory.

---

## 6. Centralized Management

Data and resources can be managed from a central location.

---

### Memory Trick

👉 RCHCSC

**R** → Resource Sharing

**C** → Communication

**H** → High Reliability

**C** → Cost Reduction

**S** → Scalability

**C** → Centralized Management

---

# Advantages of Networking

---

## 1. Resource Sharing

Shared access to hardware and software.

---

## 2. Faster Communication

Instant communication across the globe.

---

## 3. Cost Effective

Reduces hardware and maintenance costs.

---

## 4. Centralized Data Management

Easy backup and administration.

---

## 5. Remote Access

Access resources from any location.

---

## 6. Improved Collaboration

Teams can work together efficiently.

---

# Advantages Summary Table

| Advantage              | Benefit             |
| ---------------------- | ------------------- |
| Resource Sharing       | Saves Cost          |
| Communication          | Fast Data Exchange  |
| Centralized Management | Easy Control        |
| Remote Access          | Work Anywhere       |
| Collaboration          | Better Productivity |

---

# Disadvantages of Networking

---

## 1. Security Risks

Hackers may attack the network.

---

## 2. Virus and Malware Spread

Malicious software can spread quickly.

---

## 3. High Initial Cost

Network setup requires investment.

---

## 4. Maintenance Complexity

Requires skilled administrators.

---

## 5. Network Failure

Entire network may stop if major components fail.

---

## 6. Privacy Concerns

Unauthorized access may occur.

---

# Advantages vs Disadvantages

| Advantages           | Disadvantages    |
| -------------------- | ---------------- |
| Resource Sharing     | Security Risks   |
| Faster Communication | Virus Spread     |
| Cost Reduction       | High Setup Cost  |
| Remote Access        | Maintenance Cost |
| Collaboration        | Privacy Issues   |

---

# 2.2 Types of Networks

Networks are classified according to geographical coverage.

---

# Classification Diagram

```text
PAN
 │
LAN
 │
CAN
 │
MAN
 │
WAN
 │
Internet
```

---

# 1. PAN (Personal Area Network)

---

## Definition

A PAN connects devices within a very small area around an individual.

---

## Coverage

Typically 1–10 meters.

---

## Examples

* Bluetooth Headset
* Smart Watch
* Mobile Phone Connection

---

## Diagram

```text
Smart Watch
      │
Bluetooth
      │
Mobile Phone
```

---

## Features

* Small coverage area
* Low cost
* Easy setup

---

# 2. LAN (Local Area Network)

---

## Definition

A LAN connects devices within a limited area such as a room, office, building, or laboratory.

---

## Coverage

Up to a few kilometers.

---

## Examples

* School Lab
* Office Building
* Home Wi-Fi Network

---

## Diagram

```text
PC1 ─┐
PC2 ─┼── Switch ── Server
PC3 ─┘
```

---

## Features

* High speed
* Low error rate
* Private ownership

---

## Advantages

* Fast communication
* Easy management
* Low cost

---

# 3. CAN (Campus Area Network)

---

## Definition

A network that connects multiple LANs within a campus or institution.

---

## Coverage

1–5 kilometers.

---

## Examples

* University Campus
* Research Center
* Corporate Campus

---

## Diagram

```text
LAN1
   │
Campus Backbone
   │
LAN2
   │
LAN3
```

---

## Features

* Larger than LAN
* High-speed communication

---

# 4. MAN (Metropolitan Area Network)

---

## Definition

A network covering an entire city or metropolitan region.

---

## Coverage

Several kilometers to tens of kilometers.

---

## Examples

* City Cable TV Network
* Municipal Network

---

## Diagram

```text
Office A
    │
    │
 MAN Network
    │
    │
Office B
```

---

## Features

* Connects multiple LANs
* High capacity

---

# 5. WAN (Wide Area Network)

---

## Definition

A WAN connects networks over large geographical areas such as countries or continents.

---

## Coverage

Hundreds to thousands of kilometers.

---

## Examples

* Banking Networks
* Railway Reservation System
* International Corporate Networks

---

## Diagram

```text
City A ───── City B ───── City C
```

---

## Features

* Long-distance communication
* Uses leased lines, satellites, fiber optics

---

## Advantages

* Global connectivity
* Large coverage

---

## Disadvantages

* High cost
* Complex management

---

# 6. Internet

---

## Definition

The Internet is the world's largest network of interconnected networks.

### Also Called

"Network of Networks"

---

## Services Provided

* Web Browsing
* Email
* Cloud Computing
* Video Streaming
* Online Gaming

---

## Basic Internet Structure

```text
LAN
 │
ISP
 │
Internet
 │
Server
```

---

## Features

* Global accessibility
* Massive information sharing
* Supports millions of users

---

# Comparison Table (Frequently Asked)

| Feature   | PAN        | LAN       | CAN         | MAN          | WAN           |
| --------- | ---------- | --------- | ----------- | ------------ | ------------- |
| Coverage  | Few meters | Building  | Campus      | City         | Country/World |
| Ownership | Personal   | Private   | Institution | Organization | Multiple      |
| Speed     | High       | Very High | High        | Medium       | Lower         |
| Cost      | Low        | Low       | Medium      | High         | Very High     |
| Example   | Bluetooth  | Office    | University  | City Network | Internet      |

---

### Memory Trick

👉 P-L-C-M-W

Personal → Local → Campus → Metropolitan → Wide

(Small → Large Coverage)

---

# 2.3 Network Criteria

For a network to be effective, it must satisfy three important criteria.

---

# 1. Performance

---

## Definition

Performance measures how efficiently a network transfers data.

---

## Factors Affecting Performance

### Number of Users

More users → Lower performance

---

### Transmission Medium

Fiber optic is faster than copper cable.

---

### Hardware Quality

Better routers and switches improve performance.

---

### Software Efficiency

Efficient protocols increase speed.

---

## Performance Metrics

### Throughput

Actual amount of data transferred.

### Bandwidth

Maximum data carrying capacity.

### Delay

Time taken for data transfer.

### Response Time

Time between request and response.

---

# 2. Reliability

---

## Definition

Reliability indicates how dependable a network is.

---

## Factors Affecting Reliability

### Frequency of Failure

Less failure = More reliable

---

### Recovery Time

Quick recovery improves reliability.

---

### Robustness

Ability to continue functioning during faults.

---

## Example

Banking networks require extremely high reliability.

---

# 3. Security

---

## Definition

Security protects data and resources from unauthorized access.

---

## Security Goals

### Confidentiality

Only authorized users can access data.

---

### Integrity

Data should not be altered.

---

### Availability

Resources should remain accessible.

---

### Authentication

Verify user identity.

---

### Authorization

Determine user permissions.

---

# Security Threats

* Hacking
* Malware
* Phishing
* Data Theft
* Denial of Service Attacks

---

# CIA Triad (Very Important)

```text
Confidentiality
      ▲
      │
Integrity ─ Availability
```

### Memory Trick

👉 CIA

C → Confidentiality

I → Integrity

A → Availability

---

# Frequently Asked 2 Marks Questions

### Q1. Define Computer Network.

A collection of interconnected devices that communicate and share resources.

---

### Q2. What is LAN?

A network connecting devices within a limited geographical area.

---

### Q3. What is PAN?

A network connecting personal devices within a few meters.

---

### Q4. What is WAN?

A network covering large geographical areas.

---

### Q5. What are the network criteria?

Performance, Reliability, Security.

---

# Frequently Asked 5 Marks Questions

### Q1. Explain goals of networking.

### Q2. Discuss advantages and disadvantages of networking.

### Q3. Explain PAN, LAN and CAN.

### Q4. Explain network performance and reliability.

### Q5. Explain the Internet.

---

# Frequently Asked 10 Marks Questions

### Q1. Explain different types of computer networks with examples.

### Q2. Compare PAN, LAN, CAN, MAN and WAN.

### Q3. Discuss network criteria in detail.

### Q4. Explain advantages and disadvantages of networking.

---

# Viva Questions

### What is networking?

Connecting devices for communication and resource sharing.

### Which network covers a city?

MAN.

### Which network covers the largest area?

WAN.

### What is the Internet?

A global network of interconnected networks.

### What are the three network criteria?

Performance, Reliability, Security.

---

# Important MCQs

### 1. A collection of interconnected computers is called:

A. Protocol

B. Network

C. Server

D. Router

✅ Answer: B

---

### 2. Bluetooth is an example of:

A. LAN

B. MAN

C. PAN

D. WAN

✅ Answer: C

---

### 3. A university campus network is:

A. PAN

B. LAN

C. CAN

D. WAN

✅ Answer: C

---

### 4. A city-wide network is:

A. LAN

B. PAN

C. MAN

D. WAN

✅ Answer: C

---

### 5. Internet is a:

A. LAN

B. MAN

C. WAN

D. Network of Networks

✅ Answer: D

---

### 6. Which criterion measures network efficiency?

A. Reliability

B. Security

C. Performance

D. Authentication

✅ Answer: C

---

### 7. CIA stands for:

A. Confidentiality, Integrity, Availability

B. Control, Integrity, Access

C. Communication, Internet, Availability

D. None

✅ Answer: A

---

# 🚀 One-Page Revision Sheet

### Goals of Networking

* Resource Sharing
* Communication
* Reliability
* Cost Reduction
* Scalability

---

### Types of Networks

PAN → Personal

LAN → Building

CAN → Campus

MAN → City

WAN → Country/World

Internet → Network of Networks

---

### Network Criteria

Performance

Reliability

Security

---

### Security Goals

CIA

Confidentiality

Integrity

Availability

---

# ⭐ Most Important MAKAUT Questions

1. Define Computer Network and explain its goals.
2. Explain advantages and disadvantages of networking.
3. Differentiate PAN, LAN, CAN, MAN and WAN.
4. Explain Internet with diagram.
5. Discuss Network Criteria.
6. Explain Performance, Reliability and Security.
7. Compare different network types.
8. Explain CIA triad.
9. What are the factors affecting network performance?
10. Discuss security requirements of a network.

---

# 📝 Last-Minute Revision

### Remember

**RCHCSC**
→ Resource Sharing, Communication, High Reliability, Cost Reduction, Scalability, Centralized Management

**P-L-C-M-W**
→ PAN → LAN → CAN → MAN → WAN

**CIA**
→ Confidentiality → Integrity → Availability

**Most Important Long Questions**

* Types of Networks
* Network Criteria
* Advantages & Disadvantages of Networking
* Internet and Goals of Networking

These topics are among the most frequently asked in MAKAUT Computer Networks Unit-1 examinations.
