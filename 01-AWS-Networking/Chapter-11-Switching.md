# 1. Introduction to Switching

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand what Switching is.
- Learn why Switching is needed.
- Understand the purpose of a Network Switch.
- Learn how Switching improves network communication.
- Understand the role of Switching in modern networks.
- Relate Switching concepts to AWS networking.
- Answer Switching interview questions confidently.

---

# 📖 Introduction

Imagine you're in a classroom with 50 students.

You want to give a notebook to your friend.

There are two ways to do it.

### Method 1

You hand the notebook to the teacher, and the teacher gives a copy to every student.

Everyone receives it, even though only one student needed it.

This wastes time and resources.

---

### Method 2

The teacher knows exactly where your friend is sitting.

The notebook is delivered only to your friend.

Fast.

Efficient.

No unnecessary traffic.

A network works in exactly the same way.

Older networks used **Hubs**, which sent data to every connected device.

Modern networks use **Switches**, which send data only to the intended destination.

This process is called **Switching**.

---

# What is Switching?

**Switching** is the process of forwarding data from one device to another by identifying the correct destination device.

Instead of sending data to every device on the network, a switch sends it only to the intended recipient.

This improves:

- Network Performance
- Speed
- Security
- Bandwidth Utilization

---

# Definition

**Switching** is the process of receiving a data frame, identifying the destination MAC Address, and forwarding the frame to the correct device.

It is one of the fundamental concepts of Local Area Networks (LANs).

---

# Why is Switching Needed?

Imagine a company with:

- 500 Computers
- 50 Printers
- 100 IP Phones

Suppose Computer A wants to send data to Computer B.

Without switching:

```text
Computer A

↓

Everyone Receives Data

↓

499 Devices Ignore It
```

This wastes:

- Bandwidth
- Network Speed
- Processing Power

---

With Switching:

```text
Computer A

↓

Switch

↓

Computer B
```

Only the intended device receives the data.

---

# Problems Without Switching

If switching didn't exist:

- Every device would receive every frame.
- The network would become congested.
- Performance would decrease.
- More collisions would occur.
- Security would be reduced because every device could see the traffic.

---

# Benefits of Switching

Switching provides several advantages:

- Faster Communication
- Efficient Data Transfer
- Better Network Performance
- Reduced Network Congestion
- Improved Security
- Reduced Collisions
- Better Bandwidth Utilization

---

# Where is Switching Used?

Switching is used in almost every modern network.

Examples include:

- Home Networks
- Offices
- Schools
- Colleges
- Data Centers
- Enterprise Networks
- Cloud Data Centers

Whenever devices communicate within the same Local Area Network (LAN), switching is involved.

---

# High-Level Working of Switching

The communication process is simple.

```text
Computer A

↓

Network Switch

↓

Computer B
```

The switch receives the frame, checks the destination MAC Address, and forwards the frame only to the correct device.

---

# Real-Life Analogy 📦

Imagine a courier company.

Without knowing addresses:

```text
Parcel

↓

Delivered to Every House
```

Very inefficient.

With proper addresses:

```text
Parcel

↓

Courier Office

↓

Correct House
```

Similarly:

```text
Data Frame

↓

Switch

↓

Correct Device
```

The switch acts like a courier service that delivers data only to the correct destination.

---

# Switching vs Broadcasting

Broadcasting

```text
Computer

↓

All Devices Receive Data
```

Switching

```text
Computer

↓

Only Destination Device Receives Data
```

This is why switches are much more efficient than hubs.

---

# AWS Perspective ☁️

Although AWS customers never see physical switches, switching still happens inside AWS.

When two EC2 instances communicate within the same subnet:

```text
EC2 Instance A

↓

AWS Virtual Network

↓

EC2 Instance B
```

AWS performs switching internally using virtual networking technologies.

You don't configure physical switches in AWS, but the same switching concepts are used behind the scenes.

---

# Real AWS Scenario

Suppose two EC2 instances are launched in the same subnet.

```text
EC2-A

10.0.1.10

↓

Amazon VPC

↓

EC2-B

10.0.1.20
```

When EC2-A sends data to EC2-B:

- AWS identifies the destination.
- The traffic is forwarded directly.
- Other instances in the subnet do not receive the frame.

This is virtual switching.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"A Switch sends data to every device."**

✅ **Correct:**

A Switch sends data only to the intended destination device.

---

## ❌ Mistake 2

**"Switching and Routing are the same."**

✅ **Correct:**

- Switching forwards data within the same network using MAC Addresses.
- Routing forwards packets between different networks using IP Addresses.

---

## ❌ Mistake 3

**"Switches use IP Addresses to forward frames."**

✅ **Correct:**

A Layer 2 Switch forwards frames using **MAC Addresses**.

---

## ❌ Mistake 4

**"AWS does not use Switching."**

✅ **Correct:**

AWS uses virtual switching inside Amazon VPCs, even though customers do not manage physical switches.

---

# 📝 Quick Revision

- Switching forwards data to the correct destination.
- Switches use MAC Addresses.
- Switching improves speed and efficiency.
- Switching reduces unnecessary network traffic.
- Switching is used in LANs.
- AWS performs switching virtually inside Amazon VPC.

---

# 💼 Interview Questions

### 1. What is Switching?

**Answer:**

Switching is the process of forwarding data frames from one device to another by using the destination MAC Address.

---

### 2. Why is Switching needed?

**Answer:**

Switching reduces unnecessary network traffic, improves performance, increases bandwidth efficiency, and delivers data only to the intended destination.

---

### 3. What address does a Switch use to forward data?

**Answer:**

A Layer 2 Switch uses the **MAC Address** to identify the destination device and forward frames.

---

### 4. Where is Switching commonly used?

**Answer:**

Switching is commonly used in Local Area Networks (LANs) such as homes, offices, schools, data centers, and enterprise networks.

---

### 5. Does AWS use physical switches?

**Answer:**

AWS customers do not manage physical switches. AWS uses **virtual switching** within Amazon VPCs to forward traffic between resources.

---

### 6. What is the difference between Switching and Routing?

**Answer:**

| Switching | Routing |
|-----------|---------|
| Uses MAC Address | Uses IP Address |
| Works within the same network (LAN) | Works between different networks |
| Performed by a Switch | Performed by a Router |
| Operates mainly at Layer 2 | Operates at Layer 3 |

---


# 2. What is a Network Switch?

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand what a Network Switch is.
- Learn the purpose of a Network Switch.
- Understand how a Switch works.
- Differentiate between a Switch and a Hub.
- Learn where Switches are used.
- Understand the importance of Switches in AWS networking.
- Answer Switch interview questions confidently.

---

# 📖 Introduction

Imagine you work in an office with 100 employees.

One employee wants to send an important document to another employee.

There are two possibilities.

### Without a Switch

The document is copied and delivered to all 100 employees.

Everyone receives it, but only one person actually needs it.

This wastes:

- Time
- Resources
- Network Bandwidth

---

### With a Switch

The office receptionist knows exactly where the employee sits.

The document is delivered only to that employee.

Fast.

Efficient.

No unnecessary communication.

A **Network Switch** works in the same way.

---

# What is a Network Switch?

A **Network Switch** is a networking device that connects multiple devices within a Local Area Network (LAN) and forwards data only to the intended destination device.

Unlike a Hub, a Switch does **not** send data to every connected device.

Instead, it intelligently forwards data using the destination **MAC Address**.

---

# Definition

A **Network Switch** is a Layer 2 networking device that receives Ethernet frames, examines the destination MAC Address, and forwards the frame to the correct device.

---

# Purpose of a Switch

The main purpose of a Switch is to:

- Connect multiple devices.
- Reduce unnecessary network traffic.
- Improve communication speed.
- Increase network efficiency.
- Reduce collisions.

---

# Devices Connected to a Switch

A Switch can connect:

- Computers
- Laptops
- Printers
- IP Phones
- Servers
- Wireless Access Points
- CCTV Cameras
- Other Switches

Example

```text
                +-------------+
                |   Switch    |
                +-------------+
                 /   |    |   \
                /    |    |    \
             PC1   PC2  Printer Server
```

All devices communicate through the Switch.

---

# How Does a Switch Work?

The working process is simple.

### Step 1

The Switch receives an Ethernet Frame.

```text
Computer A

↓

Switch
```

---

### Step 2

The Switch checks the destination MAC Address.

Example

```text
Destination MAC

AA:BB:CC:DD:EE:FF
```

---

### Step 3

The Switch looks inside its **MAC Address Table (CAM Table).**

---

### Step 4

If the MAC Address exists:

```text
Switch

↓

Correct Port Found

↓

Frame Forwarded
```

---

### Step 5

Only the destination device receives the frame.

```text
Computer A

↓

Switch

↓

Computer B
```

Other devices never receive the frame.

---

# Features of a Network Switch

A Switch provides:

- Intelligent Forwarding
- MAC Address Learning
- High-Speed Communication
- Full Duplex Communication
- Reduced Collisions
- Better Network Performance

---

# Why is a Switch Faster Than a Hub?

A Hub simply copies data to every connected device.

```text
Hub

↓

All Devices Receive Data
```

A Switch forwards data only to the required device.

```text
Switch

↓

Only Destination Device Receives Data
```

This greatly improves network efficiency.

---

# Where are Switches Used?

Switches are used in:

- Homes
- Offices
- Schools
- Colleges
- Hospitals
- Banks
- Data Centers
- Enterprise Networks
- Cloud Data Centers

Almost every modern LAN uses switches.

---

# Real-Life Analogy 📦

Imagine a courier company.

Without knowing addresses:

```text
Parcel

↓

Every House
```

Very inefficient.

With addresses:

```text
Parcel

↓

Courier Office

↓

Correct House
```

Similarly,

```text
Data

↓

Switch

↓

Correct Device
```

The Switch acts like a smart courier service.

---

# AWS Perspective ☁️

AWS does not expose physical switches to customers.

However, switching still happens behind the scenes.

Suppose two EC2 instances are in the same subnet.

```text
EC2-A

↓

Virtual Switch

↓

EC2-B
```

AWS uses virtual networking technologies to forward traffic efficiently between resources inside a VPC.

This behaves similarly to a physical Layer 2 Switch.

---

# Real AWS Scenario

Suppose you have:

```text
EC2-1

10.0.1.10
```

```text
EC2-2

10.0.1.20
```

Both are in the same subnet.

When EC2-1 sends traffic to EC2-2:

```text
EC2-1

↓

AWS Virtual Network

↓

EC2-2
```

Traffic is delivered only to EC2-2.

Other EC2 instances in the subnet do not receive the frame.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"A Switch sends data to every device."**

✅ **Correct:**

A Switch sends data only to the destination device.

---

## ❌ Mistake 2

**"Switches use IP Addresses."**

✅ **Correct:**

A Layer 2 Switch uses **MAC Addresses** for forwarding.

---

## ❌ Mistake 3

**"A Switch and Hub work the same way."**

✅ **Correct:**

A Hub broadcasts data to every device, while a Switch intelligently forwards data only to the intended destination.

---

## ❌ Mistake 4

**"AWS does not use switching."**

✅ **Correct:**

AWS uses virtual switching inside Amazon VPCs to enable communication between resources.

---

# 📝 Quick Revision

- A Switch connects devices in a LAN.
- A Switch forwards data using MAC Addresses.
- A Switch reduces unnecessary traffic.
- A Switch improves network performance.
- A Switch is smarter and faster than a Hub.
- AWS performs virtual switching inside VPCs.

---

# 💼 Interview Questions

### 1. What is a Network Switch?

**Answer:**

A Network Switch is a Layer 2 networking device that connects multiple devices in a LAN and forwards Ethernet frames to the correct destination using MAC Addresses.

---

### 2. What is the primary purpose of a Switch?

**Answer:**

The primary purpose of a Switch is to efficiently forward data only to the intended destination, improving network performance and reducing unnecessary traffic.

---

