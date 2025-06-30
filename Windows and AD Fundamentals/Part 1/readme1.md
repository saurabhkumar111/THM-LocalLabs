# 🪟 Windows Fundamentals 1 – TryHackMe (Local Lab)

> **Path**: Cybersecurity 101  
> **Room**: Windows Fundamentals 1  
> **Platform**: TryHackMe  
> **Lab Type**: Local (VirtualBox)  
> **Machine Used**: Windows 10 VM  
> **Status**: ✅ Completed

---

## 📌 Lab Objectives

Understand the fundamentals of the Windows operating system, focusing on:

- Graphical User Interface (GUI) components
- NTFS file system and file streams
- User Account Control (UAC)
- The Control Panel and Settings
- Task Manager and system configuration tools

---

## 🖥️ Environment Setup

| Component   | Details                  |
|------------|---------------------------|
| VirtualBox | Installed on Host Machine |
| OS         | Windows 10 (Clean Install)|
| Tools      | Native Windows Tools Only |
| Snapshot   | Taken after clean install |

---

## 🔍 Task-wise Breakdown & Commands

### 1. 🧭 Exploring the Windows GUI
- Navigated:
  - Start Menu
  - Taskbar
  - File Explorer
- Observed folder structure:
  - `C:\Users\`
  - `C:\Program Files\`

---

### 2. 📁 NTFS File System

#### ✔️ Tested Alternate Data Streams (ADS):

```cmd
echo Hello > normal.txt
echo HiddenData > normal.txt:hidden.txt
more < normal.txt:hidden.txt
```

---

### 3. 🛡️ User Account Control (UAC)
Navigated to:


Control Panel > User Accounts > Change UAC settings
Adjusted UAC level.

Observed UAC prompts by running:

cmd.exe as Administrator

regedit.exe


----

### 4. ⚙️ Control Panel & System Settings
Explored:

Control Panel (via Run > control)

Modern Settings (Win + I)

Viewed:

System Info

User Accounts

Installed Programs

### 5. 🧠 Task Manager & System Configuration
Opened Task Manager (Ctrl + Shift + Esc)

Observed running processes, startup impact, users

Ran msconfig

Checked boot options and services

Ran:

Collected system-level details




