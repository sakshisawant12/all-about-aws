# 📜 IAM Policies

> **Chapter 3** | AWS Identity and Access Management (IAM)

---

## 📖 Table of Contents

- What is an IAM Policy?
- Why Do We Need IAM Policies?
- Policy Structure
- JSON Policy Example
- Policy Types
- AWS Managed Policies
- Customer Managed Policies
- Inline Policies
- Allow vs Deny
- Policy Evaluation Logic
- Best Practices
- Key Takeaways
- Interview Questions

---

# What is an IAM Policy?

An **IAM Policy** is a JSON document that defines **what actions are allowed or denied** on AWS resources.

Policies are attached to:

- IAM Users
- IAM Groups
- IAM Roles

A policy answers questions like:

- Who can access a resource?
- Which actions are allowed?
- On which resources?
- Under what conditions?

---

# Why Do We Need IAM Policies?

Without IAM Policies:

- Users would have unrestricted access.
- Resources could be accidentally modified or deleted.
- Security risks would increase.

With IAM Policies:

- Access is controlled.
- Users get only the permissions they need.
- Security improves.

---

# IAM Policy Structure

Every IAM Policy is written in **JSON (JavaScript Object Notation)**.

A policy usually contains:

- Version
- Statement
- Effect
- Action
- Resource

---

# Policy Components

| Component | Description |
|-----------|-------------|
| Version | Policy language version |
| Statement | List of permission statements |
| Effect | Allow or Deny |
| Action | AWS API operations |
| Resource | AWS resources affected |
| Condition | Optional rules for access |

---

# JSON Policy Example

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "arn:aws:s3:::my-bucket"
    }
  ]
}
```

### Explanation

- **Version** → Policy language version.
- **Effect** → Allows the action.
- **Action** → User can list the S3 bucket.
- **Resource** → Only the specified bucket.

---

# Types of IAM Policies

AWS provides three main types of IAM Policies.

## 1. AWS Managed Policies

Created and maintained by AWS.

Examples:

- AmazonS3ReadOnlyAccess
- AmazonEC2FullAccess
- AdministratorAccess

### Advantages

- Easy to use
- Automatically updated by AWS
- Recommended for beginners

---

## 2. Customer Managed Policies

Created and managed by you.

These policies allow you to customize permissions according to your organization's requirements.

### Advantages

- Reusable
- Fully customizable
- Easy to manage

---

## 3. Inline Policies

An Inline Policy is directly attached to a single User, Group, or Role.

It cannot be shared with other identities.

### Use Case

Useful when a permission should belong only to one specific identity.

---

# AWS Managed vs Customer Managed vs Inline

| Feature | AWS Managed | Customer Managed | Inline |
|----------|-------------|------------------|---------|
| Created By | AWS | Customer | Customer |
| Reusable | ✅ | ✅ | ❌ |
| Editable | ❌ | ✅ | ✅ |
| Shared | ✅ | ✅ | ❌ |
| Best For | Common Permissions | Custom Permissions | One-Time Permissions |

---

# Allow vs Deny

IAM supports two permission effects.

## Allow

Grants permission.

Example:

```
Allow EC2 Start
```

---

## Deny

Explicitly blocks permission.

Example:

```
Deny S3 Delete
```

---

# Policy Evaluation Logic

AWS evaluates permissions in the following order:

```
User Request
      │
      ▼
Is there an Explicit Deny?
      │
  Yes ─────► Access Denied
      │
      ▼
Is there an Allow?
      │
  Yes ─────► Access Granted
      │
      ▼
No Allow Found
      │
      ▼
Implicit Deny
```

---

# Important Rule

> [!IMPORTANT]
> **Explicit Deny always overrides Allow.**

Even if multiple policies allow an action, a single Explicit Deny will block access.

---

# Real-World Example

Imagine a Developer has:

- AmazonEC2FullAccess
- AmazonS3FullAccess

But another policy says:

```
Deny DeleteObject on S3
```

Result:

- Can create buckets ✅
- Can upload files ✅
- Cannot delete files ❌

Because **Explicit Deny wins**.

---

# Best Practices

- Follow the Principle of Least Privilege.
- Prefer Customer Managed Policies for custom permissions.
- Avoid giving AdministratorAccess unless necessary.
- Review policies regularly.
- Use descriptive names for policies.

---

# Key Takeaways

- IAM Policies define permissions.
- Policies are written in JSON.
- Policies can Allow or Deny actions.
- AWS supports Managed, Customer Managed, and Inline Policies.
- Explicit Deny always overrides Allow.

---

# Quick Summary

| Policy Type | Best Use |
|-------------|----------|
| AWS Managed | Standard permissions |
| Customer Managed | Organization-specific permissions |
| Inline | Single user or role permissions |

---

# Interview Questions

### 1. What is an IAM Policy?

### 2. In which format are IAM Policies written?

### 3. What is the difference between AWS Managed and Customer Managed Policies?

### 4. What is an Inline Policy?

### 5. What is Explicit Deny?

### 6. Which takes priority: Allow or Deny?

### 7. Can one IAM Policy be attached to multiple users?

### 8. What are the main components of an IAM Policy?

### 9. What is the Principle of Least Privilege?

### 10. Explain IAM Policy evaluation logic.

---
