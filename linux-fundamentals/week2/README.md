# 🔐 Linux Fundamentals – Week 2 (SSH & SCP)

## 🔧 Skills Covered
- SSH login and key setup
- Using ssh-keygen and ssh-copy-id
- Secure file transfers with scp


# 🧱 Linux Fundamentals – Part 2: SSH, SSH Keys & SCP (Local Lab)

## 🎯 Objective
Learn to securely connect to remote machines using SSH, configure key-based authentication, and transfer files via SCP.

---

## 🛠️ Lab Setup
- **Attacker VM**: Kali Linux  
- **Target VM**: Metasploitable 2  
- Both should be on the same internal VirtualBox network.

---

## 🔹 Step 1: Start SSH on Target (Metasploitable)

```bash
sudo service ssh status    # Check status
sudo service ssh start     # Start if not running
ip a                       # Note the IP address


ssh msfadmin@<Metasploitable-IP>

ssh-keygen


ssh-copy-id msfadmin@<Metasploitable-IP>


ssh msfadmin@<Metasploitable-IP>


## 🔜 Next Up
- Linux Fundamentals Part 3: Permissions & Processes
