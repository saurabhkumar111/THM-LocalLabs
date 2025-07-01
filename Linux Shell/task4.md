# TryHackMe - Linux Shells  
## Task 4: Shell Scripting and Components

---

### 🧠 Objective:
Understand the structure of a shell script, how to declare variables, use conditionals, loops, and execute scripts.

---

### 🖥️ Environment:
- **System**: Kali Linux (VirtualBox)
- **Directory**: `~/shells-lab/task4`
- **Editor**: nano or vim
- **Shell**: Bash (`#!/bin/bash`)

---

### 🛠️ Commands and Concepts Practiced

| Component               | Example                                      | Purpose                                         |
|------------------------|----------------------------------------------|-------------------------------------------------|
| Shebang                | `#!/bin/bash`                                | Defines shell interpreter                       |
| Variable Declaration   | `name="Saurabh"`                             | Stores data in a variable                       |
| Print Statement        | `echo "Hello $name"`                         | Displays output                                 |
| Conditional Statement  | `if [ "$name" = "Saurabh" ]; then ... fi`    | Executes block if condition is true             |
| Loop                   | `for i in 1 2 3; do echo $i; done`           | Iterates over a list                            |
| Execute Script         | `./script.sh` or `bash script.sh`           | Runs the script                                 |
| Make Executable        | `chmod +x script.sh`                         | Grants execute permission to script             |

---

### 🧪 Practical Steps

```bash
# 1. Create working directory
mkdir -p ~/shells-lab/task4
cd ~/shells-lab/task4

# 2. Create script
nano hello.sh



#!/bin/bash
# This is a basic shell script demo

name="Saurabh"
echo "Hello $name!"

if [ "$name" = "Saurabh" ]; then
    echo "Welcome back, $name!"
else
    echo "Who are you?"
fi

for i in 1 2 3
do
    echo "Number: $i"
done


# 3. Save and run script
chmod +x hello.sh
./hello.sh

Hello Saurabh!
Welcome back, Saurabh!
Number: 1
Number: 2
Number: 3

