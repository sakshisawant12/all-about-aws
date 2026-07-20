# 💼 IAM Interview Questions

> **Chapter 10** | AWS Identity and Access Management (IAM)

---

# 📖 Table of Contents

- Basic Questions
- Intermediate Questions
- Scenario-Based Questions
- Rapid Fire Questions

---

# Basic Interview Questions

## 1. What is AWS IAM?

**Answer:**

AWS Identity and Access Management (IAM) is a global AWS service used to securely manage access to AWS resources by controlling who can access them and what actions they can perform.

---

## 2. Is IAM a Global or Regional Service?

**Answer:**

IAM is a **Global Service**.

Users, Groups, Roles, and Policies are available across all AWS Regions.

---

## 3. What are the main components of IAM?

**Answer:**

- IAM Users
- IAM Groups
- IAM Roles
- IAM Policies
- MFA

---

## 4. What is an IAM User?

**Answer:**

An IAM User represents an individual person or application that requires access to AWS resources.

---

## 5. What is an IAM Group?

**Answer:**

An IAM Group is a collection of IAM Users that share the same permissions.

---

## 6. What is an IAM Role?

**Answer:**

An IAM Role is an AWS identity that provides temporary permissions to trusted users or AWS services without using permanent credentials.

---

## 7. What is an IAM Policy?

**Answer:**

An IAM Policy is a JSON document that defines permissions by specifying which actions are allowed or denied on AWS resources.

---

## 8. What is MFA?

**Answer:**

Multi-Factor Authentication (MFA) adds an additional layer of security by requiring a second form of authentication besides the password.

---

## 9. What is the Principle of Least Privilege?

**Answer:**

Users should receive only the permissions required to perform their tasks and nothing more.

---

## 10. Why shouldn't we use the Root User daily?

**Answer:**

The Root User has unrestricted access to all AWS resources.

It should only be used for account-level administrative tasks.

---

# Intermediate Interview Questions

## 11. What is the difference between an IAM User and an IAM Role?

| IAM User | IAM Role |
|----------|----------|
| Permanent identity | Temporary identity |
| Has password | No password |
| Has Access Keys | Temporary credentials |
| Used by people | Used by AWS services and applications |

---

## 12. What is AWS STS?

**Answer:**

AWS Security Token Service (STS) provides temporary security credentials for IAM Roles and federated users.

---

## 13. What are temporary credentials?

**Answer:**

Temporary credentials include:

- Access Key ID
- Secret Access Key
- Session Token

These credentials automatically expire after a specified duration.

---

## 14. What are AWS Managed Policies?

**Answer:**

Policies created and maintained by AWS.

Example:

- AmazonS3ReadOnlyAccess
- AmazonEC2FullAccess

---

## 15. What are Customer Managed Policies?

**Answer:**

Policies created and maintained by customers to meet specific business requirements.

---

## 16. What are Inline Policies?

**Answer:**

Policies directly attached to a single IAM User, Group, or Role and cannot be reused.

---

## 17. What is Explicit Deny?

**Answer:**

An Explicit Deny always overrides any Allow permission.

---

## 18. What is a Permission Boundary?

**Answer:**

A Permission Boundary defines the maximum permissions that an IAM User or Role can have.

---

## 19. What is Identity Federation?

**Answer:**

Identity Federation allows users from an external identity provider to access AWS resources without creating IAM Users.

---

## 20. What is AWS IAM Identity Center?

**Answer:**

AWS IAM Identity Center (formerly AWS Single Sign-On) provides centralized access management for multiple AWS accounts and applications.

---

# Scenario-Based Interview Questions

## 21. An EC2 instance needs access to an S3 bucket. What is the best approach?

**Answer:**

Attach an IAM Role with the required S3 permissions to the EC2 instance.

Avoid storing long-term Access Keys.

---

## 22. A developer accidentally received AdministratorAccess. What should you do?

**Answer:**

Remove unnecessary permissions and grant only the permissions required according to the Principle of Least Privilege.

---

## 23. An employee leaves the company. What IAM actions should you take?

**Answer:**

- Disable or delete the IAM User
- Remove Access Keys
- Revoke active sessions
- Remove group memberships
- Review assigned roles and policies

---

## 24. A user can view an S3 bucket but cannot delete objects. Why?

**Answer:**

Possible reasons:

- Missing `s3:DeleteObject` permission
- Explicit Deny in a policy
- Permission Boundary restriction

---

## 25. Why are IAM Roles preferred over Access Keys?

**Answer:**

IAM Roles provide temporary credentials that are automatically rotated and expire, making them more secure than long-term Access Keys.

---

# Rapid Fire Questions

| Question | Answer |
|----------|--------|
| IAM Service Type | Global |
| Policy Format | JSON |
| Authentication Service | IAM |
| Authorization Method | IAM Policies |
| Temporary Credentials | AWS STS |
| MFA Purpose | Extra Security |
| Least Privilege | Minimum Required Access |
| Root User | Full Account Access |
| IAM Role | Temporary Identity |
| Policy Effect | Allow or Deny |

---

# Top 10 Interview Tips

- Understand the difference between Users, Groups, and Roles.
- Remember that IAM is a Global Service.
- Know the structure of an IAM Policy.
- Explain why IAM Roles are preferred over Access Keys.
- Understand Explicit Deny.
- Know the Principle of Least Privilege.
- Always recommend enabling MFA.
- Be familiar with AWS STS.
- Know the purpose of IAM Identity Center.
- Support answers with real-world examples whenever possible.

---

# Final Revision Checklist

- [x] IAM Basics
- [x] IAM Users
- [x] IAM Groups
- [x] IAM Roles
- [x] IAM Policies
- [x] Permission Boundaries
- [x] MFA
- [x] AWS STS
- [x] IAM Identity Center
- [x] Best Practices
- [x] Hands-on Lab

---


