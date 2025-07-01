# TryHackMe - Linux Shells  
## Task 4: Shell Scripting and Components

---

### 🧠 Objective:
Understand the components of a shell script, write basic scripts, use variables, conditionals, and loops to automate tasks.

---

### 🖥️ Environment:
- **System**: Kali Linux (VirtualBox)
- **Editor Used**: `nano` or `vim`
- **Test Directory**: `~/shells-lab/task4`

---

### 🛠️ Key Script Concepts Practiced

| Component                    | Example                                    | Description                                  |
|------------------------------|--------------------------------------------|----------------------------------------------|
| Shebang                      | `#!/bin/bash`                              | Tells the OS which shell to use              |
| Variable                     | `name="Saurabh"`                           | Declares a variable                          |
| Print Output                 | `echo "Hello $name"`                       | Prints value of variable                     |
| Conditional (if)             | `if [ "$name" = "Saurabh" ]; then ... fi`  | Runs block if condition is true              |
| Loop (for)                   | `for i in 1 2 3; do echo $i; done`         | Loops through list of values                 |
| Executing a script           | `bash script.sh` or `./script.sh`         | Runs the script                              |
| Make executable              | `chmod +x script.sh`                       | Allows script to be run directly             |

---

### 🧪 Practical Walkthrough

```bash
# Create working directory
mkdir -p ~/shells-lab/task4
cd ~/shells-lab/task4

# Create a new script file
nano hello.sh


#!/bin/bash
# This is a simple shell script

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


# Make the script executable and run it
chmod +x hello.sh
./hello.sh


Hello Saurabh!
Welcome back, Saurabh!
Number: 1
Number: 2
Number: 3
