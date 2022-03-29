---
layout: post
category: writeups
title: "UTCTF 2022"
date: 2022-03-07
head_ctf_categories:
  - beginner
---
# beginner

## Baby Shark

![blue](/assets/img/UTCTF_2022/babyshark.png){: .image-50 }


We are given a pcap file.

I open it with Wireshark. The text of the challenge give me a clue:

`I think someone downloaded something from an http site.`

The clue leads me to search for HTTP Traffic.

![blue](/assets/img/UTCTF_2022/wireshark_babyshark_a.png){: .image-50 }

I see a GET Request of flag.png

So I can go to `File -> Export Objects -> HTTP`

![blue](/assets/img/UTCTF_2022/wireshark_babyshark_b.png){: .image-50 }

and save the file flag.png:

![blue](/assets/img/UTCTF_2022/wireshark_babyshark_c.png){: .image-50 }
