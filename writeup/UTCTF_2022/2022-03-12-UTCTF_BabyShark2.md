---
layout: post
category: writeups
title: "UTCTF 2022"
date: 2022-03-07
head_ctf_categories:
  - beginner
---
# beginner

## Baby Shark 2

![img_name](/assets/img/UTCTF_2022/babyshark2.png){: .image-50 }


We are given a pcap file.

I open it with Wireshark. The text of the challenge give me a clue:

`I was able to capture some ftp traffic in this pcap. I wonder if there is any good info here.`

The clue leads me to search for FTP Traffic.

![img_name](/assets/img/UTCTF_2022/wireshark_babyshark2_a.png){: .image-50 }

I see a FTP Packet `Request: PASS utflag{sharkbait_hoo_ha_ha}`

![img_name](/assets/img/UTCTF_2022/wireshark_babyshark2_b.png){: .image-50 }

So the flag is  `utflag{sharkbait_hoo_ha_ha}`
