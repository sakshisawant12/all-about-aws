# 💻 Introduction to AWS Command Line Interface (AWS CLI)

> **Chapter 1** | AWS Command Line Interface (AWS CLI)

---

## 📖 Table of Contents

- What is AWS CLI?
- Why Do We Need AWS CLI?
- How AWS CLI Works
- Features of AWS CLI
- AWS CLI Versions
- AWS CLI vs AWS Management Console
- Advantages of AWS CLI
- Real-World Example
- Key Takeaways
- Interview Questions

---

# What is AWS CLI?

**AWS Command Line Interface (AWS CLI)** is a command-line tool that allows you to interact with AWS services using commands instead of the AWS Management Console.

With AWS CLI, you can create, manage, and automate AWS resources directly from your terminal or command prompt.

---

# Why Do We Need AWS CLI?

While the AWS Management Console provides a graphical interface, AWS CLI offers a faster and more efficient way to manage AWS resources.

AWS CLI is commonly used for:

- Automating repetitive tasks
- Managing AWS resources quickly
- Writing scripts
- Working with Infrastructure as Code (IaC)
- Managing AWS without opening a web browser

---

# How AWS CLI Works

AWS CLI sends your commands to AWS service APIs.

```
User
   │
   ▼
AWS CLI
   │
   ▼
AWS API
   │
   ▼
AWS Services
```

Example:

```
aws s3 ls
```

AWS CLI sends a request to the Amazon S3 API and displays the list of S3 buckets.

---

# Features of AWS CLI

✅ Easy to Use

Run AWS commands directly from the terminal.

---

✅ Cross-Platform

Supports:

- Windows
- Linux
- macOS

---

✅ Automation

Works with:

- Bash Scripts
- PowerShell
- Shell Scripts

---

✅ Supports Almost All AWS Services

Examples:

- IAM
- EC2
- S3
- VPC
- RDS
- Lambda
- CloudWatch

---

✅ Secure Authentication

Uses:

- IAM Users
- IAM Roles
- Temporary Credentials
- AWS STS

---

# AWS CLI Versions

There are two major versions.

| Version | Status |
|----------|--------|
| AWS CLI Version 1 | Older version |
| AWS CLI Version 2 | Recommended and actively maintained |

> [!TIP]
> Always use **AWS CLI Version 2**, as it includes the latest features, improved security, and better performance.

---

# AWS CLI vs AWS Management Console

| AWS CLI | AWS Management Console |
|----------|------------------------|
| Command-line interface | Graphical web interface |
| Faster for repetitive tasks | Easier for beginners |
| Supports automation | Manual operations |
| Script-friendly | Point-and-click interface |

---

# Advantages of AWS CLI

- Faster resource management
- Easy automation
- Reduces manual work
- Supports scripting
- Works on multiple operating systems
- Ideal for Cloud Engineers and DevOps Engineers

---

# Real-World Example

Imagine you need to create 50 Amazon S3 buckets.

### Using AWS Management Console

- Sign in
- Click Create Bucket
- Enter details
- Repeat 50 times

This process is slow and repetitive.

---

### Using AWS CLI

Run a command or script to automate the creation process.

Benefits:

- Faster execution
- Less manual effort
- Consistent configuration
- Easy to repeat

---

# Common AWS CLI Use Cases

AWS CLI is commonly used to:

- Create and manage EC2 instances
- Upload files to Amazon S3
- Manage IAM users and roles
- Monitor AWS resources
- Automate infrastructure tasks
- Retrieve AWS account information

---

# Key Takeaways

- AWS CLI is a command-line tool for managing AWS resources.
- It communicates directly with AWS service APIs.
- AWS CLI supports automation and scripting.
- It is available for Windows, Linux, and macOS.
- AWS CLI Version 2 is the recommended version.

---

# Quick Summary

| Term | Description |
|------|-------------|
| AWS CLI | Command-line tool for AWS |
| Interface | Terminal / Command Prompt |
| Uses | Automation and resource management |
| Latest Version | AWS CLI Version 2 |
| Works With | Almost all AWS services |

---

# Interview Questions

### 1. What is AWS CLI?

### 2. Why do we use AWS CLI?

### 3. How does AWS CLI communicate with AWS services?

### 4. What are the advantages of AWS CLI?

### 5. Which operating systems support AWS CLI?

### 6. What is the difference between AWS CLI and the AWS Management Console?

### 7. Which AWS CLI version is recommended?

### 8. Can AWS CLI be used for automation?

### 9. Name three AWS services that can be managed using AWS CLI.

### 10. Why do Cloud Engineers prefer AWS CLI?

---

