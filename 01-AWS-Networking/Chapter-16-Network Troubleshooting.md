# 1. Introduction to Network Troubleshooting

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand Network Troubleshooting.
- Learn why troubleshooting is important.
- Understand the troubleshooting process.
- Identify common network issues.
- Learn troubleshooting in AWS.
- Answer troubleshooting interview questions confidently.

---

# 📖 Introduction

Imagine you are watching YouTube.

Suddenly,

the video stops loading.

You ask yourself:

- Is the Internet working?
- Is Wi-Fi connected?
- Is the router working?
- Is YouTube down?

This process of finding and fixing the problem is called:

```text
Network Troubleshooting
```

Network Troubleshooting is one of the most important skills for a Cloud Engineer, Network Engineer, and AWS Support Engineer.

---

# What is Network Troubleshooting?

**Network Troubleshooting** is the process of identifying, analyzing, and resolving network-related problems to restore normal communication.

The goal is to find the root cause and fix it as quickly as possible.

---

# Definition

**Network Troubleshooting** is the systematic process of detecting, diagnosing, and resolving problems affecting network connectivity, performance, or communication.

---

# Why is Network Troubleshooting Important?

Without troubleshooting,

organizations may face:

- Internet Outages
- Application Downtime
- Slow Network Performance
- Communication Failure
- Business Loss

Quick troubleshooting minimizes downtime and restores services faster.

---

# Goals of Network Troubleshooting

The main goals are:

- Identify the Root Cause
- Restore Network Connectivity
- Minimize Downtime
- Improve Performance
- Prevent Future Issues

---

# Common Network Problems

Network Engineers commonly troubleshoot:

- No Internet Connection
- Slow Internet
- High Latency
- Packet Loss
- DNS Issues
- IP Address Conflicts
- Routing Problems
- Firewall Blocking Traffic
- VPN Connectivity Issues
- Hardware Failures

---

# Common Causes

Problems may occur because of:

- Faulty Network Cable
- Router Failure
- Switch Failure
- Wrong IP Address
- Incorrect Gateway
- DNS Failure
- Firewall Rules
- Security Group Rules
- Route Table Issues
- ISP Problems

---

# Basic Troubleshooting Flow

```text
Problem Reported

↓

Identify Problem

↓

Collect Information

↓

Analyze Cause

↓

Fix Problem

↓

Test Solution

↓

Document Issue
```

Always troubleshoot step by step.

---

# Network Troubleshooting Process

A good engineer follows this approach:

```text
Identify

↓

Verify

↓

Diagnose

↓

Resolve

↓

Test

↓

Monitor
```

Avoid guessing.

Always verify each step.

---

# Real-Life Analogy 🚗

Imagine your car does not start.

You don't immediately replace the engine.

Instead, you check:

```text
Fuel

↓

Battery

↓

Starter

↓

Engine
```

Similarly,

a Network Engineer checks every component before deciding the root cause.

---

# AWS Perspective ☁️

Cloud Engineers troubleshoot issues involving:

- Amazon VPC
- Security Groups
- Network ACLs
- Route Tables
- Internet Gateway
- NAT Gateway
- VPN
- Route 53
- VPC Flow Logs

AWS also provides tools like:

- CloudWatch
- CloudTrail
- VPC Flow Logs
- Reachability Analyzer

to help diagnose network issues.

---

# Real AWS Scenario

Suppose users cannot access an EC2 web server.

Architecture

```text
Internet

↓

Internet Gateway

↓

Route Table

↓

Security Group

↓

EC2
```

Possible Causes

- Internet Gateway not attached
- Missing Route
- Security Group blocks Port 80
- NACL blocks traffic
- EC2 stopped
- Web server service not running

A Cloud Engineer checks each component one by one.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Restarting the server fixes every network issue."**

✅ **Correct:**

Restarting may temporarily help, but proper troubleshooting identifies and resolves the actual root cause.

---

## ❌ Mistake 2

**"Every connectivity issue is caused by the Internet."**

✅ **Correct:**

Problems may be related to DNS, routing, firewalls, VPNs, IP configuration, or AWS networking components.

---

## ❌ Mistake 3

**"Troubleshooting means trying random fixes."**

✅ **Correct:**

Troubleshooting should follow a structured methodology to identify the root cause efficiently.

---

## ❌ Mistake 4

**"If an EC2 instance is running, the application must be working."**

✅ **Correct:**

The instance may be running, but Security Groups, Route Tables, NACLs, the web server, or DNS configuration could still prevent access.

---

# 📝 Quick Revision

- Network Troubleshooting finds and fixes network problems.
- Follow a structured troubleshooting process.
- Identify the root cause before applying a fix.
- Common issues include DNS, routing, firewall, VPN, and IP configuration.
- AWS troubleshooting often involves VPC, Security Groups, Route Tables, NAT Gateway, and Internet Gateway.

---

# 💼 Interview Questions

### 1. What is Network Troubleshooting?

**Answer:**

Network Troubleshooting is the systematic process of identifying, diagnosing, and resolving network problems to restore normal connectivity and performance.

---

### 2. Why is Network Troubleshooting important?

**Answer:**

It helps minimize downtime, restore services quickly, improve network performance, and identify the root cause of problems.

---

### 3. What are some common network problems?

**Answer:**

Common problems include:

- No Internet connection
- Slow network
- DNS failures
- IP conflicts
- Routing issues
- Firewall blocks
- VPN connectivity issues
- Hardware failures

---

### 4. What is the first step in troubleshooting?

**Answer:**

The first step is to identify and understand the problem by gathering information about the issue before making any changes.

---

### 5. Which AWS services are commonly checked during network troubleshooting?

**Answer:**

Common AWS networking components include:

- Amazon VPC
- Security Groups
- Network ACLs
- Route Tables
- Internet Gateway
- NAT Gateway
- Route 53
- VPC Flow Logs

---

### 6. Why should engineers follow a troubleshooting methodology?

**Answer:**

A structured methodology helps identify the root cause efficiently, reduces downtime, prevents unnecessary changes, and ensures issues are resolved correctly.

---

# 2. Troubleshooting Methodology

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand the Network Troubleshooting Methodology.
- Learn the standard troubleshooting process.
- Identify the root cause of network problems.
- Apply troubleshooting in AWS environments.
- Answer troubleshooting interview questions confidently.

---

# 📖 Introduction

Suppose a user reports:

> **"I cannot access the company website."**

Should you immediately restart the server?

❌ No.

Professional Network Engineers follow a structured troubleshooting methodology instead of guessing.

A systematic approach helps identify the real problem quickly and reduces downtime.

---

# What is a Troubleshooting Methodology?

A **Troubleshooting Methodology** is a step-by-step process used to identify, diagnose, resolve, and verify network problems.

It helps engineers solve issues efficiently without making unnecessary changes.

---

# Standard Troubleshooting Process

```text
Identify Problem

↓

Collect Information

↓

Analyze the Cause

↓

Create a Solution

↓

Implement the Fix

↓

Test the Solution

↓

Document the Issue
```

---

# Step 1 – Identify the Problem

Understand exactly what the user is experiencing.

Ask questions such as:

- What is the issue?
- When did it start?
- Is everyone affected?
- Is only one application affected?
- Were any recent changes made?

Never assume the problem.

---

# Step 2 – Collect Information

Gather information before making changes.

Check:

- IP Address
- Internet Connectivity
- Device Status
- Router Status
- Switch Status
- Firewall Rules
- DNS Configuration

Use tools like:

- Ping
- Traceroute
- ipconfig / ifconfig
- nslookup

---

# Step 3 – Analyze the Cause

Analyze all collected information.

Possible causes include:

- Cable Failure
- Wrong IP Address
- DNS Failure
- Firewall Block
- Route Table Issue
- VPN Failure
- Security Group Misconfiguration

Focus on identifying the **root cause**, not just the symptoms.

---

# Step 4 – Create a Solution

Choose the safest solution.

Example

Problem

```text
Wrong Default Gateway
```

Solution

```text
Configure Correct Gateway
```

Always evaluate the impact before implementing changes.

---

# Step 5 – Implement the Fix

Apply the selected solution.

Examples

- Restart a Service
- Correct Firewall Rules
- Update Route Table
- Replace Faulty Cable
- Fix DNS Configuration

Avoid making multiple changes at the same time.

---

# Step 6 – Test the Solution

Verify that the problem has been resolved.

Example

```bash
ping google.com
```

or

```bash
curl https://example.com
```

Confirm that users can access the required resources.

---

# Step 7 – Document the Issue

Record:

- Problem Description
- Root Cause
- Solution Applied
- Date & Time
- Engineer Name

Documentation helps with future troubleshooting and knowledge sharing.

---

# Troubleshooting Flow

```text
Problem Reported

↓

Identify

↓

Collect Information

↓

Analyze

↓

Fix

↓

Test

↓

Document
```

---

# Example Scenario

Problem

```text
User Cannot Access Website
```

Troubleshooting Steps

```text
Check Internet

↓

Ping Website

↓

Check DNS

↓

Check Firewall

↓

Check Web Server

↓

Website Restored
```

---

# Real-Life Analogy 🚑

Imagine a doctor treating a patient.

The doctor does not immediately perform surgery.

Instead, the doctor:

```text
Ask Symptoms

↓

Examine Patient

↓

Run Tests

↓

Find Cause

↓

Give Treatment

↓

Check Recovery
```

Network Engineers follow the same logical process.

---

# AWS Perspective ☁️

In AWS, troubleshooting usually involves checking:

- EC2 Instance Status
- Security Groups
- Network ACLs
- Route Tables
- Internet Gateway
- NAT Gateway
- VPC Flow Logs
- Route 53
- CloudWatch
- CloudTrail

Example

```text
User Cannot Access EC2

↓

EC2 Running?

↓

Security Group OK?

↓

Route Table OK?

↓

Internet Gateway Attached?

↓

Application Running?
```

---

# Real AWS Scenario

Suppose users cannot access a web application.

Architecture

```text
Internet

↓

Internet Gateway

↓

Public Subnet

↓

EC2
```

Troubleshooting

```text
EC2 Running

✅

↓

Security Group

Port 80 Closed

❌

↓

Allow HTTP

↓

Website Accessible
```

The issue was the Security Group, not the EC2 instance.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Restart everything first."**

✅ **Correct:**

Always identify the root cause before restarting or changing configurations.

---

## ❌ Mistake 2

**"Make multiple configuration changes together."**

✅ **Correct:**

Apply one change at a time so you can easily identify what resolved the issue.

---

## ❌ Mistake 3

**"Once the issue is fixed, documentation is unnecessary."**

✅ **Correct:**

Documentation is important for future troubleshooting, audits, and knowledge sharing.

---

## ❌ Mistake 4

**"The user's description is always the actual problem."**

✅ **Correct:**

Gather evidence and verify the issue before deciding on the root cause.

---

# 📝 Quick Revision

- Follow a structured troubleshooting methodology.
- Identify the problem first.
- Collect relevant information.
- Analyze the root cause.
- Apply one solution at a time.
- Test after implementing the fix.
- Document the issue and resolution.
- AWS troubleshooting commonly involves VPC, Security Groups, Route Tables, and CloudWatch.

---

# 💼 Interview Questions

### 1. What is a troubleshooting methodology?

**Answer:**

A troubleshooting methodology is a structured process used to identify, diagnose, resolve, and verify network problems efficiently.

---

### 2. What is the first step in troubleshooting?

**Answer:**

The first step is to identify and understand the problem by gathering accurate information from the user or monitoring tools.

---

### 3. Why is documentation important after resolving an issue?

**Answer:**

Documentation records the problem, root cause, and solution, making future troubleshooting faster and improving knowledge sharing.

---

### 4. Why should you make one configuration change at a time?

**Answer:**

Making one change at a time helps identify which change resolved the issue and reduces the risk of introducing new problems.

---

### 5. Which AWS components are commonly checked during troubleshooting?

**Answer:**

Common AWS components include:

- EC2
- Amazon VPC
- Security Groups
- Network ACLs
- Route Tables
- Internet Gateway
- NAT Gateway
- Route 53
- CloudWatch
- VPC Flow Logs

---

### 6. What is the goal of network troubleshooting?

**Answer:**

The goal is to identify the root cause of a problem, restore normal network operation, minimize downtime, and prevent similar issues in the future.

---

# 3. OSI Layer Approach

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand the OSI Layer troubleshooting approach.
- Learn how to troubleshoot layer by layer.
- Identify common issues at each OSI layer.
- Understand OSI troubleshooting in AWS.
- Answer OSI troubleshooting interview questions confidently.

---

# 📖 Introduction

Imagine a building with seven floors.

If the lift stops working,

you don't immediately assume the problem is on the 7th floor.

Instead,

you check each floor one by one.

The OSI model works the same way.

Network Engineers troubleshoot from one OSI layer to another until they find the actual problem.

---

# Why Use the OSI Model for Troubleshooting?

The OSI model divides networking into seven layers.

By checking each layer individually,

you can quickly identify where the problem exists.

Benefits:

- Faster Troubleshooting
- Easier Root Cause Analysis
- Logical Approach
- Industry Standard

---

# OSI Layers

```text
7 → Application

6 → Presentation

5 → Session

4 → Transport

3 → Network

2 → Data Link

1 → Physical
```

---

# Layer 1 – Physical Layer

This layer deals with:

- Network Cable
- Fiber Cable
- Switch Port
- Router Port
- Network Card (NIC)
- Power Supply

---

## Common Problems

