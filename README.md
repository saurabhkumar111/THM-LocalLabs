# THM-LocalLabs
Hands-on Linux lab practice for cybersecurity and ethical hacking. Includes command usage, SSH, scripting, and system management basics.

# 🐧 Linux Fundamentals - Week 1

This document includes my hands-on practice and notes from Week 1 of Linux fundamentals training for cybersecurity.

---

## 📌 Topics Covered

- Linux command line navigation
- File and directory operations
- Hidden files and permissions
- Manual pages (`man`)
- Pipes and redirection
- Searching files

---

## 🧪 Commands Practiced

### 📁 Navigation & Files
```bash
pwd
ls -la
cd /home/kali
mkdir testlab
touch test.txt
cp test.txt copy.txt
mv copy.txt renamed.txt
rm renamed.txt
🔐 Permissions & Hidden Files
bash
Copy
Edit
touch .hiddenfile
ls -a
chmod 755 test.txt
chown kali test.txt
📚 Manual Pages
bash
Copy
Edit
man ls
man chmod
➡️ Redirection & Pipes
bash
Copy
Edit
echo "Hello" > file.txt
cat file.txt | grep Hello
cat file.txt | wc -l
🔍 Searching
bash
Copy
Edit
find / -name "file.txt" 2>/dev/null
📸 Screenshots
Add screenshots of terminal outputs here or upload them to the screenshots/ folder and link them here.

🧠 Lessons Learned
Importance of file permissions in Linux

How to use find, grep, and redirection for efficient searching

Use of man for learning commands

