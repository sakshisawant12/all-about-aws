# 🔐 Introduction to AWS Identity and Access Management (IAM)

> **Chapter 1** | AWS Identity and Access Management (IAM)

---

## 📖 Table of Contents

- What is IAM?
- Why Do We Need IAM?
- Features of IAM
- IAM Components
- Authentication vs Authorization
- How IAM Works
- Real-World Example
- Benefits of IAM
- Key Points
- Interview Questions

---

# What is IAM?

**AWS Identity and Access Management (IAM)** is a global AWS service that helps you **securely manage access** to AWS resources.

It allows you to decide:

- Who can access AWS
- What resources they can access
- What actions they can perform
- When and under which conditions they can access those resources

IAM follows the **Principle of Least Privilege**, meaning users should receive only the permissions required to perform their tasks.

---

# Why Do We Need IAM?

Without IAM:

- Everyone would use the AWS Root Account.
- Anyone could delete resources accidentally.
- Sensitive information could be exposed.
- There would be no permission control.

With IAM:

- Every user gets their own login.
- Permissions can be controlled.
- Access is secure.
- Activities are traceable.

---

# Features of IAM

✅ Global Service

✅ Free to Use

✅ Fine-Grained Permissions

✅ Multi-Factor Authentication (MFA)

✅ Temporary Credentials

✅ Identity Federation

✅ Role-Based Access Control (RBAC)

---

# IAM Components

| Component | Description |
|-----------|-------------|
| Users | Individual identities |
| Groups | Collection of users |
| Roles | Temporary permissions |
| Policies | JSON permission documents |
| MFA | Extra security layer |

---

# Authentication vs Authorization

| Authentication | Authorization |
|---------------|--------------|
| Verifies identity | Determines permissions |
| Username & Password | IAM Policies |
| MFA | Allow / Deny Actions |

---

# How IAM Works

```text
User
   │
   ▼
Authentication
   │
   ▼
IAM Policy Evaluation
   │
   ▼
Allow / Deny
   │
   ▼
AWS Resource
```

---

# Real-World Example

Imagine a company with three employees.

### 👨‍💻 Developer

- Launch EC2 instances
- Manage S3 buckets
- Cannot delete IAM users

### 👨‍💼 Manager

- View billing
- View reports
- Cannot modify infrastructure

### 🔒 Security Team

- Manage IAM
- Configure MFA
- Create Roles
- Audit permissions

IAM allows each person to access only what they need.

---

# Benefits of IAM

- Improves security
- Prevents unauthorized access
- Supports least privilege
- Easy permission management
- Supports AWS Organizations
- Provides auditability

---

# Key Points

- IAM is a Global Service.
- IAM controls access to AWS resources.
- IAM uses JSON policies.
- Root account should not be used for daily work.
- Enable MFA for better security.
- Follow the Principle of Least Privilege.

---

# Interview Questions

### 1. What is AWS IAM?

### 2. Is IAM a Regional or Global Service?

### 3. What are IAM Users?

### 4. What are IAM Roles?

### 5. What are IAM Policies?

### 6. Why should we avoid using the Root Account?

### 7. What is the Principle of Least Privilege?

### 8. What is the difference between Authentication and Authorization?

---
