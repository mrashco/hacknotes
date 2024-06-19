---
date: 2024-06-19
author: mrashco
title: ctfcollectionvol1
tags: 
categories: 
series:
---
[YouTube Walkthrough](https://youtu.be/hwJaHmoHSZ4)
- CyberChef > base64
- `strings $file` or `exiftool`
- `steghide --extract -sf $file`
- Inspect (CTRL + SHIFT + C)
- `zbarimg $file` [^](https://tuxthink.blogspot.com/2014/01/qr-code-encode-and-decode-qr-code-on.html)
- `strings $file`
- CyberChef > Base58
- CyberChef > ROT13 > ROT7
- Inspect (CTRL + SHIFT + C)
- `xxd -p $file > $newFile`
    - `nano $newFile`, replace 2333445f w/ 89504E47 [^](https://en.wikipedia.org/wiki/PNG)
    - CyberChef > Upload $newFile > From Hex > Render Image
- Google Dork `site:"reddit.com" intext:"THM" intitle:"tryhackme"`
- `nano $file`, `beef $file`
- [XOR Calculator](https://xor.pw/#) > ASCII (base 256)
- `binwalk $file`, `unzip $file`
- [stegsolve](https://www.aldeid.com/wiki/Stegsolve)
- `zbarimg $file`, https://sclouddownloader.net/
- [Wayback](https://web.archive.org/web/20200102131252/ttps://www.embeddedhacker.com/)
- [Decode](https://www.dcode.fr/vigenere-cipher) > Automatic > Key = THM
- [Dec](https://www.rapidtables.com/convert/number/decimal-to-hex.html) > [Hex](https://www.rapidtables.com/convert/number/hex-to-decimal.html) > ASCii
- wireshark > filter `http.request.method == “GET”` > Follow HTTP Stream