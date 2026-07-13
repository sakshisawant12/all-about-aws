# Chapter 5 – Subnetting

---

# 📚 Table of Contents

1. What is Subnetting?
2. Why Do We Need Subnetting?
3. Subnet Mask
4. CIDR-Based Subnetting
5. Network Address
6. Broadcast Address
7. First & Last Usable Host
8. How to Calculate Subnets
9. How to Calculate Hosts
10. VLSM (Variable Length Subnet Mask)
11. AWS Subnet Design
12. AWS Reserved IP Addresses
13. Best Practices
14. Chapter Summary & Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Understand the concept of subnetting.
- Learn why subnetting is required.
- Create subnets using CIDR notation.
- Calculate Network and Broadcast addresses.
- Calculate usable host addresses.
- Design AWS VPC subnets.
- Understand AWS subnetting best practices.
- Answer subnetting interview questions confidently.

---

# 1. What is Subnetting?

---

## 📖 Introduction

Imagine a company has one large office with **500 employees**.

If all 500 employees are placed in a single room:

- Communication becomes difficult.
- Too much noise.
- Hard to manage.
- Low security.

Instead, the company divides the office into different departments such as:

- HR
- Finance
- IT
- Sales

Each department has its own room, making communication more organized and secure.

Computer networks work in the same way.

Instead of keeping one large network, we divide it into smaller networks called **subnets**.

This process is known as **Subnetting**.

---

# What is Subnetting?

**Subnetting** is the process of dividing a large network into multiple smaller logical networks called **subnets**.

Each subnet has its own range of IP addresses and can communicate efficiently within the network.

---

## 💼 Simple Definition (Interview Answer)

> **Subnetting is the process of dividing a large IP network into smaller logical networks (subnets) to improve performance, security, and IP address management.**

---

# Understanding with an Example

Suppose we have the following network:

```text
192.168.1.0/24
```

This network contains:

```text
256 IP Addresses
```

Instead of using one large network, we can divide it into four smaller subnets.

```text
192.168.1.0/26

192.168.1.64/26

192.168.1.128/26

192.168.1.192/26
```

Each subnet now has its own IP address range.

---

# Visual Representation

Without Subnetting:

```text
192.168.1.0/24

──────────────────────────────

One Large Network
```

With Subnetting:

```text
192.168.1.0/26

──────────────

HR Department

──────────────────────────────

192.168.1.64/26

──────────────

Finance Department

──────────────────────────────

192.168.1.128/26

──────────────

IT Department

──────────────────────────────

192.168.1.192/26

──────────────

Sales Department
```

Each subnet works independently while still being part of the larger network.

---

# Why is Subnetting Important?

Subnetting helps to:

- Organize large networks.
- Improve network performance.
- Reduce unnecessary network traffic.
- Increase security.
- Manage IP addresses efficiently.
- Simplify troubleshooting.

---

# Real-Life Analogy

Imagine a library.

Without sections:

```text
All Books

↓

One Huge Room
```

Finding a book becomes difficult.

With sections:

```text
Science

History

Technology

Arts
```

Books become easier to organize and locate.

Subnetting organizes networks in the same way.

---

# Real AWS Example

Suppose you create a VPC:

```text
10.0.0.0/16
```

Instead of placing everything in one subnet, you divide it into:

```text
Public Subnet

10.0.1.0/24
```

```text
Private Application Subnet

10.0.2.0/24
```

```text
Private Database Subnet

10.0.3.0/24
```

Each subnet has its own purpose and security rules.

---

# AWS Perspective ☁️

Subnetting is a fundamental part of Amazon VPC.

Every VPC is divided into one or more subnets.

Example:

```text
Amazon VPC

10.0.0.0/16

│

├── Public Subnet

│      10.0.1.0/24

│

├── Private App Subnet

│      10.0.2.0/24

│

└── Private Database Subnet

       10.0.3.0/24
```

Benefits in AWS:

- Better Security
- Easier Resource Management
- High Availability
- Network Isolation
- Scalability

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Subnetting creates new IP addresses."**

✅ **Correct:**

Subnetting does not create new IP addresses.

It divides an existing network into smaller logical networks.

---

## ❌ Mistake 2

**"Every subnet can communicate directly with every other subnet."**

✅ **Correct:**

Communication between subnets depends on routing rules and security configurations.

---

## ❌ Mistake 3

**"Subnetting is only used in AWS."**

✅ **Correct:**

Subnetting is a standard networking concept used in enterprise networks, data centers, cloud environments, and AWS.

---

# 📝 Quick Revision

- Subnetting divides one large network into smaller networks.
- Smaller networks are called subnets.
- Improves performance and security.
- Makes IP address management easier.
- Every AWS VPC uses subnetting.

---

# 💼 Interview Questions

### 1. What is Subnetting?

**Answer:**

Subnetting is the process of dividing a large IP network into smaller logical networks called subnets.

---

### 2. Why is Subnetting used?

**Answer:**

Subnetting improves network performance, security, IP address management, and scalability.

---

### 3. Does subnetting create new IP addresses?

**Answer:**

No. It divides an existing IP address range into smaller subnetworks.

---

### 4. Where is subnetting used in AWS?

**Answer:**

Subnetting is used in Amazon VPC to create Public, Private, and Database subnets.

---

### 5. Can different subnets communicate with each other?

**Answer:**

Yes, provided routing rules and security settings allow the communication.


# 2. Why Do We Need Subnetting?

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand why subnetting is necessary.
- Learn the problems of a large network.
- Understand how subnetting improves performance.
- Learn how subnetting increases security.
- Understand subnetting in AWS VPC design.
- Answer interview questions confidently.

---

# 📖 Introduction

Imagine a company has **1,000 computers** connected to a single network.

Whenever one computer sends a broadcast message, **all 1,000 computers** receive it.

This results in:

- Increased network traffic
- Slower communication
- Reduced performance
- Difficult troubleshooting
- Lower security

Instead of using one large network, it is better to divide it into smaller networks called **subnets**.

This process is known as **Subnetting**.

---

# Why Do We Need Subnetting?

Subnetting is required to make networks:

- Faster
- More secure
- Easier to manage
- More efficient
- More scalable