- Broken Cable
- Loose Cable
- Damaged NIC
- Switch Power Failure
- Router Power Failure

---

## Troubleshooting

Check:

- Cable Connection
- LED Status
- Power Supply
- Network Adapter

---

# Layer 2 – Data Link Layer

Responsible for:

- MAC Address
- Ethernet Frame
- Switching
- VLAN

---

## Common Problems

- Wrong VLAN
- MAC Address Conflict
- Switch Port Disabled
- STP Blocking Port

---

## Troubleshooting

Check:

- VLAN Configuration
- Switch Port Status
- MAC Address Table

---

# Layer 3 – Network Layer

Responsible for:

- IP Address
- Routing
- Routers
- Packet Forwarding

---

## Common Problems

- Wrong IP Address
- Wrong Gateway
- Missing Route
- Routing Loop

---

## Troubleshooting

Commands

```bash
ipconfig

ifconfig

ping

traceroute
```

Check:

- IP Address
- Gateway
- Route Table

---

# Layer 4 – Transport Layer

Responsible for:

- TCP
- UDP
- Port Numbers

---

## Common Problems

- Closed Port
- Firewall Blocking
- TCP Handshake Failure

---

## Troubleshooting

Check:

- Firewall Rules
- Security Groups
- Open Ports

Commands

```bash
netstat
```

---

# Layer 5 – Session Layer

Responsible for:

- Session Management
- Login Sessions
- Authentication Sessions

---

## Common Problems

- Session Timeout
- Authentication Failure
- Login Issues

---

## Troubleshooting

Check:

- Session Logs
- Authentication Service
- Credentials

---

# Layer 6 – Presentation Layer

Responsible for:

- Encryption
- Compression
- Data Formatting

---

## Common Problems

- SSL Certificate Error
- TLS Handshake Failure
- Encryption Mismatch

---

## Troubleshooting

Check:

- SSL Certificate
- TLS Version
- Encryption Settings

---

# Layer 7 – Application Layer

Responsible for:

- Web Browser
- Email
- FTP
- DNS
- HTTP
- HTTPS

---

## Common Problems

- Website Not Loading
- DNS Failure
- Application Crash
- Email Failure

---

## Troubleshooting

Check:

- Application Logs
- DNS
- Web Server
- Browser

---

# OSI Troubleshooting Flow

```text
Application Problem

↓

Layer 7

↓

Layer 6

↓

Layer 5

↓

Layer 4

↓

Layer 3

↓

Layer 2

↓

Layer 1
```

Or,

if you suspect a hardware issue,

start from Layer 1 and move upward.

---

# Common OSI Troubleshooting Examples

| Problem | Possible OSI Layer |
|----------|-------------------|
| Cable Broken | Layer 1 |
| Wrong VLAN | Layer 2 |
| Wrong IP Address | Layer 3 |
| Port Blocked | Layer 4 |
| Login Failure | Layer 5 |
| SSL Error | Layer 6 |
| Website Not Loading | Layer 7 |

---

# Real-Life Analogy 🏢

Imagine sending a parcel.

```text
Parcel Packed

↓

Truck

↓

Road

↓

City

↓

Receiver
```

If the parcel doesn't arrive,

you check every stage one by one.

Similarly,

Network Engineers check every OSI layer until they find the issue.

---

# AWS Perspective ☁️

AWS troubleshooting can also be mapped to OSI layers.

| OSI Layer | AWS Example |
|------------|-------------|
| Layer 1 | AWS manages physical infrastructure |
| Layer 2 | ENI, MAC Address |
| Layer 3 | VPC, Route Tables, IP Address |
| Layer 4 | Security Groups, NACL, TCP/UDP |
| Layer 5 | Authentication Sessions |
| Layer 6 | SSL/TLS Certificates, AWS ACM |
| Layer 7 | ALB, Route 53, Web Applications |

---

# Real AWS Scenario

Users cannot access:

```text
https://company.com
```

Troubleshooting

```text
Application Running?

↓

SSL Certificate Valid?

↓

Security Group Port 443 Open?

↓

Route Table Correct?

↓

Internet Gateway Attached?

↓

EC2 Running?
```

Following the OSI model helps identify the exact layer where the issue occurs.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Every network issue starts at Layer 3."**

✅ **Correct:**

Problems can occur at **any OSI layer**, from a loose cable (Layer 1) to an application error (Layer 7).

---

## ❌ Mistake 2

**"Website not loading always means DNS failure."**

✅ **Correct:**

The issue could also be the web server, Security Groups, Route Tables, SSL certificates, or the application itself.

---

## ❌ Mistake 3

**"Firewall problems belong to Layer 3."**

✅ **Correct:**

Traditional firewalls often inspect traffic at **Layer 3 and Layer 4**, while Web Application Firewalls (AWS WAF) operate at **Layer 7**.

---

## ❌ Mistake 4

**"AWS engineers don't use the OSI model."**

✅ **Correct:**

AWS networking issues are commonly diagnosed using the OSI model because AWS services map closely to different networking layers.

---

# 📝 Quick Revision

- OSI Model helps troubleshoot logically.
- Layer 1 → Physical Devices & Cables.
- Layer 2 → MAC Address & VLAN.
- Layer 3 → IP Address & Routing.
- Layer 4 → TCP, UDP & Ports.
- Layer 5 → Sessions.
- Layer 6 → SSL/TLS & Encryption.
- Layer 7 → Applications & DNS.
- AWS services map across multiple OSI layers.

---

# 💼 Interview Questions

### 1. Why is the OSI model used for troubleshooting?

**Answer:**

The OSI model provides a structured, layer-by-layer approach to identify the exact location of a network problem, making troubleshooting faster and more efficient.

---

### 2. Which OSI layer is responsible for IP addressing?

**Answer:**

**Layer 3 (Network Layer)** is responsible for IP addressing, routing, and packet forwarding.

---

### 3. Which OSI layer handles TCP and UDP?

**Answer:**

**Layer 4 (Transport Layer)** handles TCP, UDP, port numbers, and reliable communication.

---

### 4. Which OSI layer is responsible for SSL/TLS?

**Answer:**

**Layer 6 (Presentation Layer)** is associated with encryption, decryption, and SSL/TLS functionality.

---

### 5. Which AWS services are commonly related to Layer 3 and Layer 4 troubleshooting?

**Answer:**

- **Layer 3:** Amazon VPC, Route Tables, Internet Gateway.
- **Layer 4:** Security Groups, Network ACLs, TCP/UDP ports.

---

### 6. A website is not loading. Which OSI layers should you check?

**Answer:**

Check:

- Layer 7 → Web application and DNS
- Layer 6 → SSL/TLS certificate
- Layer 4 → Open ports and Security Groups
- Layer 3 → IP addressing and routing
- Layer 1 & 2 → Physical connectivity (if applicable)

---

# 4. Common Network Problems

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand common network problems.
- Identify the causes of network issues.
- Learn how to troubleshoot common problems.
- Understand common AWS networking issues.
- Answer troubleshooting interview questions confidently.

---

# 📖 Introduction

Imagine you arrive at work and employees complain:

- "Internet is not working."
- "The website is very slow."
- "We cannot access the server."
- "VPN is disconnected."

As a Network or Cloud Engineer,

your job is to identify the problem quickly and restore the network.

Knowing the most common network problems helps reduce downtime and improve troubleshooting.

---

# Common Network Problems

The most common problems are:

```text
Network Problems

│

├── No Internet Connection

├── Slow Network

├── DNS Failure

├── IP Address Conflict

├── Packet Loss

├── High Latency

├── Routing Issues

├── Firewall Blocking

├── VPN Failure

└── Hardware Failure
```

---

# 1. No Internet Connection

Users cannot access:

- Websites
- Email
- Cloud Applications

---

## Possible Causes

- ISP Outage
- Router Failure
- Incorrect Gateway
- DNS Failure
- Network Cable Disconnected
- Wi-Fi Disabled

---

## Troubleshooting

Check:

- Network Cable
- Wi-Fi Connection
- Router Status
- Default Gateway
- Internet Connectivity

Command

```bash
ping 8.8.8.8
```

---

# 2. Slow Network

The network works,

but applications respond slowly.

---

## Possible Causes

- High Bandwidth Usage
- Congestion
- Hardware Overload
- Weak Wi-Fi Signal
- Malware

---

## Troubleshooting

Check:

- Bandwidth Usage
- CPU & Memory
- Switch Utilization
- Router Load
- Internet Speed

---

# 3. DNS Failure

Users cannot open websites using domain names.

Example

```bash
ping google.com

❌ Failed
```

But

```bash
ping 8.8.8.8

✅ Success
```

Internet works,

but DNS is failing.

---

## Troubleshooting

Commands

```bash
nslookup google.com
```

Check:

- DNS Server
- Route 53 Resolver
- DHCP Configuration

---

# 4. IP Address Conflict

Two devices have the same IP address.

Result

```text
PC A

192.168.1.10
```

```text
PC B

192.168.1.10
```

Communication becomes unreliable.

---

## Troubleshooting

Check:

- DHCP Server
- Static IP Configuration
- IP Address Allocation

Command

```bash
ipconfig
```

---

# 5. Packet Loss

Some packets never reach the destination.

Example

```text
100 Packets Sent

↓

92 Received

↓

8 Lost
```

---

## Possible Causes

- Bad Cable
- Congestion
- Faulty Router
- Wireless Interference

---

## Troubleshooting

Commands

```bash
ping

traceroute
```

Replace faulty hardware if necessary.

---

# 6. High Latency

Latency is the time required for a packet to travel from source to destination.

Example

```text
Ping

20 ms

✅ Good
```

```text
Ping

300 ms

❌ High Latency
```

---

## Possible Causes

- Long Distance
- Network Congestion
- Routing Problems
- ISP Issues

---

## Troubleshooting

Use

```bash
ping

traceroute
```

Identify where the delay occurs.

---

# 7. Routing Issues

Packets cannot reach the destination because of incorrect routing.

Example

```text
PC

↓

Router

↓

Wrong Route

↓

Packet Dropped
```

---

## Troubleshooting

Check:

- Route Table
- Default Gateway
- Router Configuration

Command

```bash
route
```

---

# 8. Firewall Blocking

Firewall blocks legitimate traffic.

Example

```text
Port 80

↓

Blocked

↓

Website Not Accessible
```

---

## Troubleshooting

Check:

- Firewall Rules
- Security Groups
- Network ACLs

Verify required ports are open.

---

# 9. VPN Failure

Users cannot access company resources securely.

---

## Possible Causes

- Tunnel Down
- Authentication Failure
- Incorrect Pre-Shared Key
- BGP Routing Issue

---

## Troubleshooting

Check:

- VPN Tunnel Status
- Credentials
- Route Tables
- Customer Gateway

---

# 10. Hardware Failure

Hardware issues include:

- Faulty Router
- Broken Switch
- Damaged NIC
- Loose Cable
- Power Failure

---

## Troubleshooting

Check:

- Power Supply
- Cable Connections
- Link Lights
- Hardware Status

Replace faulty equipment if required.

---

# Common Problems & Solutions

| Problem | Common Solution |
|----------|-----------------|
| No Internet | Check ISP, Gateway, Cable |
| Slow Network | Check Bandwidth & Congestion |
| DNS Failure | Verify DNS Server |
| IP Conflict | Correct IP Configuration |
| Packet Loss | Replace Cable / Check Router |
| High Latency | Trace Route & Check Network |
| Routing Issue | Verify Route Table |
| Firewall Block | Review Firewall Rules |
| VPN Failure | Verify Tunnel & Authentication |
| Hardware Failure | Replace Faulty Device |

---

# Real-Life Analogy 🚗

Imagine driving to work.

Possible problems:

```text
Road Closed

↓

Routing Issue
```

---

```text
Traffic Jam

↓

High Latency
```

---

```text
Wrong Address

↓

DNS Problem
```

---

```text
Police Checkpoint

↓

Firewall
```

Each issue affects your journey differently.

---

# AWS Perspective ☁️

Common AWS networking issues include:

- Internet Gateway Not Attached
- Incorrect Route Table
- Security Group Blocking Traffic
- Network ACL Deny Rule
- NAT Gateway Failure
- Route 53 DNS Issue
- VPN Tunnel Down
- Elastic IP Not Associated

Cloud Engineers troubleshoot these regularly.

---

# Real AWS Scenario

Users cannot access an EC2 web server.

Architecture

```text
Internet

↓

Internet Gateway

↓

Route Table

↓

Security Group

↓

EC2
```

Troubleshooting

```text
EC2 Running

✅

↓

Route Table Correct

✅

↓

Security Group

Port 80 Closed

❌

↓

Allow HTTP

↓

Website Accessible
```

The issue was a missing Security Group rule.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"If Ping fails, the server is down."**

✅ **Correct:**

Ping can fail because ICMP is blocked by a firewall or Security Group. The server may still be running.

---

## ❌ Mistake 2

**"DNS problems mean the Internet is down."**

✅ **Correct:**

If you can ping an IP address but not a domain name, the issue is DNS—not Internet connectivity.

---

## ❌ Mistake 3

**"High latency and packet loss are the same."**

✅ **Correct:**

High latency means packets arrive slowly, while packet loss means packets never arrive.

---

## ❌ Mistake 4

**"If EC2 is running, users should always be able to access it."**

✅ **Correct:**

Access may still fail due to Security Groups, Network ACLs, Route Tables, Internet Gateway, or application issues.

---

# 📝 Quick Revision

