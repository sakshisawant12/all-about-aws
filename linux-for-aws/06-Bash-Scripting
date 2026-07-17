# 📜 Bash Scripting

> Learn the basics of Bash scripting to automate repetitive tasks in Linux. Bash scripting is an essential skill for Linux Administrators, AWS Cloud Engineers, and DevOps professionals.

---

## 📚 Table of Contents

- [What is Bash?](#-what-is-bash)
- [What is a Bash Script?](#-what-is-a-bash-script)
- [Creating Your First Script](#-creating-your-first-script)
- [The Shebang (`#!/bin/bash`)](#-the-shebang-binbash)
- [The `echo` Command](#-the-echo-command)
- [Running a Bash Script](#-running-a-bash-script)
- [Making a Script Executable](#-making-a-script-executable)
- [Your First Bash Script](#-your-first-bash-script)
- [Linux in AWS](#-linux-in-aws)
- [Key Takeaways](#-key-takeaways)
- [Interview Questions](#-interview-questions)

---

# 📖 What is Bash?

**Bash (Bourne Again SHell)** is the default command-line shell in most Linux distributions.

It acts as a bridge between the user and the Linux operating system.

With Bash, you can:

- Run Linux commands
- Manage files and directories
- Install software
- Execute programs
- Automate repetitive tasks

---

# 📜 What is a Bash Script?

A **Bash Script** is a text file containing a sequence of Linux commands that are executed one after another.

Instead of typing the same commands repeatedly, you can save them in a script and run them with a single command.

Benefits of Bash scripting:

- ✅ Automates repetitive tasks
- ✅ Saves time
- ✅ Reduces manual errors
- ✅ Simplifies system administration

---

# 📝 Creating Your First Script

Create a new script using Nano.

```bash
nano hello.sh
```

Enter the following content:

```bash
#!/bin/bash

echo "Hello, Linux!"
```

Save the file:

```text
Ctrl + O
```

Press:

```text
Enter
```

Exit Nano:

```text
Ctrl + X
```

---

# 🏁 The Shebang (`#!/bin/bash`)

The first line of a Bash script is called the **Shebang**.

```bash
#!/bin/bash
```

It tells Linux to execute the script using the **Bash interpreter**.

Without the shebang, Linux may not know which interpreter should run the script.

---

# 📢 The `echo` Command

The `echo` command prints text to the terminal.

Example:

```bash
echo "Welcome to Linux"
```

Output

```text
Welcome to Linux
```

You can use multiple `echo` statements in a script to display messages.

---

# ▶️ Running a Bash Script

There are two common ways to run a Bash script.

### Method 1

Run the script using Bash:

```bash
bash hello.sh
```

---

### Method 2

Run the script directly after making it executable:

```bash
./hello.sh
```

---

# 🔐 Making a Script Executable

Before running a script directly, you must give it execute permission.

```bash
chmod +x hello.sh
```

Check the permissions:

```bash
ls -l hello.sh
```

Example Output

```text
-rwxr-xr-x hello.sh
```

Now run the script:

```bash
./hello.sh
```

---

# 🚀 Your First Bash Script

Create a script named `system_info.sh`.

```bash
nano system_info.sh
```

Add the following code:

```bash
#!/bin/bash

echo "=================================="
echo "   Linux System Information"
echo "=================================="

echo ""

echo "Current User:"
whoami

echo ""

echo "Hostname:"
hostname

echo ""

echo "Current Directory:"
pwd

echo ""

echo "Current Date and Time:"
date
```

Save the file and make it executable.

```bash
chmod +x system_info.sh
```

Run the script.

```bash
./system_info.sh
```

Example Output

```text
==================================
   Linux System Information
==================================

Current User:
janvi

Hostname:
localhost

Current Directory:
/home/janvi

Current Date and Time:
Fri Jul 17 11:45:22 IST 2026
```

---

# ☁️ Linux in AWS

Bash scripts are widely used to automate tasks on AWS EC2 instances.

Common use cases include:

- Installing packages
- Creating users
- Backing up files
- Monitoring servers
- Updating the operating system
- Deploying applications

Example:

```bash
#!/bin/bash

sudo dnf update -y

echo "System Updated Successfully!"
```

Instead of manually typing commands every time, Cloud Engineers automate them using Bash scripts.

---

# 📝 Key Takeaways

- Bash is the default Linux shell.
- Bash scripts automate repetitive tasks.
- Every Bash script should start with `#!/bin/bash`.
- The `echo` command prints messages to the terminal.
- Use `chmod +x` to make a script executable.
- Run scripts using `bash filename.sh` or `./filename.sh`.
- Bash scripting is an essential skill for AWS Cloud Engineers.

---

# 🎯 Interview Questions

### 1. What is Bash?

Bash is a command-line shell used to interact with the Linux operating system.

---

### 2. What is a Bash script?

A Bash script is a file containing a sequence of Linux commands that are executed automatically.

---

### 3. What is the purpose of `#!/bin/bash`?

It tells Linux to execute the script using the Bash interpreter.

---

### 4. Which command makes a script executable?

```bash
chmod +x filename.sh
```

---

### 5. What is the difference between these two commands?

```bash
bash hello.sh
```

and

```bash
./hello.sh
```

- `bash hello.sh` runs the script using the Bash interpreter directly.
- `./hello.sh` executes the script as a program, so it must have execute permission (`chmod +x`) and usually includes a shebang (`#!/bin/bash`).

---

