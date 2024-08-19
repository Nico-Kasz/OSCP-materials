## Enumeration

#### General
```
sudo nmap -A -p- -T5 --script "vuln" -oN nmap -oX nmap.xml
nc ip port
```

#### Web
```
nikto -o nikto -h
dirb -o dirb http://192.168.0.0
ffuf -u http://IP/FUZZ -w wordlist -recursion  
```

#### SMB
```
crackmapexec smb --users --shares --disks --loggedon-users
enum4linux -a 

mount -t cifs -o username=user,password=password //10.0.0 .3/Share /mnt/share
```

## Cracking 

#### Service Cracking
```
hydra -L users.txt -P Passwords.txt http-post-form "/path.php:user=^USER^&pass=^PASS^:F=Fail_Text"

hydra -l root -P Passwords.txt ssh://URL 
```

#### Local Cracking
```
hashcat -m 1000 NTLM.hash wordlist.txt -r rule.txt 

john 
```

## Tunneling 
```
chisel
```