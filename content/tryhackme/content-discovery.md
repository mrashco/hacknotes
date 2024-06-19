---
date: 2024-06-19
author: mrashco
title: Content Discovery
tags: ["", ""]
categories: 
series:
---
Content
- assets (files, vids, imgs...), features + more.

Discovery (methods)
- manual, automated and OSINT + combination.

Manual
- /robots.txt, `favicon | md5sum` [^](https://wiki.owasp.org/index.php/OWASP_favicon_database), sitemap.xml, headers `curl $ipa -v`, framework stack via comments, (c) notices or credits.

OSINT
- [GoogleDork](https://en.wikipedia.org/wiki/Google_hacking)(site, inurl, filetype, intitle), wappalyzer, [wayback](https://archive.org/web/), github, S3 Buckets http(s)://*{name}*.s3.amazonaws.com.

Automated:
- fuzzing(dirb, gobust, fuff, ferox).