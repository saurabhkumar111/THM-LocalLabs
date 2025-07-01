# TryHackMe - Windows Command Line  
## Task 2: Basic System Information

### 📘 Task Objective:
Gather and understand basic system information using Windows Command Prompt (`cmd.exe`).

---

### 🖥️ Environment Used:
- **Local Virtual Machine**: Windows 10 (VirtualBox)
- **Command Line Tool**: Command Prompt (`cmd.exe`)
- **Execution Path**: Commands executed from local user context

---

### 🛠️ Commands Practiced:

| Command                                | Description                                     |
|----------------------------------------|-------------------------------------------------|
| `systeminfo`                           | Displays detailed system configuration info     |
| `hostname`                             | Shows the computer's hostname                   |
| `echo %USERNAME%`                      | Prints the current user's username              |
| `echo %USERDOMAIN%`                    | Shows the user's domain                         |
| `echo %COMPUTERNAME%`                  | Displays the computer's network name            |
| `ver`                                  | Displays the Windows version                    |
| `whoami`                               | Shows full user context (`DOMAIN\username`)     |
| `tasklist`                             | Lists all currently running processes           |
| `wmic cpu get name`                    | Displays the CPU model                          |
| `wmic os get caption`                  | Displays OS name                                |

---

### 📂 Output Storage:

To save the output of systeminfo:

```cmd

