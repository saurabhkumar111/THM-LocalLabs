# TryHackMe - Linux Shells  
## Task 5: The Locker Script (Challenge)

---

### 🧠 Objective:
Use your knowledge of shell scripting to write a script that searches the `/var/log` directory for a flag file and prints it to the terminal.

---

### 🖥️ Environment:
- **System**: Kali Linux (VirtualBox)
- **Directory**: `~/shells-lab/task5`
- **Challenge Folder**: `/var/log` (read-only system logs)

---

### 🔐 Challenge Goal:
- Write a script called `locker.sh` that:
  - Recursively searches `/var/log`
  - Finds a file named `flag.txt`
  - Reads and displays its contents

---

### 🛠️ Script Structure

```bash
#!/bin/bash
# locker.sh - Script to find and display the flag

echo "[*] Searching for the flag in /var/log..."

flag_path=$(find /var/log -type f -name "flag.txt" 2>/dev/null)

if [ -n "$flag_path" ]; then
    echo "[+] Flag found at: $flag_path"
    echo "[+] Contents of the flag:"
    cat "$flag_path"
else
    echo "[-] No flag.txt found in /var/log"
fi

# 1. Create working directory
mkdir -p ~/shells-lab/task5
cd ~/shells-lab/task5

# 2. Create the script
nano locker.sh

# 3. Paste the script above and save (CTRL+X → Y → Enter)

# 4. Make it executable
chmod +x locker.sh

# 5. Run the script
./locker.sh


[*] Searching for the flag in /var/log...
[+] Flag found at: /var/log/some/deep/folder/flag.txt
[+] Contents of the flag:
THM{example-flag-content}

