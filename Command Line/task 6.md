# TryHackMe - Windows Command Line  
## Task 6: Searching for Files and Content

### 📘 Task Objective:
Learn how to locate files and search for specific content inside files using `cmd.exe` tools such as `dir`, `findstr`, and `where`.

---

### 🖥️ Environment Used:
- **Platform**: Windows 10 (VirtualBox VM)
- **Tool**: Command Prompt (`cmd.exe`)
- **Context**: Local lab setup (offline from TryHackMe)

---

### 🛠️ Commands Practiced

| Command                            | Description                                            |
|------------------------------------|--------------------------------------------------------|
| `dir *.txt /s /b`                  | Recursively lists all `.txt` files (bare format)       |
| `findstr test *.txt`              | Searches for the word "test" inside `.txt` files       |
| `findstr secret *.*`              | Searches for "secret" in all files in the folder       |
| `where notepad`                   | Locates full path of `notepad.exe` using PATH          |
| `move *.log archive\`             | Moves all `.log` files to a folder named `archive`     |
| `rmdir /s /q search-lab`          | Deletes a directory and all contents recursively       |

---

### 🧪 Practical Walkthrough

```cmd
C:\Users\Saurabh Tiwary> mkdir search-lab
C:\Users\Saurabh Tiwary> cd search-lab
C:\Users\Saurabh Tiwary\search-lab> echo This is a test file. > file1.txt
C:\Users\Saurabh Tiwary\search-lab> echo TryHackMe is awesome! > file2.txt
C:\Users\Saurabh Tiwary\search-lab> echo Another test for searching. > notes.txt
C:\Users\Saurabh Tiwary\search-lab> echo Some secret hidden stuff > secret.log

C:\Users\Saurabh Tiwary\search-lab> dir *.txt /s /b
C:\Users\Saurabh Tiwary\search-lab\file1.txt
C:\Users\Saurabh Tiwary\search-lab\file2.txt
C:\Users\Saurabh Tiwary\search-lab\notes.txt

C:\Users\Saurabh Tiwary\search-lab> findstr test *.txt
file1.txt:This is a test file.
notes.txt:Another test for searching.

C:\Users\Saurabh Tiwary\search-lab> findstr secret *.*
secret.log:Some secret hidden stuff

C:\Users\Saurabh Tiwary\search-lab> where notepad
C:\Windows\System32\notepad.exe

C:\Users\Saurabh Tiwary\search-lab> mkdir archive
C:\Users\Saurabh Tiwary\search-lab> move *.log archive\

C:\Users\Saurabh Tiwary\search-lab> cd ..
C:\Users\Saurabh Tiwary> rmdir /s /q search-lab
