# 🐧 Bash Programming for Beginners

Welcome to the wonderful world of **Bash Programming**! 🎉

Bash (Bourne Again SHell) is a command-line interpreter used on Linux and macOS systems. It allows you to automate tasks, manage files, and control your system efficiently.

---

# What is Bash?

Bash is a shell program that:

- Executes commands
- Runs scripts
- Automates repetitive tasks
- Manages files and processes

![Linux Terminal](https://ubuntucommunity.s3.dualstack.us-east-2.amazonaws.com/original/2X/b/ba76cbf3dc8dc2cc94d26dd61c7aad3cedcd5102.png)

---

# Your First Bash Script

Create a file called `hello.sh`:

```bash
#!/bin/bash

echo "Hello, World!"
```

Make it executable:

```bash
chmod +x hello.sh
```

Run it:

```bash
./hello.sh
```

Output:

```text
Hello, World!
```

---

# Variables

Variables store values.

```bash
#!/bin/bash

name="Alice"

echo "Hello, $name"
```

Output:

```text
Hello, Alice
```

---

# User Input

```bash
#!/bin/bash

echo "What's your name?"
read name

echo "Nice to meet you, $name!"
```

---

# Funny GIF Break 😂

![Funny Programmer GIF](https://media.giphy.com/media/13HgwGsXF0aiGY/giphy.gif)

*When your script works on the first try.*

---

# Conditional Statements

```bash
#!/bin/bash

age=18

if [ $age -ge 18 ]; then
    echo "Adult"
else
    echo "Minor"
fi
```

---

# Comparison Operators

| Operator | Meaning |
|-----------|-----------|
| -eq | Equal |
| -ne | Not Equal |
| -gt | Greater Than |
| -lt | Less Than |
| -ge | Greater or Equal |
| -le | Less or Equal |

Example:

```bash
if [ 10 -gt 5 ]; then
    echo "10 is greater"
fi
```

---

# Loops

## For Loop

```bash
for i in 1 2 3 4 5
do
    echo $i
done
```

Output:

```text
1
2
3
4
5
```

---

## While Loop

```bash
count=1

while [ $count -le 5 ]
do
    echo $count
    count=$((count+1))
done
```

---

# Functions

```bash
greet() {
    echo "Hello $1"
}

greet "Alice"
```

Output:

```text
Hello Alice
```

---

# Command-Line Arguments

```bash
#!/bin/bash

echo "First argument: $1"
echo "Second argument: $2"
```

Run:

```bash
./script.sh apple banana
```

Output:

```text
First argument: apple
Second argument: banana
```

---

# File Operations

Create a file:

```bash
touch file.txt
```

Copy a file:

```bash
cp file.txt backup.txt
```

Move a file:

```bash
mv file.txt documents/
```

Delete a file:

```bash
rm file.txt
```

---

# Useful Commands

| Command | Purpose |
|----------|----------|
| ls | List files |
| pwd | Current directory |
| cd | Change directory |
| mkdir | Create directory |
| rm | Remove file |
| cp | Copy file |
| mv | Move file |
| cat | Display file content |

---


*Looking for a missing semicolon... in Bash.*

---

# Exit Status

Every command returns an exit code.

```bash
ls

echo $?
```

Output:

```text
0
```

A status of `0` means success.

---

# Comments

Single-line comment:

```bash
# This is a comment
```

Multi-line style:

```bash
: '
This is
a multi-line
comment
'
```

---

# Best Practices

✅ Use meaningful variable names

✅ Add comments

✅ Check command success

✅ Use quotes around variables

```bash
echo "$name"
```

✅ Keep scripts simple

---

# Mini Project: Backup Script

```bash
#!/bin/bash

SOURCE="/home/user/documents"
DEST="/home/user/backup"

cp -r "$SOURCE" "$DEST"

echo "Backup completed!"
```

---

# Learning Path

1. Bash Basics
2. Variables
3. Conditions
4. Loops
5. Functions
6. File Handling
7. Process Management
8. Automation Scripts
9. Cron Jobs
10. Shell Scripting Projects

---

# Final Wisdom 🧙

```bash
sudo make me a sandwich
```

Output:

```text
Okay.
```

(Only if you're root 😄)

---

Happy Scripting! 🚀🐧

# Table of Contents

- What is Bash?
- Variables
- User Input
- Conditions
- Loops
- Functions
- Arrays
- Case Statements
- File Operations
- Cron Jobs
- Best Practices

---

# Bash Script Safety

Use these options in production scripts:

```bash
#!/bin/bash
set -euo pipefail
```
- `-e` Exit on errors
- `-u` Treat undefined variables as errors
- `pipefail` Detect pipeline failures

---

# Arrays

```bash
fruits=("apple" "banana" "orange")

echo "${fruits[0]}"
echo "${fruits[@]}"
```

Output:

```text
apple
apple banana orange
```

---

# Case Statements

```bash
read choice
case $choice in
  start)
    echo "Starting service..."
    ;;
  stop)
    echo "Stopping service..."
    ;;
  *)
    echo "Invalid option"
    ;;
esac
```

---

# Cron Jobs
Schedule a script to run every day at midnight:

```bash
0 0 * * * /home/user/backup.sh
```

Edit cron jobs:

```bash
crontab -e
```

---
cp -r "$SOURCE" "$DEST"
if cp -r "$SOURCE" "$DEST"; then
     echo "Backup completed successfully!"
 else
     echo "Backup failed!"
     exit 1
 fi

---

# Useful Resources

- Bash Manual
- Linux Documentation Project
- ShellCheck
- ExplainShell
