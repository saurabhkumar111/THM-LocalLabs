# Week 1 Notes

# 🐧 Linux Fundamentals – Week 1 (TryHackMe Local Lab)

## 🛠️ Lab Setup
- Kali Linux (VirtualBox)
- No internet, fully offline replication
- Practicing TryHackMe’s "Linux Fundamentals Part 1" locally

## ✅ Commands Practiced

### 📁 Navigation
```bash
pwd
ls -la
cd /home/kali


mkdir testlab
touch file.txt
cp file.txt copy.txt
mv copy.txt renamed.txt
rm renamed.txt
 


touch .hiddenfile
chmod 755 file.txt
chown kali file.txt
ls -a


echo "Hello" > hello.txt
cat hello.txt | grep Hello
cat hello.txt | wc -l


find / -name hello.txt 2>/dev/null