- No Internet → Check ISP, Gateway, Cable.
- Slow Network → Check Congestion.
- DNS Failure → Check DNS Server.
- IP Conflict → Verify IP Address.
- Packet Loss → Check Network Hardware.
- High Latency → Use Ping & Traceroute.
- Routing Issue → Check Route Tables.
- Firewall Block → Review Rules.
- VPN Failure → Verify Tunnel.
- Hardware Failure → Inspect Devices.

---

# 💼 Interview Questions

### 1. What are the most common network problems?

**Answer:**

Common network problems include:

- No Internet Connection
- Slow Network
- DNS Failure
- IP Address Conflict
- Packet Loss
- High Latency
- Routing Issues
- Firewall Blocking
- VPN Failure
- Hardware Failure

---

### 2. How do you identify a DNS problem?

**Answer:**

If you can ping an IP address (such as `8.8.8.8`) but cannot ping a domain name (such as `google.com`), the issue is likely DNS.

---

### 3. What causes packet loss?

**Answer:**

Packet loss can be caused by faulty cables, network congestion, damaged hardware, wireless interference, or routing issues.

---

### 4. What is high latency?

**Answer:**

High latency is a delay in packet transmission between the source and destination, often caused by congestion, long distances, or routing problems.

---

### 5. What AWS networking issues are commonly seen?

**Answer:**

Common AWS networking issues include:

- Missing Internet Gateway
- Incorrect Route Tables
- Security Group Misconfiguration
- Network ACL Rules
- NAT Gateway Problems
- Route 53 DNS Issues
- VPN Tunnel Failures

---

### 6. Which AWS component commonly blocks traffic to an EC2 instance?

**Answer:**

Traffic is commonly blocked by:

- **Security Groups**
- **Network ACLs (NACLs)**

Both should be checked during troubleshooting.

---

# 5. Ping Command

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand the Ping command.
- Learn how Ping works.
- Interpret Ping results.
- Troubleshoot network connectivity using Ping.
- Understand Ping in AWS.
- Answer Ping interview questions confidently.

---

# 📖 Introduction

Imagine you call your friend.

If your friend answers,

you know they are available.

If there is no answer,

either:

- They are busy.
- Their phone is switched off.
- There is a network problem.

The **Ping** command works in the same way.

It checks whether a device is reachable on the network.

---

# What is Ping?

**Ping** is a network troubleshooting command used to test whether a remote device is reachable over an IP network.

It also measures the time required for packets to travel between devices.

---

# Definition

**Ping** is a network utility that sends **ICMP Echo Request** packets to a destination and waits for **ICMP Echo Reply** packets.

---

# How Ping Works

```text
Computer

↓

ICMP Echo Request

↓

Destination Device

↓

ICMP Echo Reply

↓

Computer
```

If a reply is received,

the destination is reachable.

---

# ICMP

Ping uses:

```text
ICMP

Internet Control Message Protocol
```

ICMP is used for:

- Network Diagnostics
- Error Reporting
- Connectivity Testing

---

# Basic Ping Syntax

### Windows

```bash
ping google.com
```

---

### Linux

```bash
ping google.com
```

Linux sends continuous ping requests until stopped using:

```bash
Ctrl + C
```

---

# Ping Using IP Address

Example

```bash
ping 8.8.8.8
```

If successful,

the network connection is working.

---

# Ping Using Domain Name

Example

```bash
ping google.com
```

This tests:

- DNS Resolution
- Network Connectivity

If this fails but pinging an IP works,

the issue is likely DNS.

---

# Successful Ping Example

```text
Reply from 8.8.8.8

Bytes=32

Time=18ms

TTL=118
```

Meaning

- Destination Reachable
- Low Latency
- Network Working Properly

---

# Failed Ping Example

```text
Request Timed Out
```

Possible Causes

- Device Offline
- Firewall Blocking ICMP
- Wrong IP Address
- Network Failure

---

# Common Ping Responses

| Response | Meaning |
|-----------|---------|
| Reply from... | Destination Reachable |
| Request Timed Out | No Reply Received |
| Destination Host Unreachable | Route Not Found |
| Unknown Host | DNS Failure |

---

# Understanding Ping Output

Example

```text
Reply from 8.8.8.8

Bytes=32

Time=20ms

TTL=117
```

### Bytes

Amount of data sent.

---

### Time

Round Trip Time (RTT)

Lower value

↓

Better Performance

---

### TTL

Time To Live

Prevents packets from looping forever in a network.

---

# Ping Troubleshooting

Scenario 1

```bash
ping 8.8.8.8

✅ Success
```

```bash
ping google.com

❌ Failed
```

Problem

↓

DNS Issue

---

Scenario 2

```bash
ping 192.168.1.1

❌ Failed
```

Problem

↓

Router

↓

Gateway

↓

Cable

---

Scenario 3

```bash
ping Server

Request Timed Out
```

Possible Causes

- Firewall
- Server Down
- Network Failure

---

# Useful Ping Options

### Windows

Send only 5 packets

```bash
ping -n 5 google.com
```

---

### Linux

Send only 5 packets

```bash
ping -c 5 google.com
```

---

# Ping in AWS

Suppose an EC2 instance cannot be reached.

Architecture

```text
Laptop

↓

Internet

↓

Internet Gateway

↓

EC2
```

Possible Causes

- Security Group blocks ICMP
- Network ACL blocks ICMP
- Route Table Issue
- Instance Stopped

---

# AWS Example

Security Group

```text
Inbound Rule

↓

ICMP

↓

Allow
```

If ICMP is blocked,

Ping will fail,

even if the EC2 instance is running.

---

# Real-Life Analogy 📞

Imagine making a phone call.

```text
You Call

↓

Friend Answers

↓

Reachable
```

If no one answers,

the phone may be switched off,

or there may be a network issue.

Ping works the same way.

---

# AWS Perspective ☁️

Cloud Engineers use Ping to:

- Verify Network Connectivity
- Test Reachability
- Identify DNS Issues
- Check Gateway Connectivity
- Troubleshoot EC2 Access

However,

some AWS resources intentionally block ICMP,

so a failed Ping does not always mean the resource is unavailable.

---

# Real AWS Scenario

Users cannot access an EC2 instance.

Troubleshooting

```text
Ping Public IP

↓

Failed

↓

Check Security Group

↓

ICMP Blocked

↓

Allow ICMP

↓

Ping Successful
```

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"If Ping fails, the server is down."**

✅ **Correct:**

The server may still be running. ICMP traffic might be blocked by a firewall, Security Group, or Network ACL.

---

## ❌ Mistake 2

**"Ping uses TCP."**

✅ **Correct:**

Ping uses **ICMP**, not TCP or UDP.

---

## ❌ Mistake 3

**"Ping tests application availability."**

✅ **Correct:**

Ping tests basic network reachability. It does not confirm that services such as HTTP or SSH are working.

---

## ❌ Mistake 4

**"If Ping to an IP works, DNS is also working."**

✅ **Correct:**

Pinging an IP only confirms network connectivity. To verify DNS, ping or resolve a domain name.

---

# 📝 Quick Revision

- Ping checks network connectivity.
- Uses ICMP Echo Request and Echo Reply.
- Tests whether a host is reachable.
- Can identify DNS issues.
- Measures Round Trip Time (RTT).
- Common responses:
  - Reply
  - Request Timed Out
  - Destination Host Unreachable
- AWS Security Groups and NACLs can block ICMP.

---

# 💼 Interview Questions

### 1. What is the Ping command?

**Answer:**

Ping is a network troubleshooting utility that uses ICMP Echo Request and Echo Reply messages to verify whether a remote device is reachable.

---

### 2. Which protocol does Ping use?

**Answer:**

Ping uses the **Internet Control Message Protocol (ICMP)**.

---

### 3. What does "Request Timed Out" mean?

**Answer:**

It means no reply was received from the destination. Possible causes include a firewall blocking ICMP, a network issue, or the destination device being unavailable.

---

### 4. What is the difference between `ping 8.8.8.8` and `ping google.com`?

**Answer:**

- `ping 8.8.8.8` tests basic network connectivity.
- `ping google.com` tests both **DNS resolution** and network connectivity.

---

### 5. Why might an EC2 instance not respond to Ping?

**Answer:**

Possible reasons include:

- ICMP blocked by the Security Group
- ICMP blocked by the Network ACL
- Incorrect Route Table
- Internet Gateway issues
- The EC2 instance is stopped

---

### 6. What does RTT (Round Trip Time) indicate?

**Answer:**

RTT is the time taken for a packet to travel from the source to the destination and back. Lower RTT values generally indicate better network performance.

---

# 6. Traceroute Command

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand the Traceroute command.
- Learn how Traceroute works.
- Interpret Traceroute results.
- Troubleshoot routing problems using Traceroute.
- Understand Traceroute in AWS.
- Answer Traceroute interview questions confidently.

---

# 📖 Introduction

Imagine you order a package online.

The package travels through several cities before reaching your home.

You want to know:

- Which cities did it pass through?
- Where is it currently stuck?

Traceroute works the same way.

It shows every network device (hop) that a packet passes through before reaching its destination.

---

# What is Traceroute?

**Traceroute** is a network troubleshooting utility that identifies the path (route) packets take from a source device to a destination.

It also displays the time taken to reach each network device (hop).

---

# Definition

**Traceroute** is a network diagnostic tool that discovers the route packets travel and measures the delay at each hop between the source and destination.

---

# How Traceroute Works

```text
Computer

↓

Router 1

↓

Router 2

↓

Router 3

↓

Destination Server
```

Traceroute displays every router between the source and destination.

---

# TTL in Traceroute

Traceroute uses the **TTL (Time To Live)** field.

Example

```text
TTL = 1

↓

Router 1

↓

TTL Expired

↓

Reply Sent
```

Next

```text
TTL = 2

↓

Router 1

↓

Router 2

↓

TTL Expired

↓

Reply Sent
```

This process continues until the destination is reached.

---

# Commands

### Windows

```bash
tracert google.com
```

---

### Linux

```bash
traceroute google.com
```

---

# Example Output

```text
1  192.168.1.1

2  10.10.1.1

3  172.16.5.1

4  8.8.8.8
```

Each number represents a **Hop**.

---

# What is a Hop?

A **Hop** is every router or Layer 3 device a packet passes through on its journey.

Example

```text
Laptop

↓

Router

↓

ISP Router

↓

Core Router

↓

Google Server
```

Number of Routers

↓

Number of Hops

---

# Understanding Traceroute Output

Example

```text
1

192.168.1.1

2 ms
```

Meaning

- Hop Number → 1
- Router IP → 192.168.1.1
- Time → 2 milliseconds

Lower response times generally indicate better performance.

---

# Common Traceroute Responses

| Response | Meaning |
|-----------|---------|
| Hop IP Address | Router Responded |
| * * * | No Response from Hop |
| Request Timed Out | Device Did Not Reply |
| Trace Complete | Destination Reached |

---

# Why Use Traceroute?

Traceroute helps identify:

- Routing Problems
- High Latency
- Packet Loss
- Network Congestion
- ISP Issues

It shows exactly where communication slows down or stops.

---

# Troubleshooting Examples

### Scenario 1

```bash
ping google.com

❌ Failed
```

Run

```bash
tracert google.com
```

Traceroute shows:

```text
Hop 4

↓

Timed Out
```

Problem

↓

Router 4

---

### Scenario 2

```text
Hop 7

↓

500 ms
```

Problem

↓

High Latency

at Hop 7

---

### Scenario 3

```text
Hop 3

↓

No Reply
```

Possible Causes

- Firewall Blocking
- Router Configuration
- ICMP Disabled

---

# Traceroute vs Ping

| Ping | Traceroute |
|------|------------|
| Tests Reachability | Shows Complete Route |
| Uses ICMP | Uses TTL (and ICMP responses) |
| Shows Total Delay | Shows Delay at Every Hop |
| Simple Connectivity Test | Advanced Routing Analysis |

---

# Traceroute in AWS

Suppose users cannot access an EC2 instance.

Architecture

```text
Laptop

↓

ISP

↓

Internet

↓

Internet Gateway

↓

Amazon VPC

↓

EC2
```

Traceroute helps determine where packets stop.

Possible Causes

- ISP Problem
- Route Table Issue
- Internet Gateway Issue
- VPN Issue

---

# AWS Example

Suppose traffic reaches:

```text
Internet Gateway

↓

Stops
```

Possible Problems

- Route Table
- Security Configuration
- Instance Configuration

Traceroute helps identify the last reachable network hop.

---

# Real-Life Analogy 🚚

Imagine a courier package.

Route

```text
Mumbai

↓

Pune

↓

Hyderabad

↓

Bangalore
```

If the package stops in Hyderabad,

you know exactly where the delay occurred.

Traceroute works in the same way by showing every network stop.

---

# AWS Perspective ☁️

Cloud Engineers use Traceroute to:

- Diagnose routing issues
- Measure network latency
- Identify failed hops
- Verify connectivity between networks
- Troubleshoot hybrid cloud VPN connections

For AWS internal troubleshooting, services such as **VPC Reachability Analyzer** and **VPC Flow Logs** can provide additional insights.

---

# Real AWS Scenario

Users cannot access an EC2 application.

Troubleshooting

```text
Ping EC2

↓

Failed

↓

Run Traceroute

↓

Stops at ISP Router

↓

ISP Issue Identified
```

Another scenario

```text
Traceroute Reaches Internet Gateway

↓

Stops

↓

Check Route Table

↓

Problem Resolved
```

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Traceroute and Ping are the same."**

