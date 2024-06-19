---
date: 2024-06-19
author: mrashco
title: easy-peasy
tags: 
categories: 
series:
---
[YouTube Walkthrough](https://youtu.be/0ahKui2eBjs)

rustscan: 80:http, 6498:ssh, 65524:http

feroxbuster: 80, /hidden/whatever, view-source:base64

65524:viewsource search “flag”

65524/robots.txt [^](https://md5hashing.net/hash/md5/a18672860d0510e5ab6699730763b250), view-source:Base62 = $directory

- hashcat -m 6900 $hash $dict
- steghide --extract -sf $img, cat $file.txt, binary cyberchef
- ssh b*****@$ip -p 6498

cat crontab, nano $file > revshell [^](https://www.revshells.com/), cat $.root.txt