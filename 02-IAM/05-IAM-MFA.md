# 🔐 Multi-Factor Authentication (MFA)

> **Chapter 5** | AWS Identity and Access Management (IAM)

---

## 📖 Table of Contents

- What is MFA?
- Why Do We Need MFA?
- How MFA Works
- Types of MFA in AWS
- MFA Workflow
- Benefits of MFA
- Best Practices
- Key Takeaways
- Interview Questions

---

# What is Multi-Factor Authentication (MFA)?

**Multi-Factor Authentication (MFA)** is a security feature that requires users to provide **two or more forms of verification** before accessing an AWS account.

Instead of relying only on a password, MFA adds another layer of protection.

---

# Authentication Factors

Authentication generally uses one or more of these factors:

### 1️⃣ Something You Know

- Password
- PIN

### 2️⃣ Something You Have

- Mobile Phone
- Hardware Security Key
- Authenticator App

### 3️⃣ Something You Are

- Fingerprint
- Face Recognition
- Iris Scan

AWS MFA typically uses:

- Password
- MFA Code

---

# Why Do We Need MFA?

Passwords can be:

- Stolen
- Guessed
- Shared
- Leaked

Even if someone knows your password, they still cannot sign in without the MFA code.

This greatly reduces the risk of unauthorized access.

---

# How MFA Works

```
User Login
      │
      ▼
Enter Username & Password
      │
      ▼
Enter MFA Code
      │
      ▼
AWS Verifies Both
      │
      ▼
Access Granted
```

---

# Types of MFA Supported by AWS

AWS supports multiple MFA devices.

| MFA Type | Description |
|----------|-------------|
| Virtual MFA | Authenticator apps like Google Authenticator or Microsoft Authenticator |
| Hardware MFA | Physical security devices |
| FIDO Security Keys | USB or NFC security keys (e.g., YubiKey) |

---

# Virtual MFA Applications

Popular authenticator apps include:

- Google Authenticator
- Microsoft Authenticator
- Authy

These apps generate a new **6-digit code** every 30 seconds.

---

# Real-World Example

Imagine your AWS password is:

```
Password123
```

A hacker somehow learns your password.

Without MFA:

```
Password
     │
     ▼
Access Granted ❌
```

With MFA:

```
Password
     │
     ▼
Enter MFA Code
     │
     ▼
Hacker Cannot Continue ❌
```

Even with the correct password, access is denied because the hacker doesn't have your MFA device.

---

# Benefits of MFA

- Protects against stolen passwords
- Adds an extra layer of security
- Prevents unauthorized access
- Helps secure sensitive AWS resources
- Recommended for all AWS accounts

---

# AWS Best Practices

> [!IMPORTANT]
> Enable MFA for the **AWS Root User** immediately after creating your AWS account.

Additional recommendations:

- Enable MFA for all IAM Users.
- Never share MFA devices.
- Use Virtual MFA for personal accounts.
- Use Hardware/FIDO keys for enterprise environments.
- Store backup codes or recovery methods securely.

---

# Key Takeaways

- MFA provides an additional layer of authentication.
- AWS supports Virtual, Hardware, and FIDO MFA devices.
- Password alone is not enough for strong security.
- Always enable MFA for the Root User and IAM Users.

---

# Quick Summary

| Term | Meaning |
|------|---------|
| MFA | Multi-Factor Authentication |
| Purpose | Adds an extra layer of security |
| Root User | MFA should always be enabled |
| Common Device | Authenticator App |

---

# Interview Questions

### 1. What is Multi-Factor Authentication (MFA)?

### 2. Why is MFA important?

### 3. What are the authentication factors?

### 4. Which MFA devices does AWS support?

### 5. Can the AWS Root User use MFA?

### 6. Which is more secure: Password only or Password + MFA?

### 7. Name three Virtual MFA applications.

### 8. How often does a Virtual MFA code change?

### 9. Is MFA mandatory for IAM Users?

### 10. Why should every AWS account enable MFA?

---