Instead of managing one huge network, administrators manage several smaller networks.

---

# Problem Without Subnetting

Suppose a company has:

```text
192.168.1.0/24
```

All employees are connected to this single network.

```text
PC1

PC2

PC3

...

PC200
```

If one device sends a broadcast packet,

every device receives it.

This increases unnecessary traffic.

---

# Solution Using Subnetting

Instead of one large network,

divide it into smaller subnets.

```text
HR

192.168.1.0/26
```

```text
Finance

192.168.1.64/26
```

```text
IT

192.168.1.128/26
```

```text
Sales

192.168.1.192/26
```

Now,

broadcast traffic remains inside each subnet.

This improves overall network performance.

---

# Benefits of Subnetting

---

## 1. Better Network Performance

Smaller subnets generate less broadcast traffic.

Example:

Without subnetting:

```text
500 Devices

↓

One Broadcast

↓

500 Devices Receive It
```

With subnetting:

```text
125 Devices

↓

One Broadcast

↓

Only 125 Devices Receive It
```

Result:

- Faster communication
- Less unnecessary traffic
- Better performance

---

## 2. Improved Security

Subnetting allows sensitive systems to be isolated.

Example:

```text
Public Web Servers

↓

Public Subnet
```

```text
Database Servers

↓

Private Subnet
```

Even if the Public Subnet is attacked,

the Database Subnet remains isolated and protected.

---

## 3. Better IP Address Management

Instead of wasting IP addresses,

you allocate only the number required.

Example:

HR Department:

```text
50 Employees

↓

/26 Subnet
```

Finance Department:

```text
20 Employees

↓

/27 Subnet
```

This makes efficient use of available IP addresses.

---

## 4. Easier Troubleshooting

Smaller networks make it easier to identify and resolve issues.

Instead of checking hundreds of devices,

you troubleshoot only the affected subnet.

---

## 5. Scalability

As the organization grows,

new subnets can be created without redesigning the entire network.

Example:

```text
Current

HR

Finance

IT
```

Future:

```text
HR

Finance

IT

Marketing

Research
```

New departments can receive their own subnet.

---

# Real-Life Analogy

Imagine a shopping mall.

Without sections:

```text
All Shops

↓

One Large Hall
```

Finding a shop becomes difficult.

With sections:

```text
Food Court

Electronics

Clothing

Books
```

The mall becomes easier to navigate.

Subnetting organizes networks in the same way.

---

# AWS Perspective ☁️

AWS heavily relies on subnetting.

Example:

```text
Amazon VPC

10.0.0.0/16
```

Subnets:

```text
Public Subnet

10.0.1.0/24
```

```text
Private App Subnet

10.0.2.0/24
```

```text
Private Database Subnet

10.0.3.0/24
```

Each subnet serves a different purpose.

---

# AWS Production Architecture

```text
Internet

↓

Internet Gateway

↓

Public Subnet

↓

Application Load Balancer

↓

Private Application Subnet

↓

EC2 Instances

↓

Private Database Subnet

↓

Amazon RDS
```

Benefits:

- Better Security
- Easier Scaling
- High Availability
- Improved Performance

---

# Broadcast Domain

One of the main reasons for subnetting is to reduce the size of a **broadcast domain**.

A **broadcast domain** is a group of devices that receive the same broadcast message.

Without subnetting:

```text
500 Devices

↓

One Broadcast Domain
```

With subnetting:

```text
Subnet A

125 Devices
```

```text
Subnet B

125 Devices
```

```text
Subnet C

125 Devices
```

```text
Subnet D

125 Devices
```

Now each subnet has its own smaller broadcast domain.

This reduces unnecessary traffic.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Subnetting increases the total number of IP addresses."**

✅ **Correct:**

Subnetting divides an existing IP address range. It does not create additional IP addresses.

---

## ❌ Mistake 2

**"Subnetting is only for security."**

✅ **Correct:**

Subnetting improves performance, security, scalability, IP management, and troubleshooting.

---

## ❌ Mistake 3

**"All AWS resources should be placed in one subnet."**

✅ **Correct:**

Production AWS environments use multiple subnets for better availability, security, and organization.

---

# 📝 Quick Revision

- Subnetting divides large networks into smaller networks.
- Reduces broadcast traffic.
- Improves network performance.
- Enhances security through isolation.
- Simplifies troubleshooting.
- Makes better use of IP addresses.
- AWS VPCs are designed using multiple subnets.

---

# 💼 Interview Questions

### 1. Why do we need subnetting?

**Answer:**

Subnetting improves network performance, security, scalability, IP address management, and troubleshooting by dividing a large network into smaller logical networks.

---

### 2. How does subnetting improve performance?

**Answer:**

Subnetting reduces the size of broadcast domains, which decreases unnecessary network traffic.

---

### 3. How does subnetting improve security?

**Answer:**

Subnetting isolates different parts of the network, allowing sensitive resources such as databases to be placed in private subnets.

---

### 4. Why are multiple subnets used in AWS?

**Answer:**

AWS uses multiple subnets to separate public and private resources, improve security, enable high availability, and simplify network management.

---

### 5. What is a broadcast domain?

**Answer:**

A broadcast domain is a group of devices that receive the same broadcast message. Subnetting reduces the size of broadcast domains to improve network efficiency.


# 3. Subnet Mask

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand what a Subnet Mask is.
- Learn how a Subnet Mask works.
- Understand the relationship between Subnet Masks and CIDR notation.
- Identify the Network and Host portions of an IP Address.
- Learn default subnet masks.
- Understand how AWS uses subnet masks.
- Answer subnet mask interview questions confidently.

---

# 📖 Introduction

Imagine you have an IP Address:

```text
192.168.1.25
```

How does a computer know:

- Which part identifies the **Network**?
- Which part identifies the **Host**?

The answer is:

> **Subnet Mask**

A Subnet Mask tells a device which bits belong to the **Network** and which bits belong to the **Host**.

Without a Subnet Mask, a device cannot determine whether another device is on the same network or on a different network.

---

# What is a Subnet Mask?

A **Subnet Mask** is a 32-bit number used to separate the **Network Portion** and the **Host Portion** of an IPv4 address.

