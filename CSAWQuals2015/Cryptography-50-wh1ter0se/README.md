---
layout: post
title:  "CSAW - wh1ter0se"
date:   2015-09-20 22:00
categories: csaw2015
tags: security ctf csaw2015 cryptography
description: Cryptography challenge for 50 points
---

**Category** : Cryptography 

**Points** : 50

**Note**: The flag is the entire thing decrypted.

***

#Write-up
When we opened the challenge we had this [file]({{ site.url }}/files/CSAW2015/crypto50-wh1ter0se/eps1.7_wh1ter0se_2b007cf0ba9881d954e85eb475d0d5e4.m4v) to download.

I found that it was not a real .m4v file... When we opened it with notepad we could see this cryptogram : 

> EOY XF, AY VMU M UKFNY TOY YF UFWHYKAXZ EAZZHN. UFWHYKAXZ ZNMXPHN. UFWHYKAXZ EHMOYACOI. VH'JH EHHX CFTOUHP FX KMY'U AX CNFXY FC OU. EOY VH KMJHX'Y EHHX IFFQAXZ MY VKMY'U MEFJH OU.

I knew a useful cryptogram solver that I use online : [rumkin cryptogram solver](http://rumkin.com/tools/cipher/cryptogram-solver.php)

And I received this result :

> BUT NO IT WAS A SHORT CUT TO SOMETHING BIGGER SOMETHING GRANDER SOMETHING BEAUTIFUL WE'VE BEEN FOCUSED ON WHAT'S IN FRONT OF US BUT WE HAVEN'T BEEN LOOKING AT WHAT'S ABOVE US- BUT NO IT WAS A SHORT CUT TO SOMETHING BIGGER SOMETHING GRANDER SOMETHING BEAUTIFUL WE'VE BEEN FOCUSED ON WHAT'S IN FRONT OF US BUT WE HAVEN'T BEEN LOOPING AT WHAT'S ABOVE US


I searched a little bit on google in order to find the right sentence and it seems that it's some lyrics from an episode of Mr. Robot. And, the right sentence was :

###The flag 

> But no, it was a short cut to something bigger. Something grander. Something beautiful. We've been focused on what's in front of us. But we haven't been looking at what's above us.

