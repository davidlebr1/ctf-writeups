---
layout: post
title:  "PoliCTF - John In The Middle"
date:   2015-07-13 22:30
categories: polictf2015
tags: security ctf polictf2015 forensic
description: Forensic challenge for 100 points
---
**Category** : Forensic 

**Points** : 100

#Write-up
First, we had to download the [pcap file]({{ site.url }}/files/PoliCTF2015/John-In-The-Middle/john-in-the-middle.pcap) with the following message *Can John hijack your surfin'? :)*We know that a pcap file is an extracted file from Wireshark. So, we needed to analyze the network packets.

My first reflex with Wireshark is to verify if I can extract files that are transferred between the client and the server in the pcap file.

The extracted files were the whole [polictf.it](http://polictf.it) website with one exception, the logo was different.

So, I used [Stegsolve](http://www.caesum.com/handbook/Stegsolve.jar) to analyze the image.

Finally, the flag was in the image.

The image logo.png with the flag hidden:

![logo](https://cloud.githubusercontent.com/assets/838845/20353937/7c2d31d8-abea-11e6-8178-56a8c1da777c.png)

The image with the flag:

![flag](https://cloud.githubusercontent.com/assets/838845/20353940/7f1e5c50-abea-11e6-8b1a-eb4464898310.png)

flag{J0hn_th3_Sn1ff3r}


