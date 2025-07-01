# TryHackMe - Windows Command Line  
## Task 5: File Attributes and Extensions

### 📘 Task Objective:
Learn how to inspect and modify file attributes (such as hidden or read-only) using `attrib`, and how to view all files including hidden/system files using `dir /a`.

---

### 🖥️ Environment Used:
- **Platform**: Windows 10 (VirtualBox VM)
- **Tool**: Command Prompt (`cmd.exe`)
- **Context**: Local lab setup (no AttackBox needed)

---

### 🛠️ Commands Practiced

| Command                             | Description                                    |
|-------------------------------------|------------------------------------------------|
| `mkdir file-attributes-demo`        | Create a working folder                        |
| `cd file-attributes-demo`           | Enter the folder                               |
| `echo This is a visible file. > visible.txt` | Create a new text file                        |
| `attrib visible.txt`               | View current attributes of the file            |
| `attrib +h +r visible.txt`         | Set file as Hidden and Read-Only               |
| `attrib -h -r visible.txt`         | Remove Hidden and Read-Only flags              |
| `dir /a`                           | List all files, including hidden/system files  |
| `echo Overwritten successfully > visible.txt` | Confirm write access after removing Read-Only |
| `type visible.txt`                 | Display file content                           |
| `cd ..` / `rmdir /s /q file-attributes-demo` | Cleanup                                       |

---

### 🧪 Practical Walkthrough (Command Output Sample)

```cmd
C:\Users\Saurabh Tiwary> mkdir file-attributes-demo
C:\Users\Saurabh Tiwary> cd file-attributes-demo
C:\Users\Saurabh Tiwary\file-attributes-demo> echo This is a visible file. > visible.txt
C:\Users\Saurabh Tiwary\file-attributes-demo> attrib visible.txt
A                visible.txt
C:\Users\Saurabh Tiwary\file-attributes-demo> attrib +h +r visible.txt
C:\Users\Saurabh Tiwary\file-attributes-demo> attrib visible.txt
A  R  H          visible.txt
C:\Users\Saurabh Tiwary\file-attributes-demo> echo Trying to overwrite > visible.txt
Access is denied.
C:\Users\Saurabh Tiwary\file-attributes-demo> attrib -h -r visible.txt
C:\Users\Saurabh Tiwary\file-attributes-demo> echo Overwritten successfully > visible.txt
C:\Users\Saurabh Tiwary\file-attributes-demo> type visible.txt
Overwritten successfully
C:\Users\Saurabh Tiwary\file-attributes-demo> dir /a
