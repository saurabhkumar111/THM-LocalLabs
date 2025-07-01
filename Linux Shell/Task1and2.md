# TryHackMe - Linux Shells  
## Tasks 1 & 2: Introduction to Linux Shells + Interacting with the Shell

---

### 🧠 Objective:
- Understand what a shell is and how to interact with it.
- Practice basic Linux commands for navigation, file handling, and command-line utilities.

---

### 🖥️ Environment:
- **System**: Kali Linux (VirtualBox)
- **Shell**: Bash (`/bin/bash`)
- **Lab Directory**: `~/shells-lab`

---

### 🛠️ Commands Practiced

| Command                            | Purpose                                      |
|------------------------------------|----------------------------------------------|
| `echo $SHELL`                     | Shows the current shell                      |
| `whoami`                          | Prints the current user                      |
| `pwd`                             | Displays the current working directory       |
| `ls`, `ls -l`, `ls -a`, `ls -lh`  | Lists directory contents with variations     |
| `cd <path>`, `cd ~`               | Changes directory                            |
| `mkdir <dir>`                     | Creates a new directory                      |
| `touch <file>`                    | Creates a new empty file                     |
| `echo "text" > file.txt`          | Writes text to a file (overwrite)            |
| `cat <file>`                      | Displays contents of a file                  |
| `grep <pattern> <file>`           | Searches for pattern inside file             |
| `file <filename>`                | Identifies file type                         |
| `which <command>`                | Shows full path of a command binary          |
| `history`                         | Displays previously run commands             |

---

### 🧪 Practical Walkthrough

```bash
# Task 1: Shell Basics
echo $SHELL           # Check default shell
whoami                # Confirm logged-in user

# Task 2: Navigation and Files
pwd                   # Print current working directory
ls                    # List files
ls -l
ls -a
ls -lh

cd /tmp               # Move to temp directory
pwd
cd ~                  # Return to home

mkdir shells-lab      # Create new lab folder
cd shells-lab
touch info.txt        # Create a text file

echo "Hello Linux Shell" > info.txt
cat info.txt

grep "Linux" info.txt # Search for word in file
file info.txt         # Show file type
which grep            # Show location of command
history               # View command history
