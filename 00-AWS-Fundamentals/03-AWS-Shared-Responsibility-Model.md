# 🛡️ AWS Shared Responsibility Model

> Learn how security responsibilities are divided between AWS and the customer. Understanding the Shared Responsibility Model is essential for designing secure cloud environments and is one of the most frequently asked AWS interview topics.

---

# 📚 Table of Contents

- What is the Shared Responsibility Model?
- Why is it Important?
- AWS Responsibilities
- Customer Responsibilities
- Security of the Cloud vs Security in the Cloud
- Real-World Example
- Key Takeaways
- Interview Questions

---

# 📖 What is the Shared Responsibility Model?

The **AWS Shared Responsibility Model** defines which security responsibilities belong to **AWS** and which belong to the **customer**.

AWS manages the **security of the cloud**, while customers are responsible for **security in the cloud**.

This model ensures that both AWS and the customer work together to maintain a secure cloud environment.

---

# ❓ Why is it Important?

The Shared Responsibility Model helps to:

- 🔒 Protect cloud infrastructure
- 🛡️ Secure customer data
- ⚙️ Clearly define responsibilities
- 📋 Meet compliance requirements
- 🚨 Reduce security risks

Understanding this model helps prevent common security mistakes.

---

# ☁️ AWS Responsibilities (Security **of** the Cloud)

AWS is responsible for protecting the cloud infrastructure.

This includes:

- 🏢 Physical Data Centers
- 💻 Servers
- 🌐 Networking Equipment
- 🔌 Storage Devices
- ⚡ Power Supply
- ❄️ Cooling Systems
- 🌍 Global Infrastructure
- 🔧 Hardware Maintenance
- 🛠️ Hypervisor Management

Customers do **not** have access to these components.

---

# 👨‍💻 Customer Responsibilities (Security **in** the Cloud)

Customers are responsible for everything they deploy inside AWS.

This includes:

- 👤 IAM Users and Permissions
- 🔑 Password Policies
- 📂 Data Security
- 🔐 Encryption
- 💻 EC2 Operating System Updates
- 🛡️ Security Groups
- 🌐 Network Configuration
- 📦 Installed Applications
- 🔄 Data Backups

If a customer misconfigures resources, AWS is **not responsible** for the issue.

---

# 🔄 Security of the Cloud vs Security in the Cloud

| Security **of** the Cloud (AWS) | Security **in** the Cloud (Customer) |
|---------------------------------|--------------------------------------|
| Data Centers | IAM Users |
| Physical Servers | Passwords |
| Networking Hardware | EC2 Configuration |
| Storage Hardware | Security Groups |
| Global Infrastructure | Customer Data |
| Hypervisor | Installed Applications |
| Cooling & Power | Operating System Updates |

---

# 🌟 Real-World Example

Imagine you rent an apartment.

### 🏢 Apartment Owner (AWS)

The owner is responsible for:

- Building security
- Electricity
- Water supply
- Elevators
- Main entrance

---

### 👨 Tenant (Customer)

The tenant is responsible for:

- Locking the door
- Protecting valuables
- Keeping the apartment clean
- Installing personal security devices

AWS works in the same way.

AWS secures the infrastructure, while customers secure their applications and data.

---

# ☁️ AWS Example

Suppose you launch an **Amazon EC2 instance**.

### AWS is responsible for:

- Physical server
- Networking hardware
- Storage devices
- Data center security
- Hypervisor

### You are responsible for:

- Installing software
- Updating the operating system
- Configuring firewall rules (Security Groups)
- Managing IAM users
- Encrypting your data

---

# 📝 Key Takeaways

- AWS follows a **Shared Responsibility Model**.
- AWS secures the cloud infrastructure.
- Customers secure their applications and data.
- AWS is responsible for **Security of the Cloud**.
- Customers are responsible for **Security in the Cloud**.
- Understanding this model is essential for AWS certification and interviews.

---

# 🎯 Interview Questions

### 1. What is the AWS Shared Responsibility Model?

It is a security model that defines the responsibilities shared between AWS and the customer.

---

### 2. What is AWS responsible for?

AWS is responsible for securing the cloud infrastructure, including data centers, hardware, networking, and the hypervisor.

---

### 3. What is the customer responsible for?

Customers are responsible for IAM, operating system updates, applications, security groups, encryption, and their data.

---

### 4. What is the difference between "Security of the Cloud" and "Security in the Cloud"?

- **Security of the Cloud** → Managed by AWS.
- **Security in the Cloud** → Managed by the customer.

---

### 5. Is AWS responsible for updating your EC2 operating system?

❌ No.

The customer is responsible for updating and maintaining the operating system running on their EC2 instances.

---
