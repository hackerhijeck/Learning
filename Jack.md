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
  Ans: username: wendy
```
