# 👤 AWS CLI Profiles

> **Chapter 3** | AWS Command Line Interface (AWS CLI)

---

## 📖 Table of Contents

- What are AWS CLI Profiles?
- Why Do We Need Profiles?
- Default Profile
- Named Profiles
- Create a Profile
- View Available Profiles
- Use a Specific Profile
- Delete a Profile
- Best Practices
- Key Takeaways
- Interview Questions

---

# What are AWS CLI Profiles?

An **AWS CLI Profile** is a named set of AWS credentials and configuration settings.

Profiles allow you to manage multiple AWS accounts or IAM Users on the same computer without repeatedly reconfiguring the AWS CLI.

---

# Why Do We Need Profiles?

Imagine you're working with multiple AWS accounts.

For example:

- Personal AWS Account
- Company AWS Account
- Testing AWS Account

Instead of changing credentials every time, you can create separate profiles.

---

# Default Profile

When you run:

```bash
aws configure
```

AWS creates the **default** profile.

Example:

```ini
[default]
aws_access_key_id = AKIAxxxxxxxxxxxx
aws_secret_access_key = xxxxxxxxxxxxx
region = ap-south-1
output = json
```

If no profile is specified, AWS CLI automatically uses the **default** profile.

---

# Named Profiles

A **Named Profile** is any profile other than `default`.

Examples:

```
developer

production

testing

admin
```

Each profile can have:

- Different credentials
- Different regions
- Different output formats

---

# Create a Named Profile

Use the following command:

```bash
aws configure --profile developer
```

AWS CLI will ask for:

```
AWS Access Key ID

AWS Secret Access Key

Default Region

Default Output Format
```

Example:

```text
AWS Access Key ID [None]:
AWS Secret Access Key [None]:
Default region name [None]:
Default output format [None]:
```

---

# Configuration File Example

The credentials file:

```ini
[default]
aws_access_key_id = xxxxxxxxx
aws_secret_access_key = xxxxxxxxx

[developer]
aws_access_key_id = xxxxxxxxx
aws_secret_access_key = xxxxxxxxx
```

The config file:

```ini
[default]
region = ap-south-1
output = json

[profile developer]
region = us-east-1
output = table
```

---

# View Available Profiles

List all configured profiles:

```bash
aws configure list-profiles
```

Example Output:

```text
default
developer
testing
production
```

---

# Use a Specific Profile

To use a named profile, include the `--profile` option.

Example:

```bash
aws s3 ls --profile developer
```

This command uses the **developer** profile instead of the default profile.

---

# Check Configuration for a Profile

View the configuration of a specific profile:

```bash
aws configure list --profile developer
```

---

# Delete a Profile

AWS CLI does not have a dedicated delete command.

To remove a profile:

- Open the credentials file.
- Open the config file.
- Delete the profile entries manually.

---

# Real-World Example

Suppose you work for a company and also have a personal AWS account.

You can create two profiles:

```
default
│
└── Personal AWS Account

developer
│
└── Company AWS Account
```

When working on company resources:

```bash
aws ec2 describe-instances --profile developer
```

When working on personal resources:

```bash
aws s3 ls
```

The second command automatically uses the **default** profile.

---

# Best Practices

- Use meaningful profile names.
- Never share Access Keys.
- Avoid using the Root User.
- Use IAM Users or IAM Roles.
- Remove unused profiles.
- Rotate credentials regularly.

---

# Key Takeaways

- Profiles store AWS credentials and configuration.
- The **default** profile is created by `aws configure`.
- Named profiles help manage multiple AWS accounts.
- Use `--profile` to select a profile for a command.
- Profiles improve organization and security.

---

# Quick Summary

| Command | Purpose |
|----------|---------|
| `aws configure` | Configure the default profile |
| `aws configure --profile developer` | Create a named profile |
| `aws configure list-profiles` | List all profiles |
| `aws configure list --profile developer` | View profile configuration |
| `aws s3 ls --profile developer` | Use a specific profile |

---

# Interview Questions

### 1. What is an AWS CLI Profile?

### 2. What is the default profile?

### 3. Why do we use named profiles?

### 4. Which command creates a named profile?

### 5. How do you list all configured profiles?

### 6. How do you use a specific profile?

### 7. Can different profiles use different AWS Regions?

### 8. Where are profile configurations stored?

### 9. How do you remove a profile?

### 10. What are the advantages of AWS CLI Profiles?

---