✅ **Correct:**

Ping checks whether a destination is reachable, while Traceroute shows the complete path packets take.

---

## ❌ Mistake 2

**"Every `* * *` means the network is broken."**

✅ **Correct:**

Some routers are configured not to respond to Traceroute requests. A few `* * *` entries do not always indicate a problem.

---

## ❌ Mistake 3

**"Traceroute guarantees the exact application path."**

✅ **Correct:**

Traceroute shows the network path taken by its probe packets. Application traffic may follow different paths depending on routing and load balancing.

---

## ❌ Mistake 4

**"Traceroute only works on the Internet."**

✅ **Correct:**

Traceroute can also be used on private networks, VPNs, and enterprise networks to troubleshoot connectivity.

---

# 📝 Quick Revision

- Traceroute shows the complete path to a destination.
- Uses TTL to discover each hop.
- Helps identify routing issues.
- Measures delay at every hop.
- Useful for troubleshooting latency and packet loss.
- Windows command: `tracert`
- Linux command: `traceroute`
- AWS engineers use it to diagnose routing problems.

---

# 💼 Interview Questions

### 1. What is Traceroute?

**Answer:**

Traceroute is a network troubleshooting utility that displays the path packets take from a source to a destination and measures the response time at each hop.

---

### 2. How does Traceroute work?

**Answer:**

Traceroute sends packets with increasing TTL values. Each router where the TTL expires returns a response, allowing Traceroute to identify every hop along the path.

---

### 3. What is a Hop?

**Answer:**

A hop is any Layer 3 device (typically a router) that forwards a packet from one network to another on its way to the destination.

---

### 4. What is the difference between Ping and Traceroute?

**Answer:**

- **Ping:** Tests whether a destination is reachable and measures overall round-trip time.
- **Traceroute:** Displays every hop between the source and destination and measures the delay at each hop.

---

### 5. Why would you use Traceroute in AWS?

**Answer:**

Traceroute helps identify routing issues, latency, ISP problems, VPN connectivity issues, and determine where traffic stops before reaching an AWS resource.

---

### 6. What does `* * *` mean in Traceroute output?

**Answer:**

It means no response was received from that hop. This may occur because the router is configured not to respond to Traceroute requests, a firewall blocks the probes, or there is a network issue.

---

# 7. ipconfig / ifconfig Command

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand the ipconfig and ifconfig commands.
- Learn how to view network configuration.
- Understand IP Address, Subnet Mask, Gateway, and DNS.
- Troubleshoot network problems using ipconfig/ifconfig.
- Learn AWS networking troubleshooting.
- Answer interview questions confidently.

---

# 📖 Introduction

Imagine you visit a new city.

Before travelling,

you need to know:

- Your Address
- City
- Road
- Destination

Similarly,

a computer needs networking information before communicating.

The **ipconfig** and **ifconfig** commands display this information.

---

# What is ipconfig?

**ipconfig** (IP Configuration) is a Windows command used to display and manage network configuration.

It helps troubleshoot IP-related problems.

---

# Definition

**ipconfig** is a command-line utility that displays and manages TCP/IP network configuration on Windows systems.

---

# What is ifconfig?

**ifconfig** (Interface Configuration) is a Linux/Unix command used to view and configure network interfaces.

> **Note:** On modern Linux distributions, the `ip` command (such as `ip addr`) is preferred, but `ifconfig` is still widely asked in interviews.

---

# Basic Commands

### Windows

```bash
ipconfig
```

---

### Linux

```bash
ifconfig
```

or

```bash
ip addr
```

---

# Sample ipconfig Output

```text
IPv4 Address

192.168.1.100

Subnet Mask

255.255.255.0

Default Gateway

192.168.1.1
```

---

# Understanding the Output

### IPv4 Address

Identifies your device on the network.

Example

```text
192.168.1.100
```

---

### Subnet Mask

Defines the network and host portions of the IP address.

Example

```text
255.255.255.0
```

---

### Default Gateway

The router that connects your local network to other networks.

Example

```text
192.168.1.1
```

---

### DNS Server

Converts domain names into IP addresses.

Example

```text
8.8.8.8
```

---

# Useful ipconfig Commands

### Display Detailed Information

```bash
ipconfig /all
```

Shows:

- MAC Address
- DHCP Status
- DNS Servers
- Lease Information
- Adapter Details

---

### Release IP Address

```bash
ipconfig /release
```

Releases the current DHCP IP address.

---

### Renew IP Address

```bash
ipconfig /renew
```

Requests a new IP address from the DHCP server.

---

### Flush DNS Cache

```bash
ipconfig /flushdns
```

Clears the local DNS cache.

Useful when websites resolve to old or incorrect IP addresses.

---

# Useful Linux Commands

Show IP Address

```bash
ip addr
```

---

Show Routing Table

```bash
ip route
```

---

Show Network Interfaces

```bash
ifconfig
```

---

# Common Troubleshooting Scenarios

## Scenario 1

Internet Not Working

Check

```bash
ipconfig
```

Output

```text
IPv4

169.254.x.x
```

Problem

↓

APIPA Address

↓

DHCP Server Not Reachable

---

## Scenario 2

Wrong Default Gateway

Output

```text
Gateway

192.168.5.1
```

Actual Router

```text
192.168.1.1
```

Problem

↓

Incorrect Gateway

↓

No Internet

---

## Scenario 3

DNS Issue

Run

```bash
ipconfig /flushdns
```

Then

```bash
ping google.com
```

Website starts working.

---

# APIPA Address

If DHCP fails,

Windows automatically assigns an address from:

```text
169.254.0.0/16
```

This is called:

```text
APIPA

Automatic Private IP Addressing
```

It indicates the device could not obtain an IP address from a DHCP server.

---

# ipconfig vs ifconfig

| ipconfig | ifconfig |
|-----------|----------|
| Windows | Linux/Unix |
| Displays IP Configuration | Displays Network Interface Configuration |
| Can Renew DHCP | Can Configure Interfaces |
| Used for Troubleshooting | Used for Troubleshooting |

---

# Real-Life Analogy 🏠

Imagine sending a letter.

You need:

```text
Your Address

↓

Road

↓

City

↓

Destination
```

Similarly,

a computer needs:

- IP Address
- Subnet Mask
- Gateway
- DNS

before it can communicate.

---

# AWS Perspective ☁️

Suppose an EC2 instance cannot access the Internet.

Check:

```text
Private IP

↓

Subnet

↓

Route Table

↓

Internet Gateway

↓

Security Group
```

Inside the EC2 instance,

commands such as:

```bash
ip addr
```

or

```bash
ifconfig
```

help verify the network configuration.

---

# Real AWS Scenario

Linux EC2

```bash
ip addr
```

Output

```text
Private IP

10.0.1.25
```

Internet not working.

Troubleshooting

```text
Private IP

✅

↓

Route Table

❌

↓

Add Internet Gateway Route

↓

Internet Restored
```

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"169.254.x.x is a valid DHCP address."**

✅ **Correct:**

It is an **APIPA** address assigned automatically when a DHCP server cannot be reached.

---

## ❌ Mistake 2

**"ipconfig works on Linux."**

✅ **Correct:**

`ipconfig` is a Windows command. Linux commonly uses `ip addr` or `ifconfig`.

---

## ❌ Mistake 3

**"Flushing DNS changes the IP address."**

✅ **Correct:**

`ipconfig /flushdns` clears the DNS cache only. It does not change the device's IP address.

---

## ❌ Mistake 4

**"The Default Gateway is the DNS Server."**

✅ **Correct:**

The **Default Gateway** forwards traffic to other networks, while the **DNS Server** resolves domain names into IP addresses.

---

# 📝 Quick Revision

- ipconfig → Windows networking command.
- ifconfig / ip addr → Linux networking commands.
- `ipconfig /all` → Detailed network information.
- `ipconfig /release` → Release DHCP IP.
- `ipconfig /renew` → Obtain new DHCP IP.
- `ipconfig /flushdns` → Clear DNS cache.
- APIPA = 169.254.0.0/16.
- Check IP Address, Gateway, DNS, and Subnet during troubleshooting.

---

# 💼 Interview Questions

### 1. What is the ipconfig command?

**Answer:**

`ipconfig` is a Windows command-line utility used to display and manage TCP/IP network configuration, including IP addresses, subnet masks, gateways, and DNS settings.

---

### 2. What is the Linux equivalent of ipconfig?

**Answer:**

The traditional equivalent is **ifconfig**, while the modern recommended command is **ip addr**.

---

### 3. What does `ipconfig /all` display?

**Answer:**

It displays detailed network information such as:

- IP Address
- MAC Address
- Subnet Mask
- Default Gateway
- DNS Servers
- DHCP Status
- Lease Information

---

### 4. What is APIPA?

**Answer:**

APIPA (Automatic Private IP Addressing) automatically assigns an IP address from the **169.254.0.0/16** range when a DHCP server is unavailable.

---

### 5. What does `ipconfig /flushdns` do?

**Answer:**

It clears the local DNS resolver cache, allowing the computer to obtain fresh DNS records from the DNS server.

---

### 6. How are these commands useful in AWS?

**Answer:**

On EC2 instances, `ip addr` or `ifconfig` can be used to verify the instance's network configuration, such as private IP addresses and network interfaces, while troubleshooting connectivity issues along with VPC components like Route Tables, Security Groups, and Internet Gateways.

---

# 8. netstat Command

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand the netstat command.
- Learn how to view active network connections.
- Identify listening ports.
- Learn how to troubleshoot network services.
- Understand netstat in AWS.
- Answer interview questions confidently.

---

# 📖 Introduction

Imagine an office building.

Many employees are talking on different phone calls.

Some employees are:

- Making calls
- Receiving calls
- Waiting for calls

You want to know:

- Who is connected?
- Which phone lines are open?
- Which phone lines are waiting?

The **netstat** command provides similar information for a computer.

It shows:

- Active Network Connections
- Listening Ports
- Routing Information
- Network Statistics

---

# What is netstat?

**netstat** stands for:

```text
Network Statistics
```

It is a command-line utility used to display active network connections, listening ports, routing tables, and protocol statistics.

---

# Definition

**netstat** is a network diagnostic command used to display active TCP/UDP connections, listening ports, routing information, and network statistics.

---

# Why is netstat Used?

Network Engineers use netstat to:

- Check Active Connections
- Identify Open Ports
- Verify Listening Services
- Troubleshoot Applications
- Detect Suspicious Connections

---

# Basic Commands

### Windows

```bash
netstat
```

---

### Linux

```bash
netstat
```

or

```bash
ss
```

> **Note:** On modern Linux systems, the `ss` command is preferred because it is faster than `netstat`.

---

# Sample Output

```text
Proto

Local Address

Foreign Address

State
```

Example

```text
TCP

192.168.1.100:50500

142.250.183.46:443

ESTABLISHED
```

Meaning

- TCP Connection
- Connected to HTTPS
- Connection Active

---

# Understanding netstat Output

### Protocol

Example

```text
TCP

UDP
```

Shows the protocol being used.

---

### Local Address

Example

```text
192.168.1.100:50000
```

Your computer's IP address and port number.

---

### Foreign Address

Example

```text
142.250.183.46:443
```

The remote computer connected to your device.

---

### State

Shows the connection status.

Example

```text
ESTABLISHED
```

Connection is active.

---

# Common Connection States

| State | Meaning |
|--------|---------|
| LISTENING | Waiting for Incoming Connection |
| ESTABLISHED | Active Connection |
| TIME_WAIT | Connection Closing |
| CLOSE_WAIT | Waiting for Connection to Close |
| SYN_SENT | Connection Request Sent |

---

# Useful netstat Commands

### Show All Connections

```bash
netstat -a
```

Displays:

- Active Connections
- Listening Ports

---

### Show Numerical Addresses

```bash
netstat -n
```

Displays IP addresses instead of domain names.

---

### Show Process ID (Windows)

```bash
netstat -ano
```

Displays:

- IP Address
- Port
- Connection State
- Process ID (PID)

Useful for identifying which application is using a port.

---

### Linux

Show Listening Ports

```bash
netstat -tuln
```

or

```bash
ss -tuln
```

---

# Example

```text
TCP

0.0.0.0:80

LISTENING
```

Meaning

A web server is listening on:

```text
Port 80
```

---

# Troubleshooting Scenarios

## Scenario 1

Website Not Opening

Run

```bash
netstat -a
```

Output

```text
Port 80

Not Listening
```

Problem

↓

Web Server

Not Running

---

## Scenario 2

SSH Not Working

Run

```bash
netstat -a
```

Output

```text
Port 22

Not Listening
```

Problem

↓

SSH Service Stopped

---

## Scenario 3

Unknown Connection

Output

```text
ESTABLISHED

Unknown IP
```

Possible Causes

- Malware
- Unauthorized Software
- Suspicious Activity

Investigate immediately.

---

# netstat vs Ping

| netstat | Ping |
|----------|------|
| Shows Active Connections | Tests Connectivity |
| Displays Listening Ports | Uses ICMP |
| Used for Local Troubleshooting | Used for Network Reachability |

---

# netstat vs Traceroute

| netstat | Traceroute |
|----------|------------|
| Shows Active Connections | Shows Packet Path |
| Displays Port Information | Displays Network Hops |
| Troubleshoots Services | Troubleshoots Routing |

---

# Real-Life Analogy 📞

Imagine a telephone exchange.

You want to know:

```text
Which Phones

↓

Are Active
```

```text
Which Phones

↓

Are Waiting
```

```text
Which Phones

↓

Are Connected
```

netstat provides the same information for network connections.

---

# AWS Perspective ☁️

Suppose an EC2 web server is not responding.

Check

```bash
netstat -tuln
```

Output

```text
Port 80

Not Listening
```

Problem

↓

Apache/Nginx

Not Running

Even if the Security Group allows Port 80,

the application must also be listening on that port.

---

# Real AWS Scenario

Users cannot access an EC2 website.

Architecture

```text
Internet

↓

Security Group

↓

EC2
```

Troubleshooting

```text
Security Group

Port 80

Allowed

✅

↓

netstat

↓

Port 80

Not Listening

❌

↓

Start Apache

↓

Website Working
```

The issue was with the application service, not AWS networking.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"If Security Group allows Port 80, the website must work."**

✅ **Correct:**

The web server must also be running and listening on Port 80.

---

## ❌ Mistake 2

**"netstat checks Internet connectivity."**

✅ **Correct:**

netstat displays network connections and listening ports. It does not test connectivity like Ping.

---

## ❌ Mistake 3

**"LISTENING means someone is connected."**

✅ **Correct:**

LISTENING means the application is waiting for incoming connections. It does not mean a client is currently connected.

---

## ❌ Mistake 4

**"ESTABLISHED means the application is healthy."**

✅ **Correct:**

ESTABLISHED only indicates that a network connection exists. The application itself may still have issues.

---

# 📝 Quick Revision

- netstat = Network Statistics.
- Shows active network connections.
- Displays listening ports.
- Useful for troubleshooting services.
- `netstat -a` → All connections.
- `netstat -n` → Numeric addresses.
- `netstat -ano` → Includes Process ID (Windows).
- `netstat -tuln` or `ss -tuln` → Listening ports (Linux).

---

# 💼 Interview Questions

### 1. What is the netstat command?

**Answer:**

netstat is a command-line utility that displays active network connections, listening ports, routing information, and network statistics.

---

### 2. What does the LISTENING state mean?

**Answer:**

LISTENING means an application or service is waiting for incoming network connections on a specific port.

---

### 3. What does the ESTABLISHED state mean?

**Answer:**

ESTABLISHED indicates that a TCP connection has been successfully created and data can be exchanged between the source and destination.

---

### 4. Which command shows all active connections?

**Answer:**

```bash
netstat -a
```

It displays all active connections and listening ports.

---

### 5. How is netstat useful in AWS?

**Answer:**

On EC2 instances, netstat helps verify whether services such as SSH (Port 22) or HTTP (Port 80) are actively listening, helping distinguish application issues from networking issues.

---

### 6. What is the modern Linux alternative to netstat?

**Answer:**

The **ss** command is the modern replacement for netstat on many Linux distributions because it is fastver and provides similar network socket information.

---

# 9. nslookup Command

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand the nslookup command.
- Learn how DNS resolution works.
- Troubleshoot DNS-related problems.
- Understand nslookup in AWS.
- Answer interview questions confidently.

---

# 📖 Introduction

Imagine you want to visit your friend's house.

You know only their name,

not their address.

So you search the address using Google Maps.

DNS works the same way.

It converts a domain name into an IP address.

The **nslookup** command helps verify whether DNS is working correctly.

---

# What is nslookup?

**nslookup** stands for:

```text
Name Server Lookup
```

It is a command-line utility used to query DNS servers and resolve domain names into IP addresses.

---

# Definition

**nslookup** is a network diagnostic tool used to query DNS servers for domain name resolution and DNS record information.

---

# Why is nslookup Used?

Network Engineers use nslookup to:

- Verify DNS Resolution
- Troubleshoot DNS Issues
- Find IP Addresses
- Check DNS Servers
- Verify DNS Records

---

# How DNS Works

```text
User

↓

google.com

↓

DNS Server

↓

142.250.xxx.xxx

↓

Website Opens
```

DNS converts a domain name into an IP address.

---

# Basic Commands

### Windows

```bash
nslookup google.com
```

---

### Linux

```bash
nslookup google.com
```

*(The command is available if the DNS utilities package is installed.)*

---

# Sample Output

```text
Server

8.8.8.8

Address

8.8.8.8

Name

google.com

Address

142.250.183.46
```

Meaning

- DNS Server Used
- Domain Name
- IP Address Returned

---

# Understanding the Output

### Server

The DNS server that answered the query.

Example

```text
8.8.8.8
```

---

### Name

The domain name requested.

Example

```text
google.com
```

---

### Address

The IP address associated with the domain.

Example

```text
142.250.183.46
```

---

# Common Troubleshooting Scenarios

## Scenario 1

```bash
ping google.com

❌ Failed
```

Run

```bash
nslookup google.com
```

Output

```text
DNS Request Timed Out
```

Problem

↓

DNS Server Not Responding

---

## Scenario 2

```bash
nslookup google.com

↓

Correct IP Returned

✅
```

DNS is working correctly.

The problem is likely somewhere else in the network.

---

## Scenario 3

```bash
nslookup abcxyz123.com

↓

Non-existent domain
```

Meaning

- Domain does not exist
- Incorrect spelling
- DNS record missing

---

# Query Specific DNS Server

Example

```bash
nslookup google.com 8.8.8.8
```

This queries Google's public DNS server directly.

---

# Common DNS Record Types

| Record | Purpose |
|----------|----------|
| A | Maps Domain → IPv4 Address |
| AAAA | Maps Domain → IPv6 Address |
| CNAME | Alias Record |
| MX | Mail Server Record |
| NS | Name Server Record |
| TXT | Text Information (SPF, Verification, etc.) |

---

# DNS Troubleshooting Flow

```text
Website Not Opening

↓

Ping IP Address

↓

Working

↓

Run nslookup

↓

DNS Failure Found

↓

Fix DNS
```

---

# nslookup vs Ping

| nslookup | Ping |
|-----------|------|
| Tests DNS Resolution | Tests Network Connectivity |
| Returns IP Address | Measures Reachability |
| Queries DNS Server | Uses ICMP |

---

# nslookup vs Traceroute

| nslookup | Traceroute |
|-----------|------------|
| Resolves Domain Names | Shows Packet Route |
| Checks DNS | Checks Network Path |

---

# Real-Life Analogy 📖

Imagine a phone directory.

You know:

```text
John
```

You search the directory.

↓

You get:

```text
Phone Number
```

Similarly,

DNS converts:

```text
google.com

↓

142.250.xxx.xxx
```

---

# AWS Perspective ☁️

AWS uses **Amazon Route 53** for DNS services.

Cloud Engineers use nslookup to verify:

- Route 53 Records
- Public DNS Resolution
- Private Hosted Zones
- EC2 Public DNS
- Load Balancer DNS Names

---

# Real AWS Scenario

Users cannot access:

```text
www.company.com
```

Troubleshooting

```text
Run nslookup

↓

No IP Returned

↓

Check Route 53

↓

Missing A Record

↓

Create Record

↓

Website Working
```

The issue was DNS, not the web server.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"nslookup checks Internet connectivity."**

✅ **Correct:**

nslookup checks **DNS resolution**, not Internet connectivity.

---

## ❌ Mistake 2

**"If nslookup works, the website must work."**

✅ **Correct:**

DNS may resolve correctly, but the web server, firewall, Security Group, or application could still be unavailable.

---

## ❌ Mistake 3

**"Ping and nslookup perform the same function."**

✅ **Correct:**

Ping tests connectivity, while nslookup verifies DNS resolution.

---

## ❌ Mistake 4

**"Route 53 stores website files."**

✅ **Correct:**

Amazon Route 53 is a **DNS service**. It stores DNS records, not website content.

---

# 📝 Quick Revision

- nslookup = Name Server Lookup.
- Used to troubleshoot DNS.
- Resolves domain names into IP addresses.
- Queries DNS servers.
- Common DNS records:
  - A
  - AAAA
  - CNAME
  - MX
  - NS
  - TXT
- AWS uses Amazon Route 53 for DNS.

---

# 💼 Interview Questions

### 1. What is nslookup?

**Answer:**

nslookup is a command-line utility used to query DNS servers and resolve domain names into IP addresses.

---

### 2. Why is nslookup used?

**Answer:**

It is used to verify DNS resolution, troubleshoot DNS problems, and retrieve DNS records for domains.

---

### 3. What is the difference between Ping and nslookup?

**Answer:**

- **Ping:** Tests network connectivity using ICMP.
- **nslookup:** Tests DNS resolution by querying a DNS server.

---

### 4. What does "Non-existent domain" mean?

**Answer:**

It means the requested domain cannot be found in DNS. The domain may not exist, may be misspelled, or the required DNS record is missing.

---

### 5. Which AWS service provides DNS functionality?

**Answer:**

**Amazon Route 53** is AWS's managed DNS service used to register domains, create DNS records, and route traffic.

---

### 6. Can nslookup verify whether a website is running?

**Answer:**

No. nslookup only verifies DNS resolution. Even if DNS resolves successfully, the website or application itself may still be unavailable.

---

# 10. ARP Command

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand ARP.
- Learn how ARP works.
- Understand the ARP Cache.
- Use the ARP command for troubleshooting.
- Learn ARP in AWS.
- Answer ARP interview questions confidently.

---

# 📖 Introduction

Imagine you know your friend's house number,

but you don't know the color of the house.

Before delivering a parcel,

you ask the neighbors,

"Which house belongs to Rahul?"

Once you get the answer,

you remember it for future deliveries.

ARP works in a similar way.

It converts an **IP Address** into a **MAC Address** within a local network.

---

# What is ARP?

ARP stands for:

```text
Address Resolution Protocol
```

It is used to map an IPv4 address to a MAC address.

Without ARP,

devices on the same LAN cannot communicate.

---

# Definition

**ARP (Address Resolution Protocol)** is a protocol used to resolve an IPv4 address into the corresponding MAC address on a local network.

---

# Why is ARP Needed?

Every device has:

- IP Address (Logical Address)
- MAC Address (Physical Address)

When sending data within the same network,

the sender must know the destination MAC address.

ARP helps discover it.

---

# How ARP Works

```text
Computer A

↓

Needs MAC Address

↓

Broadcast ARP Request

↓

Computer B

↓

ARP Reply

↓

MAC Address Received

↓

Communication Begins
```

---

# ARP Request

The sender broadcasts:

```text
Who has

192.168.1.20

?

Tell

192.168.1.10
```

Every device receives the request,

but only the device with IP **192.168.1.20** responds.

---

# ARP Reply

The destination replies:

```text
192.168.1.20

is at

00-1A-2B-3C-4D-5E
```

Now communication can begin.

---

# ARP Cache

After receiving the MAC address,

the sender stores it in memory.

This is called:

```text
ARP Cache
```

This avoids sending repeated ARP requests.

---

# ARP Process

```text
Need Destination

↓

Check ARP Cache

↓

Found?

↓

Yes

↓

Send Packet
```

If not found

↓

```text
Broadcast ARP Request

↓

Receive ARP Reply

↓

Update Cache

↓

Send Packet
```

---

# ARP Command

### Windows

```bash
arp -a
```

---

### Linux

```bash
arp -a
```

or

```bash
ip neigh
```

---

# Sample Output

```text
Internet Address

192.168.1.1

Physical Address

00-50-56-C0-00-08

Type

Dynamic
```

---

# Understanding the Output

### Internet Address

The device's IP address.

Example

```text
192.168.1.1
```

---

### Physical Address

The MAC address.

Example

```text
00-50-56-C0-00-08
```

---

### Type

```text
Dynamic
```

Automatically learned using ARP.

or

```text
Static
```

Manually configured.

---

# Useful ARP Commands

### Display ARP Cache

```bash
arp -a
```

---

### Delete ARP Cache (Windows)

```bash
arp -d *
```

---

### Linux

Clear Neighbor Cache

```bash
ip neigh flush all
```

---

# Common Troubleshooting Scenarios

## Scenario 1

Cannot Reach Local Device

Run

```bash
arp -a
```

No MAC address found.

Problem

↓

ARP Resolution Failed

↓

Device Offline

or

↓

Wrong IP Address

---

## Scenario 2

Duplicate IP Address

Two devices respond for the same IP.

Result

↓

Communication Problems

---

## Scenario 3

Old MAC Address Cached

Problem

↓

Incorrect Device

↓

Communication Failure

Solution

↓

Clear ARP Cache

---

# Dynamic vs Static ARP

| Dynamic ARP | Static ARP |
|--------------|------------|
| Learned Automatically | Configured Manually |
| Temporary | Permanent |
| Most Common | Used in Special Cases |

---

# ARP vs DNS

| ARP | DNS |
|------|------|
| IP → MAC Address | Domain → IP Address |
| Works on Local Network | Works Across Networks |
| Uses Broadcast | Uses DNS Server |

---

# ARP vs RARP

| ARP | RARP |
|------|------|
| IP → MAC | MAC → IP |
| Commonly Used | Mostly Obsolete |

---

# Real-Life Analogy 🏠

Imagine a housing society.

You know:

```text
Flat Number

302
```

But you don't know

who lives there.

You ask the security guard.

↓

He tells you:

```text
Rahul Lives Here
```

Similarly,

ARP finds the MAC address using the IP address.

---

# AWS Perspective ☁️

AWS manages Layer 2 networking internally,

so Cloud Engineers usually don't troubleshoot ARP directly.

However,

ARP concepts are still important for understanding:

