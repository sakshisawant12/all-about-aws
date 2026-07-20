# 🧪 IAM Hands-On Lab

> **Chapter 9** | AWS Identity and Access Management (IAM)

---

# 🎯 Lab Objective

In this lab, you will learn how to:

- Create an IAM User
- Create an IAM Group
- Attach IAM Policies
- Enable MFA
- Create an IAM Role
- Test User Permissions

---

# 🛠 Lab Prerequisites

Before starting, make sure you have:

- AWS Account
- Root User Access
- MFA Enabled for Root User
- Internet Connection

---

# Lab 1 – Create an IAM User

## Step 1

Sign in to the AWS Management Console.

---

## Step 2

Navigate to:

```
AWS Console
    │
    ▼
IAM
```

---

## Step 3

Click

```
Users
```

---

## Step 4

Click

```
Create User
```

---

## Step 5

Enter:

```
Username

developer-user
```

---

## Step 6

Choose the access type.

✔ AWS Management Console Access

(Optional)

✔ Programmatic Access (CLI/SDK)

---

## Step 7

Click

```
Next
```

---

# Lab 2 – Create an IAM Group

Navigate to

```
IAM
    │
    ▼
User Groups
```

Click

```
Create Group
```

Group Name

```
Developers
```

Attach Policy

```
AmazonEC2ReadOnlyAccess
```

Click

```
Create Group
```

---

# Lab 3 – Add User to Group

Open

```
Users

developer-user
```

Choose

```
Add User to Group
```

Select

```
Developers
```

Save Changes.

---

# Lab 4 – Create a Custom Policy

Navigate to

```
IAM

Policies
```

Click

```
Create Policy
```

Choose

```
JSON
```

Paste the following policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:ListBucket"
      ],
      "Resource": "*"
    }
  ]
}
```

Review

Create Policy

---

# Lab 5 – Attach Policy to User

Go to

```
Users

developer-user
```

Choose

```
Add Permissions
```

Attach the custom policy.

Save Changes.

---

# Lab 6 – Enable MFA

Navigate to

```
Users

developer-user

Security Credentials
```

Click

```
Assign MFA Device
```

Choose

```
Authenticator App
```

Scan the QR Code using:

- Google Authenticator
- Microsoft Authenticator
- Authy

Enter the generated codes.

Finish Setup.

---

# Lab 7 – Create an IAM Role

Navigate to

```
IAM

Roles
```

Click

```
Create Role
```

Trusted Entity

```
AWS Service
```

Use Case

```
EC2
```

Attach Policy

```
AmazonS3ReadOnlyAccess
```

Role Name

```
EC2-S3-ReadOnly-Role
```

Create Role.

---

# Lab 8 – Test Permissions

Sign in as

```
developer-user
```

Try to:

✅ View EC2

✅ View S3

❌ Delete IAM Users

❌ Delete IAM Policies

Observe which actions are allowed and denied.

---

# Lab 9 – Delete Resources

To avoid unnecessary IAM objects, delete:

- Test User
- Test Group
- Custom Policy
- Test Role (if no longer needed)

---

# Expected Outcome

After completing this lab, you should be able to:

- Create IAM Users
- Create IAM Groups
- Attach Policies
- Enable MFA
- Create IAM Roles
- Understand Role-Based Access Control (RBAC)
- Apply the Principle of Least Privilege

---

# Troubleshooting

### Access Denied

- Check attached policies.
- Verify group membership.
- Review permission boundaries (if configured).

---

### Cannot Sign In

- Verify username.
- Reset password if necessary.
- Check MFA configuration.

---

### Policy Not Working

- Ensure the policy is attached.
- Confirm the correct resource ARN is used.
- Review IAM Policy Simulator if needed.

---

# Best Practices

- Never use the Root User for daily work.
- Enable MFA for all users.
- Use Groups for permission management.
- Prefer IAM Roles over long-term Access Keys.
- Follow the Principle of Least Privilege.

---

# Lab Summary

| Task | Status |
|------|--------|
| Create IAM User | ✅ |
| Create IAM Group | ✅ |
| Attach Policy | ✅ |
| Create Custom Policy | ✅ |
| Enable MFA | ✅ |
| Create IAM Role | ✅ |
| Test Permissions | ✅ |

---

