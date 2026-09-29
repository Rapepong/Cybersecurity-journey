# TryHackMe(THM) -> Use AttackBox on Kali Linux

## PickleRick's Room

whoami, pwd, ls -la, cat (less, more ,head, tail, tac, strings)

gobuster dir -u http://<IP> -w /usr/share/wordlists/dirb/common.txt -x php,txt,html
gobuster -> Using Brute-force(random until found)
-w /usr/share/wordlists/dirb/common.txt -> Format for finding common filename in Kali Linux and Parrot OS
dirb/common.txt ~4,600 common words (Quick Scan) | directory-list-2.3-medium.txt ~220K common words (Deep Scan)

sudo stand for Superuser DO (Run as Administrator)

sudo bash 
"# or"
sudo su

sudo -l = Display which command that admin permit user to do

Use Ctrl + U to open source_view

find /home/rick -type f -name "*second*" -> f = file, d = directory (Command for specific path)
find / -type f -name "*second*" 2>/dev/null -> (Don't know specific path) 2>/dev/null = If which file can't access just ignore show only what you can show

grep stand for Global Regular Expression Print = Command that find hiding word in file (Like Ctrl + F)

grep -rn "jerry" / 2>/dev/null -> -r (recursive) is read every file in folder, -n (line number) is which line on that text, i (ignore case) ignore capital word

grep -i "jerry" /home/rick/note.txt

| command that usually combine with grep | is pipe -> Do first command and do next instant instance of -> ls -la | grep "rick", cat /etc/passwd | grep "www-data"
