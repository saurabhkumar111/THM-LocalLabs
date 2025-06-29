# 🛡️ Linux Fundamentals – Part 3: File Permissions & Process Management

## 🎯 Objectives
- Understand `rwx` permission system
- Practice changing ownership and permissions
- Learn process control with `ps`, `kill`, `nice`, `renice`, `top`, `htop`
- Write and run a basic Bash script

---

## 🔧 Practice Steps

### ✅ Create File & View Permissions
```bash
mkdir part3-practice
cd part3-practice
touch testfile.txt
ls -l testfile.txt



chmod +x testfile.txt
chmod 777 testfile.txt
chmod 644 testfile.txt


sudo chown root testfile.txt
sudo chown kali testfile.txt



ps aux
top
sudo apt install htop
htop


ping 8.8.8.8 > /dev/null &
ps aux | grep ping
kill <PID>

 
nice -n 10 sleep 100 &
ps -eo pid,ni,comm | grep sleep


sudo renice -n 5 -p <PID>



echo -e '#!/bin/bash\necho "Hello from Part 3!"' > hello.sh
chmod +x hello.sh
./hello.sh   


