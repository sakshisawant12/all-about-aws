# 🎭 IAM Roles and AWS Security Token Service (STS)

> **Chapter 6** | AWS Identity and Access Management (IAM)

---

## 📖 Table of Contents

- What is an IAM Role?
- Why Do We Need IAM Roles?
- What is AWS STS?
- How IAM Roles Work
- Temporary Credentials
- Common Use Cases
- IAM Role vs IAM User
- Best Practices
- Key Takeaways
- Interview Questions

---

# What is an IAM Role?

An **IAM Role** is an AWS identity that grants **temporary permissions** to trusted users, applications, or AWS services.

Unlike an IAM User, a Role **does not have**:

- Username
- Password
- Permanent Access Keys

Instead, it is **assumed** whenever access is required.

---

# Why Do We Need IAM Roles?

Storing long-term AWS Access Keys is risky because they can:

- Be leaked
- Be stolen
- Be accidentally shared

IAM Roles eliminate this risk by providing **temporary credentials**.

---

# What is AWS Security Token Service (STS)?

**AWS Security Token Service (STS)** is the AWS service that creates **temporary security credentials**.

These credentials are valid only for a limited period.

After they expire, AWS automatically invalidates them.

---

# How IAM Roles Work

```
Application / User
        │
        ▼
Assume IAM Role
        │
        ▼
AWS STS
Generates Temporary Credentials
        │
        ▼
Access AWS Resources
```

---

# Temporary Credentials

Temporary credentials include:

- Access Key ID
- Secret Access Key
- Session Token

Unlike IAM User credentials, these credentials automatically expire after a specified duration.

---

# Real-World Example

Imagine an EC2 instance needs to read files from an Amazon S3 bucket.

❌ Bad Practice

```
EC2
 │
 └── Store Access Keys
```

Problems:

- Keys may leak
- Difficult to rotate
- Security risk

---

✅ Best Practice

```
EC2
 │
 ▼
IAM Role
 │
 ▼
AWS STS
 │
 ▼
Temporary Credentials
 │
 ▼
Amazon S3
```

AWS automatically provides secure temporary credentials to the EC2 instance.

---

# Common IAM Role Use Cases

## EC2 → S3

An EC2 instance reads or writes objects in an S3 bucket.

---

## Lambda → DynamoDB

A Lambda function stores data in a DynamoDB table.

---

## ECS Tasks

Containers access AWS services securely.

---

## Cross-Account Access

Users from one AWS account temporarily access resources in another AWS account.

---

## Identity Federation

External users authenticated by Google, Microsoft Entra ID (formerly Azure AD), or another identity provider assume IAM Roles to access AWS resources.

---

# IAM Role vs IAM User

| Feature | IAM User | IAM Role |
|----------|----------|----------|
| Username | ✅ Yes | ❌ No |
| Password | ✅ Yes | ❌ No |
| Access Keys | Permanent | Temporary |
| Credentials Expire | ❌ No | ✅ Yes |
| Used By | People & Applications | AWS Services, Applications, Federated Users |

---

# Advantages of IAM Roles

- No long-term credentials
- More secure than Access Keys
- Automatically rotated credentials
- Supports cross-account access
- Ideal for AWS services

---

# Best Practices

- Prefer IAM Roles over Access Keys.
- Assign IAM Roles to EC2, Lambda, and ECS.
- Grant only the permissions required.
- Use short-lived temporary credentials whenever possible.
- Regularly review IAM Role permissions.

---

# Key Takeaways

- IAM Roles provide temporary permissions.
- AWS STS generates temporary security credentials.
- Roles improve security by eliminating long-term Access Keys.
- Most AWS services use IAM Roles for secure access.
- Temporary credentials automatically expire.

---

# Quick Summary

| Term | Meaning |
|------|---------|
| IAM Role | Temporary AWS identity |
| AWS STS | Generates temporary credentials |
| Temporary Credentials | Access Key, Secret Key, Session Token |
| Common Use | EC2, Lambda, ECS, Cross-Account Access |

---

# Interview Questions

### 1. What is an IAM Role?

### 2. What is AWS STS?

### 3. Why are IAM Roles more secure than IAM Users with Access Keys?

### 4. What credentials does STS generate?

### 5. Can IAM Roles have passwords?

### 6. Name three AWS services that commonly use IAM Roles.

### 7. What is Cross-Account Access?

### 8. Do temporary credentials expire?

### 9. What is the purpose of the Session Token?

### 10. Explain IAM Roles and STS with a real-world example.

---