---

## 💼 Simple Definition (Interview Answer)

> **A Subnet Mask is a 32-bit value that identifies the Network ID and Host ID of an IP address.**

---

# Why Do We Need a Subnet Mask?

A Subnet Mask helps devices determine:

- Which network they belong to.
- Whether the destination device is on the same network.
- Whether the packet should be sent directly or forwarded to a router.

Without a Subnet Mask, routing would not work correctly.

---

# Example

IP Address:

```text
192.168.1.25
```

Subnet Mask:

```text
255.255.255.0
```

This tells us:

```text
192.168.1

↓

Network
```

```text
25

↓

Host
```

---

# How Does a Subnet Mask Work?

A Subnet Mask uses binary values.

- **1** = Network Bit
- **0** = Host Bit

Example:

```text
255.255.255.0
```

Binary:

```text
11111111.11111111.11111111.00000000
```

Visualization:

```text
11111111.11111111.11111111.00000000

^^^^^^^^^^^^^^^^^^^^^^^^
      Network Bits

                         ^^^^^^^^
                         Host Bits
```

The first **24 bits** identify the network.

The last **8 bits** identify individual hosts.

---

# Common Subnet Masks

| CIDR | Subnet Mask |
|------|-------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |
| /30 | 255.255.255.252 |
| /32 | 255.255.255.255 |

---

# Default Subnet Masks

In Classful Networking, each class had a default subnet mask.

| Class | Default Subnet Mask | CIDR |
|--------|---------------------|------|
| Class A | 255.0.0.0 | /8 |
| Class B | 255.255.0.0 | /16 |
| Class C | 255.255.255.0 | /24 |

Today, modern networks—including AWS—primarily use CIDR instead of default class-based subnet masks.

---

# Subnet Mask vs CIDR

These represent the same information in different formats.

| CIDR | Subnet Mask |
|------|-------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /28 | 255.255.255.240 |
| /32 | 255.255.255.255 |

Example:

```text
192.168.1.0/24
```

is exactly the same as:

```text
IP Address

192.168.1.0

Subnet Mask

255.255.255.0
```

---

# Real-Life Analogy

Imagine an apartment building.

```text
Building Number

↓

Network
```

```text
Apartment Number

↓

Host
```

The Subnet Mask tells us where the **Building Number** ends and where the **Apartment Number** begins.

Without it, the courier would not know which part represents the building and which part represents the apartment.

---

# AWS Perspective ☁️

AWS uses **CIDR notation**, but the concept is exactly the same as using subnet masks.

Example:

When creating a subnet:

```text
10.0.1.0/24
```

AWS interprets it as:

```text
Subnet Mask

255.255.255.0
```

This subnet can contain:

```text
256 Total IP Addresses
```

AWS automatically calculates:

- Network Address
- Available Host Addresses
- Reserved Addresses

---

# Real AWS Example

VPC:

```text
10.0.0.0/16
```

Subnet:

```text
10.0.1.0/24
```

Network Portion:

```text
10.0.1
```

Host Portion:

```text
0–255
```

EC2 Instance:

```text
10.0.1.25
```

AWS identifies:

```text
Network

↓

10.0.1.0
```

Host:

```text
25
```

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Subnet Mask creates new IP addresses."**

✅ **Correct:**

A Subnet Mask only divides an IP address into Network and Host portions.

---

## ❌ Mistake 2

**"CIDR and Subnet Mask are different technologies."**

✅ **Correct:**

CIDR and Subnet Masks represent the same network information using different formats.

---

## ❌ Mistake 3

**"AWS requires you to enter both CIDR and Subnet Mask."**

✅ **Correct:**

AWS uses **CIDR notation**. The subnet mask is calculated automatically.

---

# 📝 Quick Revision

- A Subnet Mask is a 32-bit value.
- It separates the Network ID and Host ID.
- Binary **1** represents Network bits.
- Binary **0** represents Host bits.
- `/24` = `255.255.255.0`
- AWS primarily uses CIDR notation instead of manually entering subnet masks.

---

# 💼 Interview Questions

### 1. What is a Subnet Mask?

**Answer:**

A Subnet Mask is a 32-bit value that separates the Network portion and Host portion of an IP address.

---

### 2. Why is a Subnet Mask required?

**Answer:**

It helps devices identify the network they belong to and determine whether a destination is local or requires routing.

---

### 3. What is the subnet mask for `/24`?

**Answer:**

255.255.255.0

---

### 4. What do the binary 1s and 0s represent in a subnet mask?

**Answer:**

- **1s** represent the Network portion.
- **0s** represent the Host portion.

---

### 5. Does AWS use subnet masks directly?

**Answer:**

No. AWS uses CIDR notation, but the subnet mask is derived automatically from the CIDR prefix.

# 4. CIDR-Based Subnetting

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand how subnetting works using CIDR.
- Divide a network into smaller subnets.
- Calculate Network Address, Broadcast Address, and Host Range.
- Learn common subnet sizes used in AWS.
- Design AWS subnets using CIDR notation.
- Answer subnetting interview questions confidently.

---

# 📖 Introduction

In the previous topic, we learned that **CIDR notation** defines the size of a network.

Now we'll learn how to use CIDR to **split one large network into multiple smaller subnets.**

This process is called **CIDR-Based Subnetting**.

---

# What is CIDR-Based Subnetting?

CIDR-Based Subnetting is the process of dividing a larger network into smaller networks by **borrowing bits from the Host portion** of the IP address.

Every time we increase the CIDR prefix:

- The number of subnets increases.
- The number of available host addresses decreases.

---

## 💼 Simple Definition (Interview Answer)

> CIDR-Based Subnetting is the process of creating multiple smaller subnets by increasing the CIDR prefix and borrowing bits from the Host portion.

---

# Understanding with an Example

Suppose we have:

```text
192.168.1.0/24
```

A `/24` network contains:

```text
256 Total IP Addresses
```

Now suppose we want **2 subnets**.

We increase the prefix from:

```text
/24

↓

/25
```

The network is divided into two equal parts.

---

# Example 1 – /24 to /25

Original Network