- Elastic Network Interfaces (ENIs)
- Local Network Communication
- EC2 Networking
- VPC Architecture

Inside a Linux EC2 instance,

you can view neighboring devices using:

```bash
ip neigh
```

---

# Real AWS Scenario

Suppose two EC2 instances are in the same subnet.

```text
EC2-A

↓

Needs MAC Address

↓

AWS Virtual Network

↓

ARP Resolution

↓

EC2-B
```

The ARP process happens automatically within the VPC's virtual network.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"ARP converts domain names into IP addresses."**

✅ **Correct:**

DNS converts **Domain Names → IP Addresses**.

ARP converts **IP Addresses → MAC Addresses**.

---

## ❌ Mistake 2

**"ARP works across the Internet."**

✅ **Correct:**

ARP works only within the **local network (LAN)**.

Routers do not forward ARP broadcasts.

---

## ❌ Mistake 3

**"ARP uses TCP."**

✅ **Correct:**

ARP is its own protocol and does **not** use TCP or UDP.

---

## ❌ Mistake 4

**"Cloud Engineers never need to know ARP."**

✅ **Correct:**

Although AWS abstracts Layer 2 networking, understanding ARP helps explain how local communication and ENIs work inside a VPC.

---

# 📝 Quick Revision

- ARP = Address Resolution Protocol.
- Converts IP Address → MAC Address.
- Works only on the Local Network.
- Uses ARP Request and ARP Reply.
- Stores mappings in the ARP Cache.
- `arp -a` displays the ARP table.
- Linux alternative: `ip neigh`.
- AWS handles ARP automatically inside the VPC.

---

# 💼 Interview Questions

### 1. What is ARP?

**Answer:**

ARP (Address Resolution Protocol) is used to resolve an IPv4 address into its corresponding MAC address within a local network.

---

### 2. Why is ARP required?

**Answer:**

Devices communicate using MAC addresses on a LAN. ARP helps a device discover the MAC address associated with a known IP address.

---

### 3. What is the ARP Cache?

**Answer:**

The ARP Cache is a temporary table that stores IP-to-MAC address mappings, reducing the need for repeated ARP broadcasts.

---

### 4. Which command displays the ARP table?

**Answer:**

- **Windows:** `arp -a`
- **Linux:** `arp -a` or `ip neigh`

---

### 5. What is the difference between ARP and DNS?

**Answer:**

- **ARP:** Resolves IP addresses to MAC addresses on a local network.
- **DNS:** Resolves domain names to IP addresses across networks.

---

### 6. Does ARP work across the Internet?

**Answer:**

No. ARP works only within a local network (LAN). Routers do not forward ARP broadcast messages.

---

# 11. Route Command

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand the Route command.
- Learn how routing tables work.
- View and manage routing information.
- Troubleshoot routing issues.
- Understand Route Tables in AWS.
- Answer Route command interview questions confidently.

---

# 📖 Introduction

Imagine you want to travel from Mumbai to Delhi.

Before starting,

Google Maps decides the best route.

If the route is incorrect,

you may never reach your destination.

Computers work the same way.

They use a **Routing Table** to determine where packets should be sent.

The **Route** command allows us to view and manage this routing information.

---

# What is the Route Command?

The **Route** command displays and manages the routing table of a computer.

It tells the operating system where to send network packets.

---

# Definition

**Route** is a networking command used to view, add, modify, and delete routing table entries on a computer.

---

# What is a Routing Table?

A Routing Table is a list of routes used by the operating system to forward packets to their destination.

Each route contains:

- Destination Network
- Gateway
- Subnet Mask
- Interface
- Metric

---

# Routing Process

```text
Packet

↓

Routing Table

↓

Best Route Selected

↓

Gateway

↓

Destination
```

---

# Basic Commands

### Windows

Display Routing Table

```bash
route print
```

---

### Linux

Display Routing Table

```bash
route -n
```

or

```bash
ip route
```

> **Note:** Modern Linux systems recommend using the `ip route` command.

---

# Sample Routing Table

```text
Destination

0.0.0.0

Gateway

192.168.1.1

Mask

0.0.0.0

Interface

192.168.1.100
```

---

# Understanding the Routing Table

### Destination

The network or host where packets are being sent.

Example

```text
192.168.1.0
```

---

### Gateway

The next-hop router.

Example

```text
192.168.1.1
```

---

### Netmask

Defines the destination network.

Example

```text
255.255.255.0
```

---

### Interface

The local network adapter used to send packets.

---

### Metric

The cost of a route.

Lower metric

↓

Higher priority

---

# Default Route

Example

```text
Destination

0.0.0.0

Gateway

192.168.1.1
```

The default route is used when no more specific route matches.

It is also called:

```text
Default Gateway
```

---

# Useful Route Commands

### Display Routing Table

Windows

```bash
route print
```

Linux

```bash
ip route
```

---

### Add Route

Windows

```bash
route add
```

Linux

```bash
ip route add
```

---

### Delete Route

Windows

```bash
route delete
```

Linux

```bash
ip route del
```

---

# Common Troubleshooting Scenarios

## Scenario 1

No Internet Access

Routing Table

```text
No Default Route
```

Problem

↓

Packets have nowhere to go.

Solution

↓

Configure the Default Gateway.

---

## Scenario 2

Wrong Gateway

Routing Table

```text
Gateway

192.168.10.1
```

Actual Gateway

```text
192.168.1.1
```

Problem

↓

Traffic sent to the wrong router.

---

## Scenario 3

Missing Route

Packet

↓

Destination Network

↓

No Matching Route

↓

Packet Dropped

---

# Longest Prefix Match

When multiple routes match,

the operating system chooses the route with the:

```text
Longest Prefix Match
```

Example

```text
10.0.0.0/8

↓

General Route
```

```text
10.0.1.0/24

↓

More Specific Route

↓

Selected
```

More specific routes are preferred.

---

# Route Command vs Traceroute

| Route | Traceroute |
|--------|------------|
| Shows Local Routing Table | Shows Complete Packet Path |
| Used to Manage Routes | Used to Diagnose Routing |
| Local Device Only | Entire Network Path |

---

# Real-Life Analogy 🗺️

Imagine using Google Maps.

Google Maps checks:

```text
Destination

↓

Available Roads

↓

Best Route

↓

Travel
```

Similarly,

the operating system checks the routing table before forwarding packets.

---

# AWS Perspective ☁️

AWS uses **VPC Route Tables** instead of the operating system's routing table.

A Route Table controls where traffic goes inside a VPC.

Example

```text
EC2

↓

Route Table

↓

Internet Gateway

↓

Internet
```

Common AWS routes include:

```text
0.0.0.0/0

↓

Internet Gateway
```

or

```text
0.0.0.0/0

↓

NAT Gateway
```

---

# Real AWS Scenario

Users cannot access the Internet from an EC2 instance.

Architecture

```text
EC2

↓

VPC Route Table

↓

Internet Gateway
```

Problem

```text
Missing Route

0.0.0.0/0
```

Solution

```text
Add Route

0.0.0.0/0

↓

Internet Gateway
```

Internet access is restored.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"The Route command shows every router on the Internet."**

✅ **Correct:**

The Route command displays the **local routing table** only.

Use **Traceroute** to view routers between the source and destination.

---

## ❌ Mistake 2

**"The default route is used for every packet."**

✅ **Correct:**

The default route is used **only when no more specific route exists**.

---

## ❌ Mistake 3

**"A higher metric means a better route."**

✅ **Correct:**

A **lower metric** indicates a more preferred route.

---

## ❌ Mistake 4

**"AWS Route Tables automatically provide Internet access."**

✅ **Correct:**

A Route Table must contain a valid route (such as `0.0.0.0/0` to an Internet Gateway), and other networking components such as Security Groups and Internet Gateway must also be configured correctly.

---

# 📝 Quick Revision

- Route command displays and manages the routing table.
- Routing tables determine where packets are sent.
- Default Route = `0.0.0.0/0`.
- Lower metric = Higher priority.
- Longest Prefix Match selects the most specific route.
- Windows: `route print`
- Linux: `ip route`
- AWS uses VPC Route Tables.

---

# 💼 Interview Questions

### 1. What is the Route command?

**Answer:**

The Route command is used to display and manage the routing table, which determines how network packets are forwarded to their destinations.

---

### 2. What is a Routing Table?

**Answer:**

A Routing Table is a collection of routes that tells the operating system where to send packets based on the destination network.

---

### 3. What is the Default Route?

**Answer:**

The Default Route (`0.0.0.0/0`) is used when no more specific route matches the destination IP address.

---

### 4. What is Longest Prefix Match?

**Answer:**

Longest Prefix Match is the routing principle where the most specific matching route is selected over more general routes.

---

### 5. How is the Route command useful in AWS?

**Answer:**

Although the operating system has its own routing table, AWS networking primarily relies on **VPC Route Tables** to control traffic between subnets, Internet Gateways, NAT Gateways, VPNs, and other AWS resources.

---

### 6. Which command displays the routing table?

**Answer:**

- **Windows:** `route print`
- **Linux:** `ip route` (recommended) or `route -n`

---

# 12. Packet Capture (Wireshark Basics)

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand Packet Capture.
- Learn what Wireshark is.
- Understand how packet capturing works.
- Learn basic Wireshark filters.
- Troubleshoot network problems using Wireshark.
- Understand packet analysis in AWS.
- Answer Wireshark interview questions confidently.

---

# 📖 Introduction

Imagine two people are talking on the phone.

If something goes wrong,

you may want to listen to the conversation to understand the problem.

Similarly,

Network Engineers capture network packets to understand exactly what is happening between devices.

This process is called:

```text
Packet Capture
```

The most popular packet capture tool is:

```text
Wireshark
```

---

# What is Packet Capture?

Packet Capture is the process of recording network packets as they travel across a network.

It helps engineers analyze communication and troubleshoot problems.

---

# Definition

**Packet Capture** is the process of collecting and analyzing network packets to diagnose connectivity, performance, and security issues.

---

# What is Wireshark?

Wireshark is a free and open-source network protocol analyzer.

It captures network traffic and allows engineers to inspect packets in detail.

---

# Why Use Wireshark?

Wireshark helps to:

- Troubleshoot Network Issues
- Analyze Packets
- Detect Network Errors
- Investigate Security Incidents
- Learn Network Protocols
- Debug Applications

---

# How Packet Capture Works

```text
Computer A

↓

Packets

↓

Network

↓

Wireshark

↓

Packet Analysis
```

Wireshark captures packets before displaying them for analysis.

---

# Packet Structure

Every packet contains:

```text
Packet

│

├── Source IP

├── Destination IP

├── Protocol

├── Source Port

├── Destination Port

└── Data
```

---

# Wireshark Interface

The Wireshark window mainly consists of:

```text
Packet List

↓

Packet Details

↓

Packet Bytes
```

Each section provides different information about the captured traffic.

---

# Common Protocols Seen in Wireshark

- TCP
- UDP
- HTTP
- HTTPS
- DNS
- ARP
- ICMP
- DHCP
- TLS

---

# Common Wireshark Filters

### Display HTTP Traffic

```text
http
```

---

### Display HTTPS Traffic

```text
tls
```

---

### Display DNS Traffic

```text
dns
```

---

### Display ICMP (Ping)

```text
icmp
```

---

### Display ARP

```text
arp
```

---

### Display TCP

```text
tcp
```

---

### Display UDP

```text
udp
```

---

### Display Traffic for One IP

```text
ip.addr == 192.168.1.10
```

---

### Display One Port

```text
tcp.port == 80
```

---

# Common Troubleshooting Scenarios

## Scenario 1

Website Not Opening

Capture packets.

Observation

```text
DNS Query

↓

No Response
```

Problem

↓

DNS Failure

---

## Scenario 2

Ping Not Working

Capture

```text
ICMP Request

↓

No Reply
```

Possible Causes

- Firewall
- Network Issue
- Destination Offline

---

## Scenario 3

Slow Website

Capture

```text
TCP Retransmissions

↓

High Latency

↓

Slow Performance
```

---

# Packet Flow Example

```text
Browser

↓

DNS Query

↓

DNS Response

↓

TCP Handshake

↓

HTTP Request

↓

HTTP Response

↓

Webpage Loads
```

Wireshark allows you to inspect each step.

---

# TCP Three-Way Handshake in Wireshark

```text
Client

↓

SYN

↓

Server

↓

SYN-ACK

↓

Client

↓

ACK

↓

Connection Established
```

You can easily identify this handshake in a packet capture.

---

# Wireshark vs Ping

| Wireshark | Ping |
|------------|------|
| Captures Packets | Tests Connectivity |
| Deep Packet Analysis | Simple Reachability Test |
| Supports Many Protocols | Uses ICMP Only |

---

# Wireshark vs Traceroute

| Wireshark | Traceroute |
|------------|------------|
| Captures Network Packets | Shows Packet Path |
| Packet-Level Analysis | Hop-Level Analysis |

---

# Real-Life Analogy 📹

Imagine CCTV cameras.

Instead of guessing what happened,

you review the recorded footage.

Similarly,

Wireshark records network traffic,

allowing engineers to replay and analyze communication.

---

# AWS Perspective ☁️

Traditional Wireshark captures packets on local systems.

In AWS,

Cloud Engineers often use:

- VPC Flow Logs
- Traffic Mirroring
- Reachability Analyzer
- CloudWatch
- CloudTrail

For EC2 instances,

packet capture tools like Wireshark or `tcpdump` can be used directly on the instance (where appropriate).

---

# AWS Traffic Mirroring

AWS supports:

```text
EC2

↓

Traffic Mirroring

↓

Monitoring Appliance

↓

Packet Analysis
```

This allows packet inspection without affecting production workloads.

---

# Real AWS Scenario

Users cannot access a web application.

Troubleshooting

```text
Capture Traffic

↓

DNS Success

↓

TCP Handshake Failed

↓

Security Group Blocking Port 443

↓

Allow HTTPS

↓

Application Accessible
```

Packet analysis helped identify the exact failure point.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Wireshark fixes network problems."**

✅ **Correct:**

Wireshark only captures and analyzes packets. Engineers use the information to diagnose and resolve problems.

---

## ❌ Mistake 2

**"Wireshark only captures HTTP traffic."**

✅ **Correct:**

Wireshark can capture and analyze hundreds of protocols including TCP, UDP, DNS, ICMP, ARP, TLS, and many others.

---

## ❌ Mistake 3

**"Encrypted HTTPS traffic can always be read in Wireshark."**

✅ **Correct:**

Wireshark can capture encrypted HTTPS packets, but their contents are encrypted unless appropriate decryption keys are available.

---

## ❌ Mistake 4

**"AWS provides Wireshark as a managed service."**

✅ **Correct:**

AWS does not provide Wireshark as a managed service. Instead, services such as **Traffic Mirroring**, **VPC Flow Logs**, and **Reachability Analyzer** help analyze network traffic.

---

# 📝 Quick Revision

- Packet Capture records network traffic.
- Wireshark is a packet analyzer.
- Common filters:
  - `http`
  - `dns`
  - `tcp`
  - `udp`
  - `icmp`
  - `arp`
- Used for troubleshooting connectivity, latency, and security issues.
- AWS alternatives include VPC Flow Logs, Traffic Mirroring, and Reachability Analyzer.

---

# 💼 Interview Questions

### 1. What is Packet Capture?

**Answer:**

Packet Capture is the process of recording and analyzing network packets to troubleshoot connectivity, performance, and security issues.

---

### 2. What is Wireshark?

**Answer:**

Wireshark is a free, open-source network protocol analyzer used to capture and inspect network traffic in real time.

---

### 3. Why do Network Engineers use Wireshark?

**Answer:**

They use Wireshark to:

- Analyze network packets
- Troubleshoot connectivity issues
- Investigate security incidents
- Debug network applications
- Understand protocol behavior

---

### 4. Which protocols can Wireshark capture?

**Answer:**

Wireshark can capture many protocols, including:

- TCP
- UDP
- HTTP
- HTTPS (TLS)
- DNS
- ICMP
- ARP
- DHCP

---

### 5. Which AWS service is used for packet-level traffic analysis?

**Answer:**

**VPC Traffic Mirroring** allows packet traffic from EC2 instances to be mirrored to monitoring appliances for detailed packet analysis.

---

### 6. What is the difference between Wireshark and VPC Flow Logs?

**Answer:**

- **Wireshark:** Captures and analyzes individual network packets.
- **VPC Flow Logs:** Records metadata about network traffic (such as source, destination, ports, and accept/reject status) but does not capture packet contents.

---

# 13. AWS Network Troubleshooting

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand AWS Network Troubleshooting.
- Learn a step-by-step troubleshooting methodology.
- Identify common AWS networking issues.
- Troubleshoot EC2 connectivity.
- Use AWS networking tools effectively.
- Answer AWS Network Troubleshooting interview questions confidently.

---

# 📖 Introduction

Suppose your manager says:

> **"Our EC2 website is not opening."**

Can you immediately conclude that the EC2 instance is down?

❌ No.

In AWS,

many networking components work together.

A problem in **any one** of these components can stop communication.

As a Cloud Engineer,

you must check every component systematically.

---

# AWS Networking Components

A typical AWS network consists of:

```text
Internet

↓

Internet Gateway

↓

VPC

↓

Subnet

↓

Route Table

↓

Security Group

↓

Network ACL

↓

Elastic Network Interface (ENI)

↓

EC2 Instance
```

If any component is misconfigured,

communication may fail.

---

# AWS Network Troubleshooting Process

Follow this order:

```text
Problem Reported

↓

Check EC2 Status

↓

Check Security Group

↓

Check Network ACL

↓

Check Route Table

↓

Check Internet Gateway

↓

Check Public IP

↓

Check Application

↓

Problem Solved
```

Always troubleshoot step by step.

---

# Step 1 – Check EC2 Instance Status

Verify:

- Instance is Running
- System Status Checks Passed
- Instance Status Checks Passed

AWS Console

```text
EC2

↓

Instance State

↓

Running
```

If stopped,

start the instance.

---

# Step 2 – Check Security Group

Verify:

Inbound Rules

Example

```text
HTTP

80

0.0.0.0/0

✅
```

```text
HTTPS

443

0.0.0.0/0

✅
```

```text
SSH

22

Your IP

✅
```

If required ports are blocked,

users cannot access the application.

---

# Step 3 – Check Network ACL (NACL)

Remember:

Network ACLs are:

```text
Stateless
```

Both inbound and outbound rules must allow the traffic.

Example

```text
Inbound

Allow 80

✅
```

```text
Outbound

Allow Ephemeral Ports

✅
```

---

# Step 4 – Check Route Table

Public Subnet

Should contain:

```text
Destination

0.0.0.0/0

↓

Internet Gateway
```

Private Subnet

Should contain:

```text
0.0.0.0/0

↓

NAT Gateway
```

Missing routes prevent traffic from reaching its destination.

---

# Step 5 – Check Internet Gateway

For public instances:

Verify:

```text
Internet Gateway

↓

Attached to VPC

✅
```

Without an Internet Gateway,

public Internet access is impossible.

---

# Step 6 – Check Public IP

Verify the EC2 instance has:

- Public IPv4 Address

or

- Elastic IP

Without a public IP,

Internet users cannot directly reach the instance.

---

# Step 7 – Check the Application

Even if networking is correct,

the application must be running.

Example

```bash
systemctl status nginx
```

or

```bash
systemctl status httpd
```

If the web server is stopped,

the website will not open.

---

# Step 8 – Check DNS

If users access:

```text
www.company.com
```

Verify:

- Route 53 Record
- Public DNS Name
- Domain Configuration

Use

```bash
nslookup company.com
```

---

# Step 9 – Check VPC Flow Logs

VPC Flow Logs help determine whether traffic is:

```text
ACCEPT
```

or

```text
REJECT
```

Useful for identifying:

- Blocked Traffic
- Security Issues
- Network ACL Problems

---

# Step 10 – Check CloudWatch

CloudWatch helps monitor:

- EC2 Metrics
- Network Traffic
- CPU
- Memory *(with CloudWatch Agent)*
- Disk Usage *(with CloudWatch Agent)*

High utilization may indicate performance issues rather than networking problems.

---

# Common AWS Networking Issues

| Problem | Possible Cause |
|----------|----------------|
| Website Not Opening | Security Group |
| No Internet | Missing IGW |
| Private EC2 Cannot Download Updates | NAT Gateway Missing |
| SSH Failure | Port 22 Blocked |
| DNS Failure | Route 53 Issue |
| Slow Network | High Utilization or Congestion |
| Packet Loss | Network Issue |
| VPN Down | Tunnel Failure |

---

# AWS Troubleshooting Checklist

```text
✓ EC2 Running

↓

✓ Security Group

↓

✓ Network ACL

↓

✓ Route Table

↓

✓ Internet Gateway

↓

✓ Public IP

↓

✓ Application Running

↓

✓ DNS

↓

✓ Flow Logs

↓

✓ CloudWatch
```

---

# Real-Life Analogy 🏥

Imagine visiting a hospital.

Before treating a patient,

the doctor checks:

```text
Temperature

↓

Blood Pressure

↓

Heart Rate

↓

Tests

↓

Diagnosis
```

Similarly,

Cloud Engineers check every AWS networking component before identifying the root cause.

---

# AWS Perspective ☁️

Suppose users cannot access:

```text
https://company.com
```

Architecture

```text
Internet

↓

Route 53

↓

Internet Gateway

↓

Public Subnet

↓

Security Group

↓

EC2

↓

Nginx
```

Every component must function correctly for the application to be accessible.

---

# Real AWS Scenario

Problem

Users cannot access a website.

Troubleshooting

```text
EC2 Running

✅

↓

Security Group

Port 80 Open

✅

↓

Route Table

0.0.0.0/0 Missing

❌

↓

Add Route

↓

Website Working
```

The root cause was an incorrect Route Table.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"If the EC2 instance is running, networking must be correct."**

✅ **Correct:**

Networking also depends on Security Groups, NACLs, Route Tables, Internet Gateway, Public IPs, and the application.

---

## ❌ Mistake 2

**"Security Groups and NACLs behave the same."**

✅ **Correct:**

- Security Groups are **stateful**.
- Network ACLs are **stateless**.

---

## ❌ Mistake 3

**"A Public Subnet automatically provides Internet access."**

✅ **Correct:**

A Public Subnet also requires:

- Internet Gateway
- Route to `0.0.0.0/0`
- Public IP (or Elastic IP)

---

## ❌ Mistake 4

**"CloudWatch can replace VPC Flow Logs."**

✅ **Correct:**

CloudWatch monitors metrics and logs, while VPC Flow Logs record network traffic metadata. They complement each other.

---

# 📝 Quick Revision

- Check EC2 Status.
- Verify Security Groups.
- Verify Network ACLs.
- Verify Route Tables.
- Verify Internet Gateway.
- Verify Public IP / Elastic IP.
- Verify Application Service.
- Verify DNS.
- Use VPC Flow Logs.
- Monitor with CloudWatch.

---

# 💼 Interview Questions

### 1. What is the first step when troubleshooting an AWS networking issue?

**Answer:**

The first step is to verify that the EC2 instance is running and has passed both system and instance status checks.

---

### 2. Why might a public EC2 instance not be accessible?

**Answer:**

Possible reasons include:

- Security Group blocking traffic
- Network ACL blocking traffic
- Missing Internet Gateway
- Incorrect Route Table
- No Public IP or Elastic IP
- Web server not running

---

### 3. How do VPC Flow Logs help during troubleshooting?

**Answer:**

VPC Flow Logs record network traffic metadata, allowing engineers to determine whether traffic is accepted or rejected and identify potential networking issues.

---

### 4. Why should you check the Route Table?

**Answer:**

The Route Table determines where traffic is forwarded. Missing or incorrect routes can prevent communication with the Internet or other networks.

---

### 5. Which AWS service helps monitor EC2 network metrics?

**Answer:**

**Amazon CloudWatch** monitors metrics such as network traffic, CPU utilization, and disk performance (with the CloudWatch Agent for additional metrics).

---

### 6. Which AWS components should be checked when a website hosted on EC2 is not opening?

**Answer:**

Check:

- EC2 Instance Status
- Security Group
- Network ACL
- Route Table
- Internet Gateway
- Public IP / Elastic IP
- Web Server (Apache/Nginx)
- Route 53 (if using a domain)
- VPC Flow Logs
- CloudWatch

---

# 14. Common AWS Networking Issues

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Understand common AWS networking issues.
- Identify the root causes of connectivity problems.
- Learn how to troubleshoot AWS networking.
- Understand best practices for resolving issues.
- Answer AWS networking interview questions confidently.

---

# 📖 Introduction

In AWS,

most networking issues are **not caused by EC2**.

Instead,

they usually occur because of:

- Security Groups
- Network ACLs
- Route Tables
- Internet Gateway
- NAT Gateway
- DNS
- Load Balancer

A Cloud Engineer should always troubleshoot methodically instead of guessing.

---

# Common AWS Networking Issues

```text
AWS Networking Issues

│

├── EC2 Not Reachable

├── No Internet Access

├── SSH Connection Failed

├── Website Not Opening

├── DNS Resolution Failure

├── NAT Gateway Issues

├── Security Group Misconfiguration

├── Network ACL Blocking

├── Route Table Issues

└── Load Balancer Connectivity Problems
```

---

# 1. EC2 Not Reachable

Users cannot connect to the EC2 instance.

Possible Causes

- EC2 Stopped
- Wrong Security Group
- Missing Public IP
- Missing Internet Gateway
- Incorrect Route Table
- SSH/RDP Service Stopped

---

## Troubleshooting

Check:

```text
EC2 Running

↓

Public IP

↓

Security Group

↓

Route Table

↓

Internet Gateway
```

---

# 2. No Internet Access

EC2 cannot access:

- Internet
- Software Repositories
- AWS APIs

---

## Public Subnet

Verify:

```text
0.0.0.0/0

↓

Internet Gateway
```

---

## Private Subnet

Verify:

```text
0.0.0.0/0

↓

NAT Gateway
```

---

# 3. SSH Connection Failed

Linux EC2

```bash
ssh -i key.pem ec2-user@Public-IP
```

Connection fails.

Possible Causes

- Port 22 Blocked
- Wrong Key Pair
- Incorrect Username
- Instance Not Running
- NACL Blocking SSH

---

## Troubleshooting

Verify:

- Port 22 Open
- Correct Key Pair
- Correct User
- Public IP
- Internet Gateway

---

# 4. Website Not Opening

Users cannot access:

```text
http://Public-IP
```

Possible Causes

- Port 80 Closed
- Apache/Nginx Not Running
- Route Table Issue
- NACL Blocking
- Wrong Target Group

---

## Troubleshooting

Check:

```bash
systemctl status nginx
```

or

```bash
systemctl status httpd
```

