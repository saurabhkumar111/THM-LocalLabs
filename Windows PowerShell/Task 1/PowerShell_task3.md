# TryHackMe - Windows PowerShell  
## Task 3: Navigating the File System and Working with Files

### 🧠 Objective:
Practice directory navigation, file and folder creation, content manipulation, and cleanup using PowerShell cmdlets.

---

### 🖥️ Environment:
- **System**: Windows 10 (VirtualBox VM)
- **Shell**: Windows PowerShell (Admin or normal)
- **Log File**: `powershell_task3.txt` (optional)

---

### 🛠️ Commands Practiced:

| Command                                                  | Description                                 |
|-----------------------------------------------------------|---------------------------------------------|
| `Get-Location`                                            | Shows current working directory             |
| `cd <path>`                                               | Changes current directory                   |
| `Get-ChildItem` / `ls`                                    | Lists contents of a directory               |
| `New-Item -ItemType Directory -Path <path>`               | Creates a new folder                        |
| `New-Item -ItemType File -Path <path>`                    | Creates a new file                          |
| `Set-Content -Path <file> -Value "<text>"`                | Writes (overwrites) content in a file       |
| `Add-Content -Path <file> -Value "<text>"`                | Appends content to a file                   |
| `Get-Content <file>`                                      | Reads contents of a file                    |
| `Rename-Item -Path <old> -NewName <new>`                  | Renames a file or folder                    |
| `Remove-Item <path>`                                      | Deletes a file or folder                    |
| `Remove-Item <path> -Recurse`                             | Deletes a folder and its contents           |

---

### 🧪 Practical Walkthrough

```powershell
Start-Transcript -Path "$HOME\Desktop\powershell_task3.txt"

# Navigation
Get-Location
cd ..
cd "$HOME\Desktop"

# Create directory and file
New-Item -ItemType Directory -Path "$HOME\Desktop\pslab"
New-Item -ItemType File -Path "$HOME\Desktop\pslab\info.txt"

# Write and append content
Set-Content -Path "$HOME\Desktop\pslab\info.txt" -Value "Hello PowerShell"
Add-Content -Path "$HOME\Desktop\pslab\info.txt" -Value "This is Task 3"

# Read and rename
Get-Content "$HOME\Desktop\pslab\info.txt"
Rename-Item -Path "$HOME\Desktop\pslab\info.txt" -NewName "task3.txt"

# Clean up
Remove-Item "$HOME\Desktop\pslab\task3.txt"
Remove-Item "$HOME\Desktop\pslab" -Recurse

Stop-Transcript