```text
192.168.1.0/24
```

After subnetting

### Subnet 1

Network Address

```text
192.168.1.0/25
```

Host Range

```text
192.168.1.1

↓

192.168.1.126
```

Broadcast Address

```text
192.168.1.127
```

---

### Subnet 2

Network Address

```text
192.168.1.128/25
```

Host Range

```text
192.168.1.129

↓

192.168.1.254
```

Broadcast Address

```text
192.168.1.255
```

---

# Visual Representation

```text
192.168.1.0/24

↓

Split into Two Networks

↓

192.168.1.0/25

192.168.1.128/25
```

---

# Example 2 – /24 to /26

Increase the prefix again.

```text
/24

↓

/26
```

Now the network becomes **4 equal subnets**.

| Subnet | Network Address | Broadcast Address |
|---------|-----------------|-------------------|
| 1 | 192.168.1.0/26 | 192.168.1.63 |
| 2 | 192.168.1.64/26 | 192.168.1.127 |
| 3 | 192.168.1.128/26 | 192.168.1.191 |
| 4 | 192.168.1.192/26 | 192.168.1.255 |

Each subnet contains:

```text
64 Total IP Addresses

62 Usable Hosts
```

---

# Example 3 – /24 to /27

```text
/24

↓

/27
```

Now we get:

```text
8 Subnets
```

Subnet increment:

```text
32
```

Network Addresses

```text
192.168.1.0

192.168.1.32

192.168.1.64

192.168.1.96

192.168.1.128

192.168.1.160

192.168.1.192

192.168.1.224
```

Each subnet contains:

```text
32 Total IP Addresses

30 Usable Hosts
```

---

# Example 4 – /24 to /28

```text
/24

↓

/28
```

Now we get:

```text
16 Subnets
```

Subnet increment:

```text
16
```

Each subnet contains:

```text
16 Total IP Addresses

14 Usable Hosts

11 Usable in AWS
```

---

# Quick Increment Table

| CIDR | Increment |
|------|----------:|
| /25 | 128 |
| /26 | 64 |
| /27 | 32 |
| /28 | 16 |
| /29 | 8 |
| /30 | 4 |

The increment tells you where the next subnet begins.

Example:

For `/26`:

```text
0

64

128

192
```

These are the network addresses.

---

# Easy Memory Trick 🧠

Every time you increase the prefix by **1**:

- Number of subnets doubles.
- Number of IP addresses per subnet is cut in half.

Example:

| CIDR | Total IPs |
|------|----------:|
| /24 | 256 |
| /25 | 128 |
| /26 | 64 |
| /27 | 32 |
| /28 | 16 |

Pattern:

```text
256

↓

128

↓

64

↓

32

↓

16
```

---

# AWS Perspective ☁️

Suppose you create a VPC:

```text
10.0.0.0/16
```

Now create four subnets.

```text
Public Subnet A

10.0.1.0/24
```

```text
Public Subnet B

10.0.2.0/24
```

```text
Private App Subnet

10.0.3.0/24
```

```text
Private Database Subnet

10.0.4.0/24
```

Each subnet has its own CIDR block.

AWS allocates Private IP addresses from the subnet's CIDR range.

---

# Why AWS Uses CIDR-Based Subnetting

CIDR-based subnetting allows AWS to:

- Isolate workloads.
- Improve security.
- Separate application tiers.
- Build highly available architectures.
- Efficiently allocate IP addresses.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Increasing the CIDR prefix gives more host addresses."**

✅ **Correct:**

Increasing the prefix **reduces** the number of host addresses.

---

## ❌ Mistake 2

**"A /24 network can have only one subnet."**

✅ **Correct:**

A /24 network can be divided into many smaller subnets, such as /25, /26, /27, and /28.

---

## ❌ Mistake 3

**"AWS automatically creates subnets for every VPC."**

✅ **Correct:**

AWS creates **default subnets** only in the **Default VPC**. In a **Custom VPC**, you create the subnets yourself.

---

# 📝 Quick Revision

- CIDR-based subnetting divides a network into smaller subnets.
- Increasing the CIDR prefix creates more subnets.
- Increasing the CIDR prefix reduces available host addresses.
- The increment determines where each subnet starts.
- AWS VPCs use CIDR-based subnetting for network design.

---

# 💼 Interview Questions

### 1. What is CIDR-Based Subnetting?

**Answer:**

CIDR-Based Subnetting is the process of dividing a larger network into smaller subnets by increasing the CIDR prefix.

---

### 2. What happens when the CIDR prefix increases?

**Answer:**

The number of subnets increases, while the number of available host addresses per subnet decreases.

---

### 3. How many subnets are created when a `/24` network is divided into `/26`?

**Answer:**

Four subnets.

---

### 4. Why does AWS use CIDR-Based Subnetting?

**Answer:**

AWS uses CIDR-based subnetting to efficiently allocate IP addresses, isolate workloads, and design scalable VPC architectures.

---

### 5. What is the subnet increment for a `/27` network?

**Answer:**

32.


# 5. Finding the Network Address, Broadcast Address & Host Range

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Find the Network Address.
- Find the Broadcast Address.
- Find the First and Last Usable Host.
- Calculate the Host Range.
- Solve subnetting questions quickly.
- Apply subnetting calculations in AWS.

---

# 📖 Introduction

Whenever you create a subnet, four important values are calculated:

- Network Address
- First Usable Host
- Last Usable Host
- Broadcast Address

These values define the subnet boundaries and the range of usable IP addresses.

---

# What is a Network Address?

The **Network Address** is the **first IP Address** in a subnet.

It identifies the subnet itself.

It **cannot** be assigned to any host.

---

## 💼 Simple Definition (Interview Answer)

> The **Network Address** is the first IP address of a subnet and uniquely identifies that subnet.

---

# What is a Broadcast Address?

The **Broadcast Address** is the **last IP Address** in a subnet.

It is used to send data to every device within that subnet.

It **cannot** be assigned to a host.

---

## 💼 Simple Definition (Interview Answer)

> The **Broadcast Address** is the last IP address of a subnet and is used for broadcast communication.

---

# What is the First Usable Host?

The first usable host is:

```text
Network Address + 1
```

Example:

```text
Network

192.168.1.0
```

First Host:

```text
192.168.1.1
```

---

# What is the Last Usable Host?

The last usable host is:

```text
Broadcast Address − 1
```

Example:

```text
Broadcast

192.168.1.255
```

Last Host:

```text
192.168.1.254
```

---

# Example 1

Subnet:

```text
192.168.1.0/24
```

Network Address

```text
192.168.1.0
```

First Host

```text
192.168.1.1
```

Last Host

```text
192.168.1.254
```

Broadcast Address

```text
192.168.1.255
```

---

# Example 2

Subnet:

```text
192.168.1.64/26
```

Subnet Increment:

```text
64
```

Network Address

```text
192.168.1.64
```

Broadcast Address

```text
192.168.1.127
```

First Host

```text
192.168.1.65
```

Last Host

```text
192.168.1.126
```

---

# Example 3

Subnet:

```text
192.168.10.96/27
```

Subnet Increment:

```text
32
```

Network Address

```text
192.168.10.96
```

Broadcast Address

```text
192.168.10.127
```

First Host

```text
192.168.10.97
```

Last Host

```text
192.168.10.126
```

---

# Example 4

Subnet:

```text
10.0.1.0/28
```

Subnet Increment:

```text
16
```

Network Address

```text
10.0.1.0
```

Broadcast Address

```text
10.0.1.15
```

First Host

```text
10.0.1.1
```

Last Host

```text
10.0.1.14
```

---

# Visual Representation

```text
Network Address

↓

First Host

↓

Usable Hosts

↓

Last Host

↓

Broadcast Address
```

Example:

```text
192.168.1.64/26

64     65     ...     126     127

│      │               │        │

Network First Host Last Host Broadcast
```

---

# Quick Calculation Method

### Step 1

Identify the CIDR prefix.

Example:

```text
192.168.1.64/26
```

---

### Step 2

Find the subnet increment.

```text
/26

↓

64
```

---

### Step 3

Network Address

```text
64
```

---

### Step 4

Broadcast Address

```text
64 + 64 − 1

=

127
```

---

### Step 5

First Host

```text
65
```

---

### Step 6

Last Host

```text
126
```

Done!

---

# Quick Reference Table

| CIDR | Increment | Total IPs | Traditional Usable Hosts |
|------|----------:|----------:|-------------------------:|
| /24 | 256 | 256 | 254 |
| /25 | 128 | 128 | 126 |
| /26 | 64 | 64 | 62 |
| /27 | 32 | 32 | 30 |
| /28 | 16 | 16 | 14 |
| /29 | 8 | 8 | 6 |

---

# AWS Perspective ☁️

Suppose you create the subnet:

```text
10.0.1.0/24
```

AWS reserves these addresses:

| Address | Purpose |
|----------|----------|
| 10.0.1.0 | Network Address |
| 10.0.1.1 | VPC Router |
| 10.0.1.2 | Amazon DNS |
| 10.0.1.3 | Reserved |
| 10.0.1.255 | Reserved by AWS |

Therefore, the first EC2 instance receives an IP starting from:

```text
10.0.1.4
```

Even though traditional networking says the first usable host is `10.0.1.1`, AWS reserves additional addresses for VPC operations.

---

# Real AWS Example

```text
VPC

10.0.0.0/16

│

├── Public Subnet

│      10.0.1.0/24

│      EC2 → 10.0.1.10

│

└── Private Subnet

       10.0.2.0/24

       EC2 → 10.0.2.20
```

AWS automatically allocates IP addresses from the usable range of each subnet.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"The Network Address can be assigned to a device."**

✅ **Correct:**

The Network Address identifies the subnet and cannot be assigned to a host.

---

## ❌ Mistake 2

**"The Broadcast Address can be assigned to a host."**

✅ **Correct:**

The Broadcast Address is reserved and cannot be assigned to a host.

---

## ❌ Mistake 3

**"AWS uses every usable IP address."**

✅ **Correct:**

AWS reserves **5 IP addresses** in every subnet, reducing the number of usable IPs.

---

# 📝 Quick Revision

- Network Address = First IP of the subnet.
- Broadcast Address = Last IP of the subnet.
- First Host = Network Address + 1 (traditional networking).
- Last Host = Broadcast Address − 1.
- AWS reserves 5 IP addresses in every subnet.
- Use the subnet increment to quickly calculate subnet boundaries.

---

# 💼 Interview Questions

### 1. What is a Network Address?

**Answer:**

The Network Address is the first IP address of a subnet and identifies the subnet.

---

### 2. What is a Broadcast Address?

**Answer:**

The Broadcast Address is the last IP address of a subnet and is used to send packets to all devices in that subnet.

---

### 3. How do you find the First Usable Host?

**Answer:**

First Usable Host = Network Address + 1 (traditional networking).

---

### 4. How do you find the Last Usable Host?

**Answer:**

Last Usable Host = Broadcast Address − 1.

---

### 5. What is the first IP address that AWS can assign in a `/24` subnet?

**Answer:**

Although the traditional first usable host is `.1`, AWS reserves `.1`, `.2`, and `.3`. Therefore, the first assignable IP address is typically `.4`.


# 6. How to Calculate Subnets

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Calculate the number of subnets.
- Calculate the number of hosts.
- Understand Borrowed Bits and Host Bits.
- Solve subnetting questions step by step.
- Apply subnet calculations in AWS VPC design.
- Answer subnetting interview questions confidently.

---

# 📖 Introduction

When subnetting a network, there are two common questions:

1. **How many subnets can I create?**
2. **How many hosts can each subnet support?**

To answer these, we use two simple formulas.

---

# Formula 1 – Number of Subnets

The formula is:

```text
Number of Subnets = 2^(Borrowed Bits)
```

### What are Borrowed Bits?

Borrowed Bits are the bits taken from the **Host Portion** and added to the **Network Portion**.

Every borrowed bit doubles the number of available subnets.

---

## Example

Original Network:

```text
192.168.1.0/24
```

New Network:

```text
192.168.1.0/26
```

Borrowed Bits:

```text
26 − 24 = 2
```

Number of Subnets:

```text
2² = 4
```

So a `/24` network becomes **4 subnets**.

---

# Formula 2 – Number of Hosts

The formula is:

```text
Total IP Addresses = 2^(Host Bits)
```

Traditional usable hosts:

```text
Usable Hosts = 2^(Host Bits) − 2
```

---

## Example

CIDR:

```text
/26
```

Host Bits:

```text
32 − 26 = 6
```

Total IP Addresses:

```text
2⁶ = 64
```

Traditional Usable Hosts:

```text
64 − 2 = 62
```

AWS Usable Hosts:

```text
64 − 5 = 59
```

Because AWS reserves **5 IP addresses** in every subnet.

---

# Step-by-Step Example 1

Original Network:

```text
192.168.1.0/24
```

Required:

Convert to:

```text
/25
```

### Step 1

Borrowed Bits:

```text
25 − 24 = 1
```

### Step 2

Subnets:

```text
2¹ = 2
```

### Step 3

Host Bits:

```text
32 − 25 = 7
```

### Step 4

Total IPs:

```text
2⁷ = 128
```

### Step 5

Traditional Hosts:

```text
126
```

AWS Hosts:

```text
123
```

---

# Step-by-Step Example 2

Network:

```text
10.0.0.0/16
```

Convert to:

```text
/20
```

### Borrowed Bits

```text
20 − 16 = 4
```

### Number of Subnets

```text
2⁴ = 16
```

### Host Bits

```text
32 − 20 = 12
```

### Total IPs

```text
2¹² = 4096
```

Traditional Hosts:

```text
4094
```

AWS Hosts:

```text
4091
```

---

# Step-by-Step Example 3

Network:

```text
172.16.0.0/16
```

Convert to:

```text
/24
```

Borrowed Bits:

```text
24 − 16 = 8
```

Subnets:

```text
2⁸ = 256
```

Host Bits:

```text
8
```

Total IPs:

```text
256
```

Traditional Hosts:

```text
254
```

AWS Hosts:

```text
251
```

---

# Quick Formula Summary

## Number of Subnets

```text
2^(Borrowed Bits)
```

---

## Total IP Addresses

```text
2^(Host Bits)
```

---

## Traditional Usable Hosts

```text
2^(Host Bits) − 2
```

---

## AWS Usable Hosts

```text
2^(Host Bits) − 5
```

---

# Quick Reference Table

| CIDR | Host Bits | Total IPs | Traditional Hosts | AWS Hosts |
|------|----------:|----------:|------------------:|----------:|
| /24 | 8 | 256 | 254 | 251 |
| /25 | 7 | 128 | 126 | 123 |
| /26 | 6 | 64 | 62 | 59 |
| /27 | 5 | 32 | 30 | 27 |
| /28 | 4 | 16 | 14 | 11 |
| /29 | 3 | 8 | 6 | 3 |

---

# Easy Memory Trick 🧠

Every borrowed bit:

```text
Subnets × 2
```

Every additional prefix:

```text
Hosts ÷ 2
```

Example:

```text
/24

↓

/25

↓

/26

↓

/27
```

Subnets:

```text
1

↓

2

↓

4

↓

8
```

Hosts:

```text
256

↓

128

↓

64

↓

32
```

---

# AWS Perspective ☁️

Suppose you create:

```text
VPC

10.0.0.0/16
```

You divide it into:

```text
16 Subnets
```

Each subnet uses:

```text
/20
```

AWS automatically assigns:

- Network Address
- Reserved IPs
- Available Host IPs

Each subnet can contain:

```text
4091 Assignable IP Addresses
```

after AWS reserves five addresses.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Borrowed Bits are taken from the Network Portion."**

✅ **Correct:**

Borrowed Bits are taken from the **Host Portion**.

---

## ❌ Mistake 2

**"A larger CIDR prefix means more hosts."**

✅ **Correct:**

A larger prefix means **fewer host addresses**.

---

## ❌ Mistake 3

**"AWS usable hosts = Total IPs − 2."**

✅ **Correct:**

AWS reserves **5 IP addresses** in every subnet.

---

# 📝 Quick Revision

- Number of Subnets = **2^(Borrowed Bits)**
- Total IP Addresses = **2^(Host Bits)**
- Traditional Hosts = **2^(Host Bits) − 2**
- AWS Hosts = **2^(Host Bits) − 5**
- Borrowed Bits come from the Host Portion.
- Every borrowed bit doubles the number of subnets.

---

# 💼 Interview Questions

### 1. How do you calculate the number of subnets?

**Answer:**

Number of Subnets = **2^(Borrowed Bits)**

---

### 2. How do you calculate the total number of IP addresses?

**Answer:**

Total IP Addresses = **2^(Host Bits)**

---

### 3. How many subnets are created when a `/24` network is subnetted into `/26`?

**Answer:**

Borrowed Bits = 2

Number of Subnets = **2² = 4**

---

### 4. How many usable IP addresses are available in an AWS `/28` subnet?

**Answer:**

A `/28` subnet has 16 total IP addresses. AWS reserves 5, so **11 IP addresses** are assignable.

---

### 5. What happens when you increase the CIDR prefix?

**Answer:**

The number of subnets increases, while the number of available host addresses per subnet decreases.


# 7. Variable Length Subnet Mask (VLSM)

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand what VLSM is.
- Learn why VLSM is used.
- Understand the difference between FLSM and VLSM.
- Design efficient subnetting using VLSM.
- Apply VLSM in AWS VPC design.
- Answer VLSM interview questions confidently.

---

# 📖 Introduction

Imagine a company has three departments:

- HR → 20 Employees
- Finance → 50 Employees
- IT → 200 Employees

If we give every department a subnet that supports **254 hosts**, most IP addresses will remain unused.

This wastes IP addresses.

To avoid this problem, networking uses **Variable Length Subnet Mask (VLSM).**

---

# What is VLSM?

**VLSM (Variable Length Subnet Mask)** is a subnetting technique that allows different subnets within the same network to have **different subnet sizes**, based on the number of hosts required.

Instead of giving every subnet the same number of IP addresses, each subnet receives only what it needs.

---

## 💼 Simple Definition (Interview Answer)