Verify:

- Security Group
- Route Table
- Load Balancer
- Application Logs

---

# 5. DNS Resolution Failure

Domain

```text
www.company.com
```

does not resolve.

Possible Causes

- Missing Route 53 Record
- Incorrect Hosted Zone
- Wrong Name Server
- DNS Cache

---

## Troubleshooting

Use

```bash
nslookup company.com
```

Verify:

- Route 53 Records
- Public Hosted Zone
- Domain Registration

---

# 6. NAT Gateway Issues

Private EC2 cannot:

- Download Packages
- Access Internet
- Connect to AWS APIs

Possible Causes

- NAT Gateway Deleted
- Route Missing
- NAT in Wrong Subnet
- Elastic IP Missing

---

## Troubleshooting

Verify:

```text
Private Route Table

↓

0.0.0.0/0

↓

NAT Gateway
```

---

# 7. Security Group Misconfiguration

Example

```text
HTTP

Port 80

Blocked
```

Result

↓

Website Inaccessible

---

## Troubleshooting

Verify:

Inbound Rules

```text
HTTP

80

HTTPS

443

SSH

22
```

Open only the required ports.

---

# 8. Network ACL Blocking

NACL

```text
Inbound

Allow

↓

Outbound

Deny
```

Result

↓

Traffic Blocked

Remember:

Network ACLs are **stateless**, so both inbound and outbound rules must allow the traffic.

---

# 9. Route Table Issues

Example

```text
Public Subnet

↓

No Route

0.0.0.0/0
```

Result

↓

No Internet Access

---

## Troubleshooting

Verify

```text
Destination

0.0.0.0/0

↓

Internet Gateway
```

---

# 10. Load Balancer Connectivity Issues

Users cannot access the application through the Load Balancer.

Possible Causes

- Target Group Unhealthy
- Health Check Failure
- Security Group Blocking
- Wrong Listener Configuration

---

## Troubleshooting

Check:

- Target Group Health
- Health Check Path
- Listener Rules
- Security Groups

---

# Common AWS Issue Summary

| Issue | Common Cause |
|--------|--------------|
| EC2 Not Reachable | SG, Route Table, Public IP |
| No Internet | IGW/NAT Missing |
| SSH Failure | Port 22 Blocked |
| Website Not Opening | Port 80/443 Closed |
| DNS Failure | Route 53 Issue |
| NAT Failure | Missing NAT Gateway |
| Security Group Issue | Wrong Rules |
| NACL Issue | Inbound/Outbound Deny |
| Route Issue | Missing Default Route |
| ALB Issue | Unhealthy Targets |

---

# AWS Troubleshooting Checklist

```text
✓ EC2 Running

↓

✓ Public IP

↓

✓ Internet Gateway

↓

✓ Route Table

↓

✓ Security Group

↓

✓ Network ACL

↓

✓ NAT Gateway

↓

✓ Route 53

↓

✓ Load Balancer

↓

✓ Application Running
```

---

# Real-Life Analogy 🏢

Imagine an office building.

To enter,

you need:

```text
Road

↓

Main Gate

↓

Security Guard

↓

Reception

↓

Lift

↓

Office
```

If any one step fails,

you cannot reach your office.

AWS networking works the same way.

Every networking component must function correctly.

---

# AWS Perspective ☁️

Typical Internet Traffic

```text
Internet

↓

Internet Gateway

↓

Route Table

↓

Public Subnet

↓

Security Group

↓

EC2

↓

Web Server
```

Private Traffic

```text
Private EC2

↓

Route Table

↓

NAT Gateway

↓

Internet
```

Every component must be correctly configured.

---

# Real AWS Scenario

Problem

Users cannot open:

```text
https://company.com
```

Troubleshooting

```text
EC2 Running

✅

↓

ALB Healthy

❌

↓

Health Check Path Wrong

↓

Correct Path

↓

Targets Healthy

↓

Website Working
```

The issue was the Load Balancer health check configuration.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Opening Port 80 in the Security Group guarantees website access."**

✅ **Correct:**

The application must also be running, and Route Tables, Internet Gateway, NACLs, and Load Balancer settings must be correct.

---

## ❌ Mistake 2

**"Private EC2 instances can access the Internet without NAT Gateway."**

✅ **Correct:**

Private subnets require a **NAT Gateway** (or another outbound solution) for Internet access.

---

## ❌ Mistake 3

**"Security Groups and Network ACLs work the same way."**

✅ **Correct:**

- Security Groups → Stateful
- Network ACLs → Stateless

---

## ❌ Mistake 4

**"If Route 53 resolves correctly, the website must be working."**

✅ **Correct:**

DNS resolution only points users to the destination. The web server, Load Balancer, Security Groups, and application must also function correctly.

---

# 📝 Quick Revision

- Check EC2 status.
- Verify Public IP.
- Check Internet Gateway.
- Verify Route Tables.
- Check Security Groups.
- Check Network ACLs.
- Verify NAT Gateway.
- Verify Route 53.
- Check Load Balancer.
- Ensure the application is running.

---

# 💼 Interview Questions

### 1. Why is an EC2 instance not reachable from the Internet?

**Answer:**

Possible reasons include:

- Instance stopped
- Missing Public IP
- Security Group blocking traffic
- Incorrect Route Table
- Internet Gateway not attached
- Network ACL blocking traffic

---

### 2. Why can't a private EC2 instance access the Internet?

**Answer:**

A private EC2 instance usually requires:

- A NAT Gateway
- A Route Table with `0.0.0.0/0` pointing to the NAT Gateway

Without these, outbound Internet access will fail.

---

### 3. Why does SSH fail even when the EC2 instance is running?

**Answer:**

Possible reasons include:

- Port 22 blocked
- Wrong key pair
- Incorrect username
- Network ACL blocking traffic
- No Public IP
- SSH service not running

---

### 4. How do you troubleshoot a website that is not opening?

**Answer:**

Check:

- EC2 Status
- Web Server (Apache/Nginx)
- Security Groups
- Network ACLs
- Route Tables
- Internet Gateway
- Load Balancer
- Route 53

---

### 5. Why is a Load Balancer showing unhealthy targets?

**Answer:**

Common causes include:

- Incorrect Health Check Path
- Application not running
- Security Group blocking health checks
- Wrong port configuration

---

### 6. Which AWS networking components are most commonly involved in troubleshooting?

**Answer:**

- Amazon VPC
- Route Tables
- Internet Gateway
- NAT Gateway
- Security Groups
- Network ACLs
- Route 53
- Elastic Load Balancer
- EC2
- VPC Flow Logs

---

# 15. Network Troubleshooting Best Practices

---

## 🎯 Learning Objectives

After completing this topic, you will be able to:

- Learn network troubleshooting best practices.
- Understand systematic troubleshooting.
- Minimize downtime.
- Improve troubleshooting efficiency.
- Apply best practices in AWS environments.
- Answer interview questions confidently.

---

# 📖 Introduction

Two Cloud Engineers are troubleshooting the same problem.

Engineer A

```text
Randomly Restarts EC2

↓

Changes Security Groups

↓

Deletes Route Table

↓

Still Doesn't Work
```

Engineer B

```text
Collect Information

↓

Analyze Problem

↓

Find Root Cause

↓

Apply Correct Fix

↓

Problem Solved
```

Who is the better engineer?

✅ **Engineer B**

Professional Cloud Engineers always follow best practices instead of guessing.

---

# What are Troubleshooting Best Practices?

Troubleshooting Best Practices are proven methods that help engineers identify, diagnose, and resolve problems quickly while minimizing risk.

---

# 1. Understand the Problem First

Never start changing configurations immediately.

Ask questions:

- What is the issue?
- When did it start?
- Who is affected?
- Has anything changed recently?

Understanding the problem saves time.

---

# 2. Gather Information

Collect information before making changes.

Check:

- Error Messages
- Logs
- Monitoring Data
- User Reports
- Recent Changes

Use tools like:

- Ping
- Traceroute
- nslookup
- netstat
- CloudWatch
- VPC Flow Logs

---

# 3. Follow a Layered Approach

Troubleshoot from the lowest possible layer upward.

Example

```text
Physical

↓

Network

↓

Transport

↓

Application
```

Using the OSI model prevents missing important issues.

---

# 4. Check the Simple Things First

Always verify basic configurations.

Examples

- Cable Connected
- Wi-Fi Enabled
- Correct IP Address
- Correct Gateway
- DNS Working
- EC2 Running

Many issues are caused by simple mistakes.

---

# 5. Make One Change at a Time

Avoid changing multiple configurations simultaneously.

Example

❌ Bad Practice

```text
Change Route Table

+

Change Security Group

+

Restart EC2

+

Modify DNS
```

You won't know which change solved the issue.

---

✅ Good Practice

```text
One Change

↓

Test

↓

Next Change (if needed)
```

---

# 6. Verify the Solution

After applying a fix,

always confirm that:

- Users can access the service.
- Applications work correctly.
- No new issues were introduced.

Never assume the problem is solved.

---

# 7. Document Everything

Record:

- Problem
- Root Cause
- Solution
- Commands Used
- Time Taken

Documentation improves future troubleshooting.

---

# 8. Use Monitoring Tools

Monitor continuously.

Examples

AWS

- CloudWatch
- CloudTrail
- VPC Flow Logs
- GuardDuty

Monitoring helps detect issues early.

---

# 9. Understand Recent Changes

Many problems occur after:

- Software Updates
- Firewall Changes
- Route Changes
- Security Group Changes
- Application Deployment

Always ask:

```text
What Changed?
```

---

# 10. Know When to Escalate

If the issue cannot be resolved,

escalate with:

- Clear Findings
- Logs
- Error Messages
- Troubleshooting Steps Already Performed

This saves time for higher-level support teams.

---

# AWS Troubleshooting Best Practices

When troubleshooting AWS,

always verify:

```text
EC2

↓

Security Group

↓

Network ACL

↓

Route Table

↓

Internet Gateway

↓

NAT Gateway

↓

DNS

↓

Application

↓

CloudWatch

↓

Flow Logs
```

This checklist covers the most common networking issues.

---

# Recommended Troubleshooting Workflow

```text
Identify Problem

↓

Collect Information

↓

Analyze

↓

Apply One Fix

↓

Test

↓

Monitor

↓

Document
```

This workflow is used by professional Cloud Engineers.

---

# Real-Life Analogy 🏥

Imagine a doctor treating a patient.

The doctor:

```text
Checks Symptoms

↓

Performs Tests

↓

Finds Root Cause

↓

Prescribes Medicine

↓

Monitors Recovery
```

Doctors don't guess.

Neither should Network Engineers.

---

# AWS Perspective ☁️

Suppose users cannot access an application.

Architecture

```text
Internet

↓

Route 53

↓

Application Load Balancer

↓

EC2

↓

Database
```

Best Practice

```text
Check DNS

↓

Check ALB

↓

Check Security Groups

↓

Check EC2

↓

Check Application Logs

↓

Check Database
```

Work through each layer systematically.

---

# Real AWS Scenario

Problem

```text
Users Cannot Access Website
```

Engineer follows checklist

```text
EC2 Running

✅

↓

Security Group

✅

↓

Route Table

✅

↓

Application Service

❌

↓

Start Nginx

↓

Website Working
```

The issue was the application service, not AWS networking.

---

# Common Interview Mistakes ⚠️

## ❌ Mistake 1

**"Restarting resources is the first troubleshooting step."**

✅ **Correct:**

Always identify the root cause before restarting or changing resources.

---

## ❌ Mistake 2

**"Changing multiple settings saves time."**

✅ **Correct:**

Make one change at a time to accurately identify what resolved the issue.

---

## ❌ Mistake 3

**"Documentation is optional."**

✅ **Correct:**

Documentation is essential for audits, future troubleshooting, and knowledge sharing.

---

## ❌ Mistake 4

**"If the issue is fixed, monitoring is no longer needed."**

✅ **Correct:**

Continue monitoring after the fix to ensure the issue does not reoccur.

---

# 📝 Quick Revision

- Understand the problem first.
- Gather information.
- Follow the OSI troubleshooting approach.
- Check simple things first.
- Make one change at a time.
- Verify the solution.
- Document everything.
- Monitor continuously.
- Review recent changes.
- Escalate with proper evidence when necessary.

---

# 💼 Interview Questions

### 1. What is the first rule of troubleshooting?

**Answer:**

Understand the problem before making any changes. Gather information and identify the root cause.

---

### 2. Why should you make only one change at a time?

**Answer:**

It helps identify exactly which change resolved the issue and prevents introducing multiple new problems.

---

### 3. Why is documentation important?

**Answer:**

Documentation records the issue, root cause, and solution, making future troubleshooting faster and improving team knowledge.

---

### 4. Which AWS services help during troubleshooting?

**Answer:**

Common AWS troubleshooting services include:

- Amazon CloudWatch
- AWS CloudTrail
- VPC Flow Logs
- Amazon Route 53
- AWS Reachability Analyzer
- AWS Systems Manager

---

### 5. Why should engineers review recent changes?

**Answer:**

Many outages occur after configuration changes, software updates, deployments, or security modifications. Reviewing recent changes often helps identify the root cause quickly.

---

### 6. What is the recommended troubleshooting workflow?

**Answer:**

```text
Identify Problem

↓

Collect Information

↓

Analyze Root Cause

↓

Apply One Fix

↓

Test

↓

Monitor

↓

Document
```

This structured approach minimizes downtime and improves troubleshooting efficiency.

---