### 3. Which address does a Switch use to forward data?

**Answer:**

A Layer 2 Switch uses the **destination MAC Address** to forward Ethernet frames.

---

### 4. Why is a Switch more efficient than a Hub?

**Answer:**

A Switch sends data only to the intended destination, whereas a Hub sends data to every connected device, creating unnecessary traffic.

---

### 5. Where are Network Switches commonly used?

**Answer:**

Network Switches are commonly used in homes, offices, schools, data centers, enterprise networks, and cloud environments.

---

### 6. How does AWS implement switching?

**Answer:**

AWS uses virtual switching within Amazon VPCs to enable communication between EC2 instances and other resources. Customers do not manage physical switches, but the same switching principles apply behind the scenes.

---


# 3. How Switching Works

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand how a Switch forwards data.
- Learn the complete switching process.
- Understand MAC Address learning.
- Learn frame forwarding.
- Understand flooding and filtering.
- Relate switching to AWS networking.
- Answer switching interview questions confidently.

---

# 📖 Introduction

Suppose there are three computers connected to a Switch.

```text
        +------------+
        |   Switch   |
        +------------+
        /     |      \
      PC-A   PC-B   PC-C
```

Now, **PC-A wants to send data to PC-B.**

How does the Switch know where PC-B is connected?

Does it send the data to every computer?

No.

Instead, it follows a series of intelligent steps.

This entire process is called **Switching**.

---

# Switching Process Overview

Whenever a Switch receives a frame, it performs four main tasks.

```text
Receive Frame

↓

Learn Source MAC Address

↓

Check Destination MAC Address

↓

Forward Frame
```

If the destination is unknown, it floods the frame.

If the destination is known, it forwards it to the correct port.

---

# Step 1 – Receive the Frame

Suppose PC-A sends data.

```text
PC-A

↓

Ethernet Frame

↓

Switch
```

The Switch receives the Ethernet frame on one of its ports.

---

# Step 2 – Learn the Source MAC Address

Every Ethernet frame contains:

- Source MAC Address
- Destination MAC Address

Example

```text
Source MAC

AA:AA:AA:AA:AA:AA
```

The Switch stores the Source MAC Address in its **MAC Address Table (CAM Table).**

Example

```text
MAC Address

AA:AA:AA:AA:AA:AA

↓

Port 1
```

This process is called **MAC Learning**.

---

# Step 3 – Check the Destination MAC Address

Now the Switch examines:

```text
Destination MAC

BB:BB:BB:BB:BB:BB
```

It searches the CAM Table.

Two situations are possible.

---

# Case 1 – Destination MAC Found ✅

Suppose the CAM Table contains:

```text
BB:BB:BB:BB:BB:BB

↓

Port 2
```

The Switch immediately forwards the frame.

```text
PC-A

↓

Switch

↓

PC-B
```

Only PC-B receives the frame.

---

# Case 2 – Destination MAC Not Found ❌

Suppose the CAM Table does not contain:

```text
BB:BB:BB:BB:BB:BB
```

The Switch doesn't know where PC-B is connected.

So it performs **Flooding**.

---

# Flooding

Flooding means sending the frame to **every port except the incoming port.**

Example

```text
        +------------+
        |   Switch   |
        +------------+
        /     |      \
      PC-A   PC-B   PC-C
        |
     Frame Arrives

↓

Sent To

PC-B ✅

PC-C ✅

Not Sent Back To PC-A
```

Only PC-B accepts the frame.

PC-C simply ignores it.

---

# Step 4 – Learn the New MAC Address

When PC-B replies,

```text
PC-B

↓

Reply

↓

Switch
```

The Switch learns:

```text
BB:BB:BB:BB:BB:BB

↓

Port 2
```

Now both MAC addresses are stored.

Future communication becomes much faster.

---

# Complete Switching Process

```text
PC-A

↓

Frame Sent

↓

Switch Receives Frame

↓

Learn Source MAC

↓

Check Destination MAC

↓

Known?

↓

Yes

↓

Forward to Correct Port

↓

PC-B Receives Data
```

---