> **VLSM (Variable Length Subnet Mask) is a subnetting technique that allows different subnet sizes within the same network, improving IP address utilization.**

---

# Why Do We Need VLSM?

Suppose a company has the following departments:

| Department | Devices |
|------------|--------:|
| HR | 20 |
| Finance | 50 |
| IT | 200 |

If every department receives:

```text
/24

256 Addresses
```

Most addresses are wasted.

Example:

| Department | Required | Allocated | Wasted |
|------------|---------:|----------:|--------:|
| HR | 20 | 256 | 236 |
| Finance | 50 | 256 | 206 |
| IT | 200 | 256 | 56 |

This is inefficient.

---

# Solution Using VLSM

Allocate subnet sizes based on actual requirements.

| Department | Required Hosts | Suggested CIDR |
|------------|---------------:|---------------|
| IT | 200 | /24 |
| Finance | 50 | /26 |
| HR | 20 | /27 |

Now the IP addresses are used much more efficiently.

---

# FLSM vs VLSM

---

## FLSM (Fixed Length Subnet Mask)

Every subnet has the same size.

Example:

```text
HR

/24
```

```text
Finance

/24
```

```text
IT

/24
```

Simple, but wasteful.

---

## VLSM (Variable Length Subnet Mask)

Each subnet is sized according to its needs.

Example:

```text
IT

/24
```

```text
Finance

/26
```

```text
HR

/27
```

Efficient and flexible.

---

# Comparison

| Feature | FLSM | VLSM |
|---------|------|------|
| Subnet Size | Same | Different |
| IP Utilization | Poor | Excellent |
| Flexibility | Low | High |
| Used Today | Rarely | Yes |

---

# Practical Example

Suppose you own:

```text
10.0.0.0/16
```

Requirements:

| Department | Hosts |
|------------|------:|
| IT | 200 |
| Finance | 60 |
| HR | 25 |

Using VLSM:

```text
IT

10.0.0.0/24
```

```text
Finance

10.0.1.0/26
```

```text
HR

10.0.1.64/27
```

Every subnet receives only the number of IP addresses it needs.

---

# Steps to Design VLSM

### Step 1

List all networks.

---

### Step 2

Arrange them from **largest** to **smallest**.

Example:

```text
IT

200 Hosts
```

```text
Finance

60 Hosts
```

```text
HR

25 Hosts
```

---

### Step 3

Allocate the largest subnet first.

Example:

```text
10.0.0.0/24
```

---

### Step 4

Allocate the next available subnet.

```text
10.0.1.0/26
```

---

### Step 5

Allocate the remaining subnet.

```text
10.0.1.64/27
```

Done!

---

# Real-Life Analogy

Imagine a hotel.

You have three groups:

- Family → 3 Rooms
- School Tour → 40 Rooms
- Corporate Event → 100 Rooms

Would you give every group 100 rooms?

No.

Each group receives only the number of rooms it needs.

VLSM works exactly the same way with IP addresses.

---

# AWS Perspective ☁️

AWS uses VLSM extensively.

Suppose your VPC is:

```text
10.0.0.0/16
```

You design your network like this:

```text
Public Subnet

10.0.1.0/24
```

```text
Private App Subnet

10.0.2.0/24
```

```text
Database Subnet

10.0.3.0/27
```

```text
Management Subnet

10.0.3.32/28
```

Notice that every subnet has a different size.

This is VLSM.

---

# Why AWS Uses VLSM

AWS environments grow over time.

Some workloads require:

- Hundreds of EC2 instances.

Others require:

- Only a few database servers.

Using VLSM allows:

- Better IP utilization.
- Easier expansion.
- Lower IP wastage.
- Flexible network design.

---

# Best Practices

✅ Allocate larger subnets for application servers.

✅ Allocate smaller subnets for databases.

✅ Leave unused address space for future expansion.

✅ Design subnets based on expected growth, not just current usage.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"VLSM and CIDR are the same."**

✅ **Correct:**

CIDR is the addressing method.

VLSM is the subnetting technique that uses CIDR to create different-sized subnets.

---

## ❌ Mistake 2

**"Every AWS subnet should be /24."**

✅ **Correct:**

Choose subnet sizes based on application requirements.

---

## ❌ Mistake 3

**"VLSM wastes more IP addresses."**

✅ **Correct:**

VLSM reduces IP address wastage by allocating subnet sizes according to actual needs.

---

# 📝 Quick Revision

- VLSM = Variable Length Subnet Mask.
- Different subnets can have different sizes.
- Improves IP address utilization.
- Better than FLSM.
- AWS commonly uses VLSM in VPC design.
- Always allocate the largest subnet first.

---

# 💼 Interview Questions

### 1. What is VLSM?

**Answer:**

VLSM is a subnetting technique that allows different subnet sizes within the same network, improving IP address utilization.

---

### 2. Why is VLSM used?

**Answer:**

To reduce IP address wastage by allocating subnet sizes according to actual requirements.

---

### 3. What is the difference between FLSM and VLSM?

**Answer:**

FLSM uses the same subnet size for every subnet, while VLSM allows different subnet sizes.

---

### 4. Does AWS use VLSM?

**Answer:**

Yes. AWS VPCs commonly use VLSM to create subnets of different sizes based on workload requirements.

---

### 5. What is the best practice when designing VLSM?

**Answer:**

Allocate the largest subnet first, then assign smaller subnets to the remaining address space.

# 8. AWS Subnet Design

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand how AWS subnets are designed.
- Learn Public, Private, and Database Subnets.
- Understand Multi-AZ subnet design.
- Design secure and highly available VPC architectures.
- Follow AWS networking best practices.
- Answer AWS subnet design interview questions confidently.

---

# 📖 Introduction

In AWS, a subnet is more than just a range of IP addresses.

A subnet determines:

- Which resources can access the Internet.
- Which resources remain private.
- How traffic flows inside a VPC.
- The security level of your application.

A well-designed subnet architecture improves:

- Security
- High Availability
- Scalability
- Performance

---

# Typical AWS Subnet Types

A production VPC usually contains three types of subnets:

- Public Subnet
- Private Application Subnet
- Private Database Subnet

