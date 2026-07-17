# 🐧 Linux Fundamentals

> Build a strong Linux foundation before working with AWS Cloud services.

---

## 📚 Table of Contents

- [Introduction to Linux](#-introduction-to-linux)
- [What is an Operating System?](#-what-is-an-operating-system)
- [Why Linux for Cloud Computing?](#-why-linux-for-cloud-computing)
- [Linux Architecture](#-linux-architecture)
- [Linux Kernel](#-linux-kernel)
- [Popular Linux Distributions](#-popular-linux-distributions)
- [Linux vs Windows](#-linux-vs-windows)
- [Real-World AWS Example](#-real-world-aws-example)
- [Key Takeaways](#-key-takeaways)
- [Interview Questions](#-interview-questions)

---

# 📖 Introduction to Linux

Linux is an **open-source operating system** that manages computer hardware and software resources while providing services for applications.

It is the most widely used operating system for:

- ☁️ Cloud Computing
- 🌐 Web Servers
- 🛢️ Database Servers
- 🐳 Docker Containers
- ☸️ Kubernetes Clusters
- 🔒 Cyber Security
- 🤖 Embedded Systems
- 💻 Supercomputers

Today, Linux powers **millions of servers** around the world.

---

# 💻 What is an Operating System?

An **Operating System (OS)** is software that acts as a bridge between the user and the computer hardware.

It is responsible for:

- Managing CPU
- Managing Memory (RAM)
- Managing Storage
- Managing Files
- Managing Processes
- Managing Devices
- Running Applications

Without an operating system, a computer cannot function properly.

---

# ☁️ Why Linux for Cloud Computing?

Cloud providers heavily rely on Linux because it is:

- ✅ Open Source
- ✅ Secure
- ✅ Stable
- ✅ Lightweight
- ✅ Fast
- ✅ Highly Customizable
- ✅ Cost Effective
- ✅ Easy to Automate

Most cloud servers use Linux.

Examples:

- Amazon Linux
- Red Hat Enterprise Linux (RHEL)
- Ubuntu Server
- Debian
- SUSE Linux

---

# 🏗️ Linux Architecture

Linux follows a layered architecture.

```text
+----------------------+
|        User          |
+----------------------+
           │
           ▼
+----------------------+
|    Applications      |
+----------------------+
           │
           ▼
+----------------------+
|    Shell (Bash)      |
+----------------------+
           │
           ▼
+----------------------+
|       Kernel         |
+----------------------+
           │
           ▼
+----------------------+
|      Hardware        |
+----------------------+
```

### Components

### 👤 User

The person interacting with the computer.

---

### 🖥️ Applications

Programs like:

- Chrome
- VS Code
- Firefox
- Docker

---

### 🐚 Shell

The Shell accepts commands from the user and passes them to the Linux Kernel.

Example:

```bash
ls
pwd
mkdir project
```

---

### ❤️ Kernel

The Kernel is the **core of the Linux Operating System**.

It is responsible for:

- CPU Management
- Memory Management
- Process Management
- Device Management
- File Management
- Network Management

Without the Kernel, Linux cannot communicate with hardware.

---

### 💾 Hardware

Physical components like:

- CPU
- RAM
- Hard Disk
- Keyboard
- Network Card

---

# ❤️ Linux Kernel

The Kernel is the heart of Linux.

It controls communication between software and hardware.

### Responsibilities

- Process Management
- Memory Management
- File Management
- Device Management
- CPU Scheduling
- Networking

Example:

```text
User
   │
   ▼
Shell
   │
   ▼
Kernel
   │
   ▼
Hardware
```

---

# 📦 Popular Linux Distributions

| Distribution | Common Usage |
|--------------|--------------|
| Red Hat Enterprise Linux (RHEL) | Enterprise Servers |
| Amazon Linux | AWS EC2 |
| Ubuntu | Servers & Development |
| Debian | Stable Servers |
| SUSE Linux | Enterprise |
| CentOS Stream | Development |

---

# ⚔️ Linux vs Windows

| Linux | Windows |
|--------|----------|
| Open Source | Proprietary |
| More Secure | More Malware Targeted |
| Lightweight | Resource Intensive |
| CLI Friendly | GUI Focused |
| Preferred for Servers | Preferred for Personal Computers |

---

# ☁️ Real-World AWS Example

Suppose you launch an EC2 instance.

You may choose one of these operating systems:

- Amazon Linux
- Red Hat Enterprise Linux (RHEL)
- Ubuntu Server

After connecting using SSH:

```bash
ssh -i my-key.pem ec2-user@PUBLIC_IP
```

You'll use Linux commands to:

- Manage files
- Install software
- Configure services
- Monitor the server
- Troubleshoot issues

Linux is the foundation of AWS server administration.

---

# 📝 Key Takeaways

- Linux is an open-source operating system.
- The Kernel is the heart of Linux.
- Linux is the preferred operating system for cloud servers.
- Most AWS EC2 instances run Linux.
- Linux is secure, stable, and lightweight.
- Learning Linux is essential for becoming an AWS Cloud Engineer.

---

# 🎯 Interview Questions

### 1. What is Linux?

Linux is an open-source operating system that manages computer hardware and software resources.

---

### 2. Why is Linux widely used in Cloud Computing?

Because it is secure, stable, lightweight, cost-effective, and easy to automate.

---

### 3. What is the Linux Kernel?

The Kernel is the core component of Linux that manages communication between software and hardware.

---

### 4. Name some popular Linux distributions.

- Amazon Linux
- Red Hat Enterprise Linux (RHEL)
- Ubuntu
- Debian
- SUSE Linux

---

### 5. Why do AWS Cloud Engineers need Linux?

Because most AWS EC2 instances run Linux, and Linux commands are required to manage cloud servers.

---
