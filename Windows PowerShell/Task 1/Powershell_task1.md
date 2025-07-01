# TryHackMe - Windows PowerShell  
## Task 1: Introduction to PowerShell

### 🧠 Objective:
Familiarize with PowerShell, its version, and basic built-in cmdlets. Learn how to start a transcript to log your commands and outputs.

---

### 🖥️ Environment:
- **System**: Windows 10 (VirtualBox VM)
- **Shell**: Windows PowerShell (Admin mode)
- **Log File**: `powershell_task1.txt` (attached separately)

---

### 🛠️ Commands Practiced:

| Command                                      | Description                                     |
|----------------------------------------------|-------------------------------------------------|
| `Start-Transcript -Path "<path>"`           | Starts logging the session to a file           |
| `$PSVersionTable`                            | Displays PowerShell version info               |
| `Get-Process`                                | Lists running processes                        |
| `Get-Date`                                   | Shows current system date and time             |
| `Get-Command`                                | Lists all available cmdlets                    |
| `Get-Command -Noun Process`                  | Lists cmdlets related to "Process"             |
| `Get-Help Get-Process`                       | Shows help information for `Get-Process`       |
| `Stop-Transcript`                            | Stops the logging session                      |

---

### 🧪 Practical Walkthrough (Transcript Logged)

1. Started PowerShell as Administrator.
2. Ran `Start-Transcript` to begin logging:
   ```powershell
   Start-Transcript -Path "$HOME\Desktop\powershell_task1.txt"