# Unknown Destination Flow

```text
PC-A

↓

Frame

↓

Switch

↓

Destination Unknown

↓

Flood

↓

All Ports Except Source
```

Once the destination replies,

the Switch learns its MAC address.

Future frames are forwarded directly.

---

# Filtering

Suppose the destination MAC Address is already known.

Instead of flooding,

the Switch forwards the frame only to one port.

This process is called **Filtering**.

```text
Known Destination

↓

Correct Port

↓

Frame Delivered
```

Filtering reduces unnecessary traffic.

---

# MAC Learning Process

Every time a device sends data,

the Switch learns:

```text
Source MAC

↓

Incoming Port

↓

Store in CAM Table
```

Example

```text
MAC Address

AA:AA:AA:AA:AA:AA

↓

Port 1

MAC Address

BB:BB:BB:BB:BB:BB

↓

Port 2

MAC Address

CC:CC:CC:CC:CC:CC

↓

Port 3
```

The table keeps growing as devices communicate.

---

# Real-Life Analogy 📦

Imagine a courier office.

Day 1

The courier doesn't know anyone's address.

So he asks around.

```text
Package

↓

Every House
```

Eventually,

he learns where everyone lives.

Day 2

```text
Package

↓

Correct House
```

No unnecessary deliveries.

A Switch behaves exactly the same way.

---

# AWS Perspective ☁️

Suppose two EC2 instances exist in the same subnet.

```text
EC2-A

↓

AWS Virtual Network

↓

EC2-B
```

AWS maintains virtual networking information behind the scenes.

Instead of physical switch ports,

AWS uses virtual networking constructs to forward traffic efficiently between instances.

The concept remains the same:

- Learn the destination.
- Forward traffic only where needed.

---

# Real AWS Scenario

Suppose you have:

```text
EC2-A

10.0.1.10

↓

EC2-B

10.0.1.20
```

Both instances are in the same subnet.

Traffic flow:

```text
EC2-A

↓

Virtual Switch

↓

EC2-B
```

No unnecessary traffic reaches other instances.

Communication is efficient and secure.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"A Switch always floods frames."**

✅ **Correct:**

Flooding happens only when the destination MAC Address is unknown.

---

## ❌ Mistake 2

**"Switches learn Destination MAC Addresses."**

✅ **Correct:**

Switches learn **Source MAC Addresses** from incoming frames.

---

## ❌ Mistake 3

**"Flooding sends frames back to the source port."**

✅ **Correct:**

Flooding sends frames to all ports **except** the incoming port.

---

## ❌ Mistake 4

**"Switches always know every MAC Address."**

✅ **Correct:**

A Switch builds its MAC Address Table dynamically as devices communicate.

---

# 📝 Quick Revision

- Switch receives an Ethernet Frame.
- Learns the Source MAC Address.
- Checks the Destination MAC Address.
- If known → Forward.
- If unknown → Flood.
- Learns MAC Addresses dynamically.
- Future communication becomes faster.

---

# 💼 Interview Questions

### 1. What happens first when a Switch receives a frame?

**Answer:**

The Switch receives the Ethernet frame and reads the Source and Destination MAC Addresses.

---

### 2. How does a Switch learn MAC Addresses?

**Answer:**

The Switch learns the **Source MAC Address** from incoming frames and stores it in the CAM (MAC Address) Table along with the port number.

---

### 3. What is Flooding?

**Answer:**

Flooding is the process of sending a frame to all switch ports except the incoming port when the destination MAC Address is unknown.

---

### 4. What is Filtering?

**Answer:**

Filtering is the process of forwarding a frame only to the correct destination port when the destination MAC Address is already present in the CAM Table.

---

### 5. Does a Switch learn Source or Destination MAC Addresses?

**Answer:**

A Switch learns **Source MAC Addresses**, not Destination MAC Addresses.

---

### 6. How does AWS perform switching?

**Answer:**

AWS performs switching using virtual networking inside Amazon VPCs. Traffic between EC2 instances is forwarded efficiently using virtual networking technologies rather than physical switches.

---
