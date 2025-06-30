# 🪟 Windows Fundamentals 3 – TryHackMe (Local Lab)

> **Path**: Cybersecurity 101  
> **Room**: Windows Fundamentals 3  
> **Platform**: TryHackMe  
> **Lab Type**: Local (VirtualBox)  
> **Machine Used**: Windows 10 VM  
> **Status**: ✅ Completed

---

## 📌 Lab Objectives

Learn about advanced system-level features of Windows:

- System Configuration (msconfig)
- Advanced UAC settings
- Resource Monitoring
- Windows Registry
- System Services

---

## 🔍 Task-wise Breakdown & Commands

### 1. ⚙️ System Configuration (`msconfig`)

- Opened via: `Win + R → msconfig`
- Explored:
  - General tab: Selective startup
  - Boot tab: Safe boot options
  - Services tab: Viewed background services
  - Tools tab: Access to utilities like Event Viewer
- Verified startup redirection to Task Manager

---

### 2. 🛡️ Advanced UAC Settings

- Navigated to:  
  `Control Panel → User Accounts → Change User Account Control settings`
- Changed UAC level to **“Always Notify”**
- Observed:
  - Prompt when running `cmd.exe` as admin
  - Prompt when launching `regedit.exe`

---

### 3. 📊 Resource Monitor (`resmon`)

- Opened via:
  - `Win + R → resmon`, or
  - Task Manager → Performance → Resource Monitor
- Explored tabs:
  - **CPU**: Monitored real-time process usage
  - **Memory**: RAM allocation by processes
  - **Disk**: Read/Write I/O
  - **Network**: App-wise bandwidth usage
- Tested:
  - Opened and closed apps to see real-time changes

---

### 4. 🧠 Windows Registry (`regedit`)

- Opened via: `Win + R → regedit`
- Explored:
  - `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run`
  - `HKEY_CURRENT_USER\Software`
- Created a **dummy registry key**:
  - Key name: `TryHackMeTest`
  - String: `test = 123`
- Deleted the key afterward

---

### 5. 🧰 Services Management (`services.msc`)

- Opened via: `Win + R → services.msc`
- Observed:
  - List of system services with their status (Running/Stopped)
  - Startup type: Manual / Automatic / Disabled
- Interacted with a service:
  - Right-clicked `Windows Update` → Restarted it

---

## 🛠️ Tools Used

| Tool             | Purpose                              |
|------------------|--------------------------------------|
| msconfig         | System boot & services configuration |
| Control Panel    | Adjust UAC levels                    |
| resmon           | Resource usage monitoring            |
| regedit          | Registry inspection and editing      |
| services.msc     | Manage system-level services         |

---

