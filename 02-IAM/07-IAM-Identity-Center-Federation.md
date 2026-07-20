# 🏢 AWS IAM Identity Center & Identity Federation

> **Chapter 7** | AWS Identity and Access Management (IAM)

---

## 📖 Table of Contents

- What is AWS IAM Identity Center?
- What is Identity Federation?
- Why Do We Need Identity Federation?
- How Identity Federation Works
- Identity Providers (IdPs)
- Benefits of IAM Identity Center
- IAM Users vs Identity Center
- Real-World Example
- Best Practices
- Key Takeaways
- Interview Questions

---

# What is AWS IAM Identity Center?

**AWS IAM Identity Center** (formerly **AWS Single Sign-On**) is a service that helps organizations manage **centralized access** to multiple AWS accounts and business applications.

Instead of creating separate IAM Users for every employee, organizations can allow employees to sign in using their existing company credentials.

---

# What is Identity Federation?

**Identity Federation** is the process of allowing users from an external identity provider (IdP) to access AWS resources without creating IAM Users.

AWS trusts the external identity provider to authenticate users.

After successful authentication, AWS grants temporary permissions using IAM Roles.

---

# Why Do We Need Identity Federation?

Imagine a company with:

- 5,000 employees
- 50 AWS accounts

Creating IAM Users for every employee would be difficult to manage.

Instead:

- Employees log in using company credentials.
- AWS verifies their identity through the external identity provider.
- AWS grants temporary access based on IAM Roles.

---

# How Identity Federation Works

```
Employee
    │
    ▼
Company Login Portal
    │
    ▼
Identity Provider (IdP)
    │
    ▼
AWS IAM Identity Center
    │
    ▼
IAM Role
    │
    ▼
AWS Resources
```

---

# Common Identity Providers (IdPs)

AWS supports integration with many external identity providers.

Examples include:

- Microsoft Entra ID (formerly Azure Active Directory)
- Okta
- Google Workspace
- Ping Identity
- OneLogin

---

# Benefits of IAM Identity Center

- Centralized user management
- Single Sign-On (SSO)
- Temporary credentials
- Better security
- Easier user onboarding and offboarding
- Access to multiple AWS accounts with one login

---

# IAM Users vs IAM Identity Center

| Feature | IAM Users | IAM Identity Center |
|----------|-----------|---------------------|
| Best For | Small AWS Accounts | Medium & Large Organizations |
| User Management | Individual IAM Users | Centralized Identity Provider |
| Single Sign-On (SSO) | ❌ No | ✅ Yes |
| Multiple AWS Accounts | Limited | ✅ Yes |
| Temporary Credentials | ❌ No | ✅ Yes |

---

# Real-World Example

A company uses **Microsoft Entra ID** to manage employee accounts.

When an employee wants to access AWS:

1. They sign in using their company email and password.
2. Microsoft Entra ID authenticates the user.
3. AWS IAM Identity Center verifies the authentication.
4. AWS assigns the appropriate IAM Role.
5. The employee gains temporary access to AWS resources.

No IAM User is created in AWS for that employee.

---

# Advantages

- Reduces IAM User management
- Improves security
- Supports centralized authentication
- Simplifies access to multiple AWS accounts
- Uses temporary credentials instead of long-term access keys

---

# Best Practices

- Use IAM Identity Center for organizations with multiple AWS accounts.
- Integrate with an existing corporate identity provider.
- Assign permissions using IAM Roles.
- Follow the Principle of Least Privilege.
- Review user access regularly.

---

# Key Takeaways

- IAM Identity Center provides centralized access management.
- Identity Federation allows external users to access AWS.
- AWS uses IAM Roles and temporary credentials for federated users.
- Single Sign-On (SSO) improves user experience and security.

---

# Quick Summary

| Term | Meaning |
|------|---------|
| IAM Identity Center | Centralized access management for AWS accounts and applications |
| Identity Federation | Access AWS using an external identity provider |
| Identity Provider (IdP) | Service that authenticates users |
| SSO | One login for multiple AWS accounts and applications |

---

# Interview Questions

### 1. What is AWS IAM Identity Center?

### 2. What was AWS IAM Identity Center previously called?

### 3. What is Identity Federation?

### 4. What is an Identity Provider (IdP)?

### 5. Name some commonly used Identity Providers.

### 6. Why do enterprises prefer IAM Identity Center over IAM Users?

### 7. Does Identity Federation create IAM Users?

### 8. How are permissions granted to federated users?

### 9. What is Single Sign-On (SSO)?

### 10. Explain Identity Federation with a real-world example.

---
