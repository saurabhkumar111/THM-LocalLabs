# TryHackMe - Windows Command Line  
## Task 8: Users, Permissions, and Security

### 📘 Task Objective:
Understand how to manage local users and groups, and how to inspect and modify file permissions using the Windows Command Prompt (`cmd.exe`).

---

### 🖥️ Environment Used:
- **Platform**: Windows 10 (VirtualBox VM)
- **Tool**: Command Prompt (`cmd.exe`) **(Run as Administrator)**
- **Context**: Local lab environment (offline)

---

### 🛠️ Commands Practiced

| Command                                         | Description                                             |
|-------------------------------------------------|---------------------------------------------------------|
| `net user`                                      | Lists all local user accounts                           |
| `net user <username>`                           | Shows details of a specific user                        |
| `net user thmuser Password123! /add`            | Creates a new user with a password                      |
| `net localgroup`                                | Lists all local groups                                  |
| `net localgroup Administrators thmuser /add`    | Adds user to the Administrators group                   |
| `net localgroup Administrators thmuser /delete` | Removes user from the group                             |
| `net user thmuser /delete`                      | Deletes the user account                                |
| `icacls secured.txt`                            | Displays file/folder permissions (ACLs)                 |
| `icacls secured.txt /grant "Users":R`           | Grants read-only access to Users group                  |
| `icacls secured.txt /grant "Saurabh Tiwary":F`  | Grants full access to your user                         |
| `icacls secured.txt /remove:g "Users"`          | Removes permissions from Users group                    |

---

### 🧪 Practical Walkthrough

```cmd
C:\Users\Saurabh Tiwary> net user
C:\Users\Saurabh Tiwary> net user Saurabh

:: Create a user
C:\Users\Saurabh Tiwary> net user thmuser Password123! /add

:: Add to Admin group
C:\Users\Saurabh Tiwary> net localgroup Administrators thmuser /add

:: Check membership
C:\Users\Saurabh Tiwary> net localgroup Administrators

:: Remove from Admin group
C:\Users\Saurabh Tiwary> net localgroup Administrators thmuser /delete

:: Delete the user
C:\Users\Saurabh Tiwary> net user thmuser /delete

:: Create a test file
C:\Users\Saurabh Tiwary> echo test > secured.txt

:: View file permissions
C:\Users\Saurabh Tiwary> icacls secured.txt

:: Grant read permission to Users
C:\Users\Saurabh Tiwary> icacls secured.txt /grant "Users":R

:: Grant full control to yourself
C:\Users\Saurabh Tiwary> icacls secured.txt /grant "Saurabh Tiwary":F

:: Remove Users group access
C:\Users\Saurabh Tiwary> icacls secured.txt /remove:g "Users"
