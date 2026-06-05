# Computer Networks – Unit 1 Notes

# 3. Network Topology (MAKAUT Exam-Oriented Notes)

---

# 📖 Topic Overview

Network Topology refers to the arrangement of computers, cables, network devices, and communication links in a computer network.

It defines how devices are connected and how data flows between them.

Understanding network topology is important because it affects:

* Network performance
* Reliability
* Scalability
* Cost
* Fault tolerance

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

✔ Define Network Topology.

✔ Differentiate between Physical and Logical Topology.

✔ Explain Bus, Star, Ring, Mesh, Tree, and Hybrid Topologies.

✔ Compare different topologies.

✔ Answer MAKAUT theory, numerical, and viva questions.

---

# 3.1 Physical Topology

---

## Definition

Physical Topology refers to the actual physical arrangement of devices, cables, and network components in a network.

It describes how devices are physically connected.

---

## Simple Explanation

Physical topology shows:

👉 Where devices are placed

👉 How cables connect devices

👉 Actual network structure

---

## Example

```text
Computer A ----- Computer B ----- Computer C
```

This shows the physical connection between devices.

---

## Characteristics

* Concerned with hardware layout.
* Easy to visualize.
* Determines installation cost.
* Affects maintenance.

---

## Real-Life Example

An office network where all computers are connected to a central switch.

---

# 3.2 Logical Topology

---

## Definition

Logical Topology describes how data flows between devices regardless of physical connections.

---

## Simple Explanation

It shows:

👉 How communication occurs

👉 Data transmission path

👉 Network behavior

---

## Example

Physically a network may be Star, but logically data may flow like a Bus.

---

## Characteristics

* Concerned with data movement.
* Independent of physical arrangement.
* Controlled by protocols.

---

# Physical vs Logical Topology

| Feature    | Physical Topology    | Logical Topology   |
| ---------- | -------------------- | ------------------ |
| Focus      | Hardware Arrangement | Data Flow          |
| Concern    | Cables & Devices     | Communication Path |
| Visibility | Physical Layout      | Logical Behavior   |
| Example    | Star Cabling         | Bus Communication  |

---

# 3.3 Types of Topology

---

# Classification

```text
Network Topology
        │
 ┌──────┼──────┐
 │      │      │
Bus   Star   Ring
 │      │      │
Mesh  Tree Hybrid
```

---

# 1. Bus Topology

---

## Definition

In Bus Topology, all devices are connected to a single communication cable called the backbone cable.

---

## Structure

```text
PC1 ──┬────┬────┬──── PC4
       │    │
      PC2  PC3

Backbone Cable
```

---

## Working

* Data is transmitted through the backbone.
* All devices receive the signal.
* Intended receiver accepts the data.
* Others ignore it.

---

## Components

### Backbone Cable

Main communication line.

### Terminators

Placed at both ends to absorb signals and prevent reflection.

---

## Advantages

✅ Easy installation

✅ Low cost

✅ Requires less cable

✅ Suitable for small networks

---

## Disadvantages

❌ Backbone failure affects entire network

❌ Difficult fault detection

❌ Limited length

❌ Performance decreases with traffic

---

## Applications

* Small office networks
* Temporary networks

---

## Exam Tip

**Frequently Asked Question:**
"Draw and explain Bus Topology with advantages and disadvantages."

---

# 2. Star Topology

---

## Definition

All devices are connected to a central hub or switch.

---

## Structure

```text
         PC1
          │
          │
PC2 ── Switch ── PC3
          │
          │
         PC4
```

---

## Working

* Data is sent to the switch.
* Switch forwards data to the destination device.

---

## Advantages

✅ Easy installation

✅ Easy maintenance

✅ Fault isolation is simple

✅ High performance

✅ Easy expansion

---

## Disadvantages

❌ Central switch failure stops network

❌ More cable required

❌ Higher installation cost

---

## Applications

* Modern LANs
* Schools
* Offices
* Computer Labs

---

## Real-Life Example

Most Wi-Fi networks use Star topology.

---

# 3. Ring Topology

---

## Definition

Each device is connected to exactly two neighboring devices, forming a circular path.

---

## Structure

```text
      PC1
    /     \
  PC2     PC4
    \     /
      PC3
```

---

## Working

Data travels around the ring.

Often uses a token passing mechanism.

---

## Token Passing

Only the device holding the token can transmit data.

---

## Advantages

✅ No data collision

✅ Equal network access

✅ Better performance under heavy load

---

## Disadvantages

❌ Single node failure may stop network

❌ Difficult troubleshooting

❌ Expansion is difficult

---

## Applications

* Token Ring Networks
* Industrial Networks

---

# 4. Mesh Topology

---

## Definition

Every device is connected to every other device.

---

## Structure

```text
 PC1────PC2
  │ \  / │
  │  \/  │
  │  /\  │
  │ /  \ │
 PC3────PC4
```

---

## Formula for Number of Links

For n nodes:

\frac{n(n-1)}{2}

---

### Example

For 5 nodes:

Links = 5 × 4 / 2 = 10

---

## Advantages

✅ Highly reliable

✅ Fault tolerant

✅ High security

✅ Multiple communication paths

---

## Disadvantages

❌ Expensive

❌ Complex installation

❌ Large amount of cabling

---

## Applications

* Internet backbone
* Military networks
* Banking systems

---

## Exam Tip

The formula for number of links is frequently asked in MAKAUT exams.

---

# 5. Tree Topology

---

## Definition

Tree topology combines characteristics of Bus and Star topologies.

---

## Structure

```text
           Root
             │
      ┌──────┴──────┐
      │             │
   Switch1      Switch2
      │             │
    PCs          PCs
```

---

## Working

Data flows hierarchically from root to branches.

---

## Advantages

✅ Easy expansion

✅ Hierarchical management

✅ Suitable for large organizations

---

## Disadvantages

❌ Backbone failure affects branches

❌ Complex cabling

❌ Costly

---

## Applications

* Universities
* Corporate Networks
* Government Organizations

---

# 6. Hybrid Topology

---

## Definition

Combination of two or more topologies.

---

## Example

Star + Bus

Star + Ring

---

## Structure

```text
Star Network
      │
      │
Bus Backbone
      │
      │
Star Network
```

---

## Advantages

✅ Flexible

✅ Scalable

✅ Reliable

✅ Customizable

---

## Disadvantages

❌ Expensive

❌ Complex design

❌ Maintenance difficulty

---

## Applications

* Large Enterprises
* Data Centers
* Modern Networks

---

# 3.4 Comparison of Topologies

---

# Comprehensive Comparison Table

| Feature           | Bus       | Star      | Ring      | Mesh      | Tree     | Hybrid    |
| ----------------- | --------- | --------- | --------- | --------- | -------- | --------- |
| Cost              | Low       | Medium    | Medium    | Very High | High     | High      |
| Installation      | Easy      | Easy      | Moderate  | Difficult | Moderate | Difficult |
| Reliability       | Low       | High      | Medium    | Very High | High     | High      |
| Expansion         | Difficult | Easy      | Difficult | Difficult | Easy     | Easy      |
| Maintenance       | Difficult | Easy      | Difficult | Difficult | Moderate | Moderate  |
| Fault Isolation   | Poor      | Excellent | Moderate  | Excellent | Good     | Good      |
| Cable Requirement | Low       | High      | Medium    | Very High | High     | High      |
| Performance       | Medium    | High      | High      | Very High | High     | High      |

---

# Which Topology is Best?

| Requirement         | Best Topology |
| ------------------- | ------------- |
| Lowest Cost         | Bus           |
| Easy Maintenance    | Star          |
| Highest Reliability | Mesh          |
| Large Organization  | Tree          |
| Flexible Design     | Hybrid        |
| Modern LAN          | Star          |

---

# Memory Tricks

## Types of Topology

👉 **BSRMTH**

B → Bus

S → Star

R → Ring

M → Mesh

T → Tree

H → Hybrid

---

## Best Feature Trick

Bus → Budget

Star → Simple

Ring → Rotation

Mesh → Maximum Reliability

Tree → Hierarchy

Hybrid → Mix

---

# Frequently Asked 2 Marks Questions

### Q1. What is Network Topology?

Arrangement of devices and communication links in a network.

---

### Q2. Define Physical Topology.

Physical arrangement of devices and cables.

---

### Q3. Define Logical Topology.

Pattern of data flow in a network.

---

### Q4. What is a Backbone Cable?

Main communication cable in Bus topology.

---

### Q5. What is Token Passing?

A method where only the token holder can transmit data.

---

# Frequently Asked 5 Marks Questions

### Q1. Explain Physical and Logical Topology.

### Q2. Explain Bus Topology with diagram.

### Q3. Explain Star Topology with advantages and disadvantages.

### Q4. Explain Ring Topology.

### Q5. Explain Mesh Topology.

---

# Frequently Asked 10 Marks Questions

### Q1. Compare all network topologies.

### Q2. Explain Bus, Star and Ring Topologies with diagrams.

### Q3. Explain Mesh, Tree and Hybrid Topologies.

### Q4. Discuss advantages and disadvantages of various topologies.

### Q5. Differentiate Physical and Logical Topology.

---

# Viva Questions

### Which topology uses a backbone cable?

Bus Topology.

### Which topology uses a central switch?

Star Topology.

### Which topology uses token passing?

Ring Topology.

### Which topology provides maximum reliability?

Mesh Topology.

### Which topology is commonly used in LAN?

Star Topology.

### Which topology combines multiple topologies?

Hybrid Topology.

---

# Important MCQs

### 1. Which topology uses a single backbone cable?

A. Star

B. Ring

C. Bus

D. Mesh

✅ Answer: C

---

### 2. Which topology uses a central hub or switch?

A. Bus

B. Ring

C. Star

D. Tree

✅ Answer: C

---

### 3. Which topology provides highest fault tolerance?

A. Bus

B. Ring

C. Mesh

D. Star

✅ Answer: C

---

### 4. Which topology uses token passing?

A. Bus

B. Ring

C. Mesh

D. Tree

✅ Answer: B

---

### 5. Which topology is most commonly used in modern LANs?

A. Bus

B. Ring

C. Star

D. Mesh

✅ Answer: C

---

### 6. Which topology is hierarchical?

A. Tree

B. Bus

C. Ring

D. Mesh

✅ Answer: A

---

### 7. Hybrid topology is:

A. Single topology

B. Combination of topologies

C. Wireless topology

D. Internet topology

✅ Answer: B

---

# 🚀 One-Page Revision Sheet

### Physical Topology

Actual arrangement of devices.

### Logical Topology

Data flow arrangement.

### Bus

Single backbone cable.

### Star

Central switch/hub.

### Ring

Circular connection.

### Mesh

Every node connected to every node.

### Tree

Hierarchical structure.

### Hybrid

Combination of topologies.

---

# ⭐ Most Important MAKAUT Questions

1. Define Network Topology.
2. Differentiate Physical and Logical Topology.
3. Explain Bus Topology with diagram.
4. Explain Star Topology with diagram.
5. Explain Ring Topology and token passing.
6. Explain Mesh Topology and derive link formula.
7. Explain Tree and Hybrid Topologies.
8. Compare all topologies.
9. Advantages and disadvantages of different topologies.
10. Which topology is best for LAN and why?

---

# 📝 Last-Minute Revision

Remember:

**BSRMTH**
→ Bus, Star, Ring, Mesh, Tree, Hybrid

**Bus**
→ Cheapest, Backbone Cable

**Star**
→ Most Popular LAN Topology

**Ring**
→ Token Passing

**Mesh**
→ Highest Reliability

**Tree**
→ Hierarchical Network

**Hybrid**
→ Combination of Topologies

**Most Important Exam Topics**

* Star vs Bus Topology
* Mesh Topology Formula
* Comparison Table of Topologies
* Physical vs Logical Topology
* Advantages and Disadvantages of Each Topology

These are among the most frequently repeated MAKAUT Computer Networks Unit-1 examination questions.
