##We are going to do basic of Hacking

#Enumeration
1. nmap -Sc -sV <`ip address>
2. nmap -sT <'ip address>
3. nmap -sP <'ip address>

#Enumeration
1. gobuster dir -u <`ip address> -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

BruteForcing

1. hydra -L fsocity.txt -p mypassword 192.168.10.100 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log In:Invalid username"