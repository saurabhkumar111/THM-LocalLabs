# TryHackMe - Windows Command Line  
## Task 7: Redirection, Pipes, and Chaining Commands

### 📘 Task Objective:
Understand how to redirect command output, use pipes to chain commands, and conditionally execute commands using logical operators in the Windows Command Prompt (`cmd.exe`).

---

### 🖥️ Environment Used:
- **Platform**: Windows 10 (VirtualBox VM)
- **Tool**: Command Prompt (`cmd.exe`)
- **Context**: Offline, local execution

---

### 🛠️ Commands Practiced

| Command                                     | Description                                              |
|---------------------------------------------|----------------------------------------------------------|
| `>`                                         | Redirects (overwrites) output to a file                  |
| `>>`                                        | Redirects (appends) output to a file                     |
| `|`                                         | Pipes output of one command into another                 |
| `&&`                                        | Runs second command **only if the first succeeds**       |
| `||`                                        | Runs second command **only if the first fails**          |

---

### 🧪 Practical Walkthrough

```cmd
C:\Users\Saurabh Tiwary> mkdir chainlab
C:\Users\Saurabh Tiwary> cd chainlab

:: Redirection - Create and Append to File
C:\Users\Saurabh Tiwary\chainlab> echo First line of text > test.txt
C:\Users\Saurabh Tiwary\chainlab> echo Second line >> test.txt
C:\Users\Saurabh Tiwary\chainlab> echo Third line >> test.txt
C:\Users\Saurabh Tiwary\chainlab> type test.txt
First line of text
Second line
Third line

:: Pipe Example - Tasklist filtered
C:\Users\Saurabh Tiwary\chainlab> tasklist | findstr explorer
explorer.exe                   2432 Console                    1     25,636 K

:: Chaining - AND (&&)
C:\Users\Saurabh Tiwary\chainlab> echo Hello > hello.txt && type hello.txt
Hello

:: Chaining - OR (||)
C:\Users\Saurabh Tiwary\chainlab> dir nonexist || echo That folder does not exist
File Not Found
That folder does not exist

:: Combined chain
C:\Users\Saurabh Tiwary\chainlab> echo First > all.txt && echo Second >> all.txt && type all.txt
First
Second
