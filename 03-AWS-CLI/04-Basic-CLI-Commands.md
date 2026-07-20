# ⌨️ Basic AWS CLI Commands

> **Chapter 4** | AWS Command Line Interface (AWS CLI)

---

## 📖 Table of Contents

- Why Learn CLI Commands?
- Check AWS CLI Version
- Display Help
- Configure AWS CLI
- View Configuration
- List Profiles
- Check Current Identity
- Auto-Completion
- Command Structure
- Best Practices
- Key Takeaways
- Interview Questions

---

# Why Learn CLI Commands?

AWS CLI provides commands to interact with AWS services directly from your terminal.

Learning these basic commands helps you:

- Verify your AWS CLI installation
- Configure AWS credentials
- Troubleshoot issues
- Work efficiently with AWS

---

# Check AWS CLI Version

Display the installed AWS CLI version.

```bash
aws --version
```

Example Output:

```text
aws-cli/2.31.0 Python/3.13 Windows/10 exe/AMD64
```

---

# Display Help

View all available AWS CLI commands.

```bash
aws help
```

View help for a specific AWS service.

```bash
aws s3 help
```

View help for a specific command.

```bash
aws configure help
```

---

# Configure AWS CLI

Configure AWS CLI with your AWS account credentials.

```bash
aws configure
```

AWS CLI prompts for:

- AWS Access Key ID
- AWS Secret Access Key
- Default Region
- Output Format

---

# View Current Configuration

Display all configured values.

```bash
aws configure list
```

Example Output:

```text
      Name                    Value
      ----                    -----
   profile                default
access_key     ****************ABCD
secret_key     ****************WXYZ
    region              ap-south-1
```

---

# View Configured Region

Display the default AWS Region.

```bash
aws configure get region
```

Example Output:

```text
ap-south-1
```

---

# View Configured Output Format

```bash
aws configure get output
```

Example Output:

```text
json
```

---

# List All Profiles

Display all configured AWS CLI profiles.

```bash
aws configure list-profiles
```

Example Output:

```text
default
developer
testing
```

---

# Check Current AWS Identity

Verify which AWS account and IAM identity the CLI is using.

```bash
aws sts get-caller-identity
```

Example Output:

```json
{
  "UserId": "AIDAXXXXXXXXXXXXX",
  "Account": "123456789012",
  "Arn": "arn:aws:iam::123456789012:user/developer-user"
}
```

This command is commonly used to verify that the CLI is configured correctly.

---

# Auto-Completion

AWS CLI supports command auto-completion.

Examples:

```bash
aws ec2
```

Press:

```
TAB
```

AWS CLI displays available EC2 commands (supported shells only).

---

# AWS CLI Command Structure

Most AWS CLI commands follow this structure:

```text
aws <service> <operation> [options]
```

Examples:

```bash
aws s3 ls
```

```bash
aws ec2 describe-instances
```

```bash
aws iam list-users
```

Although these examples reference AWS services, you'll learn their specific commands in later modules.

---

# Commonly Used Basic Commands

| Command | Purpose |
|---------|---------|
| `aws --version` | Display AWS CLI version |
| `aws help` | Display AWS CLI help |
| `aws configure` | Configure AWS CLI |
| `aws configure list` | View current configuration |
| `aws configure get region` | Display default region |
| `aws configure list-profiles` | Display configured profiles |
| `aws sts get-caller-identity` | Verify authenticated identity |

---

# Best Practices

- Verify AWS CLI installation before configuring it.
- Use IAM Users or IAM Roles instead of the Root User.
- Keep AWS CLI updated.
- Never expose Access Keys.
- Verify your active profile before running commands.

---

# Key Takeaways

- AWS CLI commands follow a simple structure.
- Use `aws --version` to verify installation.
- Use `aws configure` to configure credentials.
- Use `aws help` to explore available commands.
- Use `aws sts get-caller-identity` to verify your AWS identity.

---

# Quick Summary

| Command | Description |
|----------|-------------|
| `aws --version` | Check CLI version |
| `aws help` | Display help |
| `aws configure` | Configure AWS CLI |
| `aws configure list` | View configuration |
| `aws configure list-profiles` | List profiles |
| `aws sts get-caller-identity` | Show authenticated IAM identity |

---

# Interview Questions

### 1. Which command checks the AWS CLI version?

### 2. Which command configures AWS CLI?

### 3. How do you display AWS CLI help?

### 4. Which command lists all configured profiles?

### 5. How do you view the configured AWS Region?

### 6. Which command verifies your AWS identity?

### 7. What is the general structure of an AWS CLI command?

### 8. Why should you verify your active profile before running commands?

### 9. What is the purpose of `aws configure list`?

### 10. Which command displays help for a specific AWS service?

---
