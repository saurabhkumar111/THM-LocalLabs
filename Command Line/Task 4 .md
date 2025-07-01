# TryHackMe - Windows Command Line  
## Task 4: File and Folder Manipulation

### 📘 Task Objective:
Learn to create, copy, rename, move, and delete files and folders using the Windows Command Prompt (`cmd.exe`).

---

### 🖥️ Environment Used:
- **Platform**: Windows 10 (VirtualBox VM)
- **Tool**: Command Prompt (`cmd.exe`)
- **Context**: Local practice without TryHackMe AttackBox

---

### 🛠️ Commands Practiced

| Command                               | Description                                      |
|---------------------------------------|--------------------------------------------------|
| `mkdir workspace`                     | Creates a new folder named `workspace`           |
| `cd workspace`                        | Enters the `workspace` directory                 |
| `echo This is my first file > file1.txt` | Creates a text file with sample content         |
| `copy file1.txt file2.txt`           | Copies `file1.txt` to a new file `file2.txt`     |
| `move file2.txt renamed.txt`         | Renames `file2.txt` to `renamed.txt`             |
| `mkdir subfolder`                    | Creates a new subfolder                          |
| `move renamed.txt subfolder\`        | Moves file into the `subfolder`                  |
| `del file1.txt`                      | Deletes `file1.txt`                              |
| `cd subfolder`                       | Navigates into the subfolder                     |
| `del renamed.txt`                    | Deletes the file inside the subfolder            |
| `cd ..`                              | Goes back to parent folder                       |
| `rmdir subfolder`                    | Deletes the empty `subfolder`                    |
| `cd ..`                              | Returns to Desktop or upper directory            |
| `rmdir workspace`                    | Deletes the empty `workspace` folder             |

---

### 🧪 Practical Walkthrough (Command Output Sample)

```cmd
C:\Users\Saurabh Tiwary> mkdir workspace
C:\Users\Saurabh Tiwary> cd workspace
C:\Users\Saurabh Tiwary\workspace> echo This is my first file > file1.txt
C:\Users\Saurabh Tiwary\workspace> copy file1.txt file2.txt
C:\Users\Saurabh Tiwary\workspace> move file2.txt renamed.txt
C:\Users\Saurabh Tiwary\workspace> mkdir subfolder
C:\Users\Saurabh Tiwary\workspace> move renamed.txt subfolder\
C:\Users\Saurabh Tiwary\workspace> del file1.txt
C:\Users\Saurabh Tiwary\workspace> cd subfolder
C:\Users\Saurabh Tiwary\workspace\subfolder> del renamed.txt
C:\Users\Saurabh Tiwary\workspace\subfolder> cd ..
C:\Users\Saurabh Tiwary\workspace> rmdir subfolder
C:\Users\Saurabh Tiwary\workspace> cd ..
C:\Users\Saurabh Tiwary> rmdir workspace
