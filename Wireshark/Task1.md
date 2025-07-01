# TryHackMe - Wireshark Basics (Local Lab in VirtualBox)

## 🧠 Objective:
Perform local packet capture and protocol analysis using Wireshark in Kali Linux by generating real traffic to Metasploitable VM.

---

## 🧰 Lab Environment

| Machine         | Purpose                   |
|----------------|---------------------------|
| Kali Linux      | Attacker / Analysis host |
| Metasploitable2 | Vulnerable target        |
| Tool Used       | Wireshark (on Kali)      |

---

## 📥 Step 1: Install Wireshark on Kali

```bash
sudo apt update
sudo apt install wireshark -y


sudo usermod -aG wireshark $USER

wireshark &


curl http://192.168.1.5


nmap -sV 192.168.1.5


http || (tcp.len > 0 && !tcp.analysis.keep_alive)
