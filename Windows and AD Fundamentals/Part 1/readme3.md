# 🪟 Windows Fundamentals 3 – TryHackMe (Local Lab)

> **Path**: Cybersecurity 101  
> **Room**: Windows Fundamentals 3  
> **Platform**: TryHackMe  
> **Lab Type**: Local (VirtualBox)  
> **Machine Used**: Windows 10 VM  
> **Status**: ✅ Completed

---

## 📌 Lab Objectives

Explore system configuration tools and built-in security features of Windows 10:

- System Configuration (msconfig)
- UAC (advanced levels)
- Resource Monitoring
- Windows Registry
- Services Management
- Windows Update
- Windows Security Center
- Firewall
- SmartScreen Protection

---

## 🔧 System Tools & Configuration

### 1. ⚙️ System Configuration (`msconfig`)

- Opened via: `Win + R → msconfig`
- Explored:
  - **General tab**: Selective startup
  - **Boot tab**: Safe boot options
  - **Services tab**: Viewed background services
  - **Tools tab**: Launched Event Viewer and more
- Observed redirection of startup tab to Task Manager

---

### 2. 🛡️ Advanced UAC Settings

- Accessed via:  
  `Control Panel → User Accounts → Change UAC settings`
- Changed level to **“Always Notify”**
- Observed prompts for:
  - `cmd.exe` (as Admin)
  - `regedit.exe`

---

### 3. 📊 Resource Monitor (`resmon`)

- Opened via:
  - `Win + R → resmon`, or
  - Task Manager → Performance tab → Open Resource Monitor
- Explored tabs:
  - **CPU**: Live usage by processes
  - **Memory**: Real-time RAM usage
  - **Disk**: Read/Write stats
  - **Network**: Bandwidth per app

---

### 4. 🧠 Windows Registry (`regedit`)

- Opened via: `Win + R → regedit`
- Explored:
  - `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run`
  - `HKEY_CURRENT_USER\Software`
- Created & deleted a dummy key:
  - Key: `TryHackMeTest`
  - String: `test = 123`

---

### 5. 🧰 Services Management (`services.msc`)

- Opened via: `Win + R → services.msc`
- Observed:
  - List of all Windows services
  - Status: Running / Stopped
  - Startup types: Manual, Auto, Disabled
- Restarted `Windows Update` service as test

---

## 🛡️ Windows Security Features

### 6.1 🔄 Windows Update

- Accessed via: `Settings → Update & Security → Windows Update`
- Actions performed:
  - Clicked **Check for updates**
  - Viewed update history
  - Explored **Advanced options**

---

### 6.2 🛡️ Windows Security Center (Defender)

- Opened via:  
  `Settings → Update & Security → Windows Security → Open Windows Security`
- Explored tabs:

| Section                      | Action Taken                                               |
|------------------------------|------------------------------------------------------------|
| **Virus & Threat Protection** | Ran Quick Scan, viewed threat history                      |
| **Account Protection**        | Checked account security status                            |
| **Firewall & Network**        | Viewed firewall status for all 3 profiles                  |
| **App & Browser Control**     | Checked SmartScreen settings                               |
| **Device Security**           | Viewed Core Isolation / Secure Boot (if supported)         |
| **Device Performance**        | Reviewed health report                                     |

---

### 6.3 🔥 Windows Firewall

- Opened via:
  - `Control Panel → Windows Defender Firewall`, or
  - `Windows Security → Firewall & Network Protection`
- Observed:
  - Firewall status for Domain, Private, and Public profiles
  - App permission settings
  - Default rules view

---

### 6.4 ⚠️ SmartScreen Protection

- Accessed via: `Windows Security → App & Browser Control`
- Checked settings:
  - SmartScreen for Microsoft Edge
  - SmartScreen for app installations
- Ensured reputation-based protection was **enabled**

---

## 🛠️ Tools Used

| Tool                  | Purpose                                      |
|-----------------------|----------------------------------------------|
| `msconfig`            | System configuration                         |
| `resmon`              | Advanced resource monitoring                 |
| `regedit`             | Windows Registry editor                      |
| `services.msc`        | Service manager                              |
| Windows Update        | System patch management                      |
| Windows Security      | Central security dashboard                   |
| Windows Firewall      | Network traffic protection                   |
| SmartScreen           | App and browser protection                   |

---

## ✅ Completion Status

All tools and settings explored and tested in a Windows 10 VM (locally).  
BitLocker excluded (not available in current edition).  
No third-party tools were used.

---