Each subnet serves a different purpose.

---

# 1. Public Subnet

A **Public Subnet** is a subnet that has a route to an **Internet Gateway (IGW).**

Route Table:

```text
Destination

0.0.0.0/0

↓

Internet Gateway
```

Resources commonly placed here:

- Bastion Host
- NAT Gateway
- Application Load Balancer (ALB)
- Public EC2 Instances

---

## Example

```text
Public Subnet

10.0.1.0/24
```

Resources:

```text
ALB

NAT Gateway

Bastion Host
```

These resources can communicate directly with the Internet.

---

# 2. Private Application Subnet

A **Private Application Subnet** does not have a direct route to the Internet.

Instead, it accesses the Internet through a **NAT Gateway** when needed.

Resources commonly placed here:

- Application Servers
- Backend EC2 Instances
- Internal APIs
- ECS Tasks
- EKS Worker Nodes

---

## Example

```text
Private App Subnet

10.0.2.0/24
```

Internet Access:

```text
EC2

↓

NAT Gateway

↓

Internet
```

Inbound Internet traffic is not allowed directly.

---

# 3. Private Database Subnet

Database servers should never be exposed to the Internet.

Resources commonly placed here:

- Amazon RDS
- Amazon Aurora
- Amazon DocumentDB
- Amazon ElastiCache

Example:

```text
Database Subnet

10.0.3.0/27
```

Only application servers are allowed to communicate with the database.

---

# Typical AWS Architecture

```text
                    Internet
                        │
                        ▼
              Internet Gateway
                        │
                        ▼
            Public Subnet (10.0.1.0/24)
        ┌──────────────────────────────┐
        │  Application Load Balancer   │
        │      NAT Gateway             │
        └──────────────────────────────┘
                        │
                        ▼
         Private App Subnet (10.0.2.0/24)
        ┌──────────────────────────────┐
        │      EC2 Application         │
        │       ECS / EKS              │
        └──────────────────────────────┘
                        │
                        ▼
      Private DB Subnet (10.0.3.0/27)
        ┌──────────────────────────────┐
        │      Amazon RDS              │
        │     Amazon Aurora            │
        └──────────────────────────────┘
```

---

# Multi-AZ Design

AWS recommends creating subnets in multiple Availability Zones.

Example:

```text
Availability Zone A

Public Subnet

10.0.1.0/24

Private App

10.0.11.0/24

Database

10.0.21.0/27
```

```text
Availability Zone B

Public Subnet

10.0.2.0/24

Private App

10.0.12.0/24

Database

10.0.22.0/27
```

Benefits:

- High Availability
- Fault Tolerance
- Disaster Recovery
- Better Performance

---

# Communication Flow

```text
User

↓

Internet

↓

Application Load Balancer

↓

Application Server

↓

Amazon RDS
```

The database never communicates directly with Internet users.

---

# Why Separate Subnets?

Suppose a hacker attacks your website.

If everything is placed in one subnet:

```text
Web Server

Database

Application

Same Network
```

the attacker may gain access to all resources.

Instead, AWS isolates them:

```text
Public Subnet

↓

Application Subnet

↓

Database Subnet
```

This greatly improves security.

---

# AWS Best Practices

✅ Keep databases in Private Subnets.

✅ Place Load Balancers in Public Subnets.

✅ Use NAT Gateway for outbound Internet access.

✅ Use at least two Availability Zones.

✅ Keep Public and Private resources separate.

✅ Use Security Groups and NACLs to control traffic.

✅ Leave free CIDR space for future expansion.

---

# Real Production Example

```text
VPC

10.0.0.0/16

│

├── Public AZ-A

│      10.0.1.0/24

├── Public AZ-B

│      10.0.2.0/24

├── App AZ-A

│      10.0.11.0/24

├── App AZ-B

│      10.0.12.0/24

├── DB AZ-A

│      10.0.21.0/27

└── DB AZ-B

       10.0.22.0/27
```

This architecture provides:

- High Availability
- Better Security
- Auto Scaling Support
- Load Balancing
- Easy Maintenance

---

# AWS Perspective ☁️

Every AWS production environment follows the same basic design principles:

- Public Subnets for Internet-facing resources.
- Private Application Subnets for business logic.
- Private Database Subnets for data storage.
- Multiple Availability Zones for High Availability.
- CIDR planning to avoid future IP conflicts.

This design is used by organizations ranging from startups to large enterprises.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Amazon RDS should be placed in a Public Subnet."**

✅ **Correct:**

Amazon RDS should normally be placed in a **Private Subnet**.

---

## ❌ Mistake 2

**"Every EC2 instance should have a Public IP."**

✅ **Correct:**

Only Internet-facing instances require a Public IP.

Backend application servers should remain private.

---

## ❌ Mistake 3

**"One Availability Zone is enough."**

✅ **Correct:**

Production workloads should use multiple Availability Zones for High Availability.

---

# 📝 Quick Revision

- Public Subnet → Internet-facing resources.
- Private App Subnet → Application servers.
- Private DB Subnet → Databases.
- Use Internet Gateway for Public Subnets.
- Use NAT Gateway for Private Subnets.
- Deploy across multiple Availability Zones.
- Follow the principle of least privilege.

---

# 💼 Interview Questions

### 1. What is the difference between a Public and a Private Subnet?

**Answer:**

A Public Subnet has a route to an Internet Gateway, while a Private Subnet does not have direct Internet access and typically uses a NAT Gateway for outbound traffic.

---

### 2. Which AWS resources are usually placed in a Public Subnet?

**Answer:**

- Application Load Balancer
- NAT Gateway
- Bastion Host
- Public EC2 Instances

---

### 3. Which AWS resources should be placed in a Private Database Subnet?

**Answer:**

Amazon RDS, Amazon Aurora, Amazon DocumentDB, and Amazon ElastiCache.

---

### 4. Why do production environments use multiple Availability Zones?

**Answer:**

To improve High Availability, Fault Tolerance, and Disaster Recovery.

---

### 5. Why should databases not be placed in Public Subnets?

**Answer:**

Keeping databases in Private Subnets protects them from direct Internet access and improves security.






