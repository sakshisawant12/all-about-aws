# 👥 IAM Users, Groups, and Roles

> **Chapter 2** | AWS Identity and Access Management (IAM)

---

## 📖 Table of Contents

- What is an IAM User?
- What is an IAM Group?
- What is an IAM Role?
- IAM User vs Group vs Role
- Real-World Example
- Best Practices
- Key Takeaways
- Interview Questions

---

# What is an IAM User?

An **IAM User** is an identity created within an AWS account that represents a **person or an application**.

Each IAM User has its own credentials and permissions to access AWS resources.

### An IAM User can have:

- 👤 Username
- 🔑 Password (for AWS Management Console)
- 🗝️ Access Keys (for AWS CLI/SDK)
- 📜 Permissions through IAM Policies

### Example

```
AWS Account
    │
    ├── John (IAM User)
    ├── Alice (IAM User)
    └── David (IAM User)
```

---

# Why Do We Create IAM Users?

Instead of sharing the AWS Root Account, every individual should have their own IAM User.

Benefits include:

- Better security
- Individual login credentials
- Activity tracking
- Fine-grained access control

---

# What is an IAM Group?

An **IAM Group** is a collection of IAM Users.

Groups help you manage permissions for multiple users at once.

Instead of attaching permissions to every user individually, attach them to the group.

### Example

```
Developers Group

├── John
├── Alice
├── David
└── Priya
```

Attach one policy to the **Developers** group, and every member receives those permissions automatically.

---

# Advantages of IAM Groups

- Easier permission management
- Consistent access control
- Simplifies onboarding new employees
- Reduces administrative work

---

# What is an IAM Role?

An **IAM Role** is an AWS identity that provides **temporary permissions**.

Unlike IAM Users, IAM Roles do **not** have:

- Username
- Password
- Permanent Access Keys

Roles are assumed by trusted users, AWS services, or applications when access is required.

---

# Why Do We Use IAM Roles?

IAM Roles are commonly used when:

- EC2 needs access to S3
- Lambda accesses DynamoDB
- Cross-account access is required
- Temporary permissions are needed
- Federated users sign in from external identity providers

---

# Example of an IAM Role

```
EC2 Instance
      │
      ▼
Assume IAM Role
      │
      ▼
Read Objects from Amazon S3
```

Instead of storing Access Keys on the EC2 instance, attach an IAM Role.

AWS automatically provides temporary credentials.

---

# IAM User vs IAM Group vs IAM Role

| Feature | IAM User | IAM Group | IAM Role |
|----------|----------|-----------|----------|
| Represents | Person/Application | Collection of Users | Temporary Identity |
| Login Credentials | ✅ Yes | ❌ No | ❌ No |
| Password | ✅ | ❌ | ❌ |
| Access Keys | ✅ | ❌ | ❌ |
| Policies Attached | ✅ | ✅ | ✅ |
| Temporary Credentials | ❌ | ❌ | ✅ |
| Common Use | Employees | Teams | AWS Services & Temporary Access |

---

# Real-World Example

Imagine a company with three departments.

## 👨‍💻 Development Team

Users:

- John
- Alice
- Priya

They belong to the **Developers Group**.

Permissions:

- Launch EC2 Instances
- Access S3 Buckets
- View CloudWatch Logs

---

## 👨‍💼 Finance Team

Users:

- Sarah
- Mike

They belong to the **Finance Group**.

Permissions:

- View Billing Dashboard
- Download Cost Reports

---

## 🤖 EC2 Instance

The EC2 server needs to upload logs to Amazon S3.

Instead of storing AWS Access Keys:

- Create an IAM Role
- Attach the required S3 policy
- Assign the Role to the EC2 instance

AWS automatically provides temporary credentials.

---

# Best Practices

- Create individual IAM Users for each person.
- Never share AWS Root Account credentials.
- Use IAM Groups for users with similar job roles.
- Prefer IAM Roles over Access Keys whenever possible.
- Grant only the permissions that are required (Principle of Least Privilege).
- Regularly remove unused users and roles.

---

# Key Takeaways

- IAM Users represent individual identities.
- IAM Groups simplify permission management.
- IAM Roles provide temporary credentials.
- AWS services commonly use IAM Roles.
- Avoid using long-term Access Keys when a Role can be used.

---

# Quick Summary

| Component | Purpose |
|-----------|---------|
| IAM User | Represents a person or application |
| IAM Group | Organizes users with similar permissions |
| IAM Role | Grants temporary permissions to trusted entities |

---

# Interview Questions

### 1. What is an IAM User?

### 2. What is an IAM Group?

### 3. What is an IAM Role?

### 4. What is the difference between an IAM User and an IAM Role?

### 5. Can one IAM User belong to multiple Groups?

### 6. Why are IAM Roles preferred over Access Keys?

### 7. Which AWS services commonly use IAM Roles?

### 8. Can an IAM Group contain another IAM Group?

### 9. Does an IAM Role have permanent credentials?

### 10. Explain a real-world use case for IAM Roles.

---
