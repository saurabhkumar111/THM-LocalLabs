# TryHackMe - Windows Command Line  
## Task 3: Navigating the Filesystem

### 📘 Task Objective:
Practice navigating the Windows filesystem using the Command Prompt (`cmd.exe`) and learn how to manage directories and files.

---

### 🖥️ Environment Used:
- **Platform**: Windows 10 (Local VirtualBox VM)
- **Tool**: Command Prompt (`cmd.exe`)
- **Execution Context**: Standard user shell (no admin required)

---

### 🛠️ Commands Practiced

| Command                          | Description                                      |
|----------------------------------|--------------------------------------------------|
| `cd`                             | Displays or changes the current directory        |
| `dir`                            | Lists files and folders in the current directory |
| `cls`                            | Clears the screen                                |
| `mkdir testfolder`               | Creates a new folder called `testfolder`         |
| `cd testfolder`                  | Enters the new folder                            |
| `echo Hello THM! > notes.txt`    | Creates a file and writes a line of text         |
| `type notes.txt`                 | Displays the contents of the file                |
| `cd ..`                          | Moves back to the parent directory               |
| `del testfolder\notes.txt`       | Deletes the file created                         |
| `rmdir testfolder`               | Removes the now-empty folder                     |

---

### 🧪 Practical Walkthrough (Command Output Sample):

```cmd
C:\Users\Saurabh Tiwary> mkdir testfolder
C:\Users\Saurabh Tiwary> cd testfolder
C:\Users\Saurabh Tiwary\testfolder> echo Hello THM! > notes.txt
C:\Users\Saurabh Tiwary\testfolder> type notes.txt
Hello THM!
C:\Users\Saurabh Tiwary\testfolder> cd ..
C:\Users\Saurabh Tiwary> del testfolder\notes.txt
C:\Users\Saurabh Tiwary> rmdir testfolder
