---
layout: post
category: writeups
title: "UMDCTF 2022"
date: 2022-03-07
head_ctf_categories:
  - forensics
---
# forensics

## Renzik's Case

![blue](/assets/img/UMDCTF_2022/rezinksCase.png){: .image-50 }


We are given an image of a flash drive.

I mount the image file and I don't see nothing interesting

![blue](/assets/img/UMDCTF_2022/listRezinkscase.png){: .image-50 }

But the text of the challenge give me a clue:

`My friend deleted important documents....`

The clue leads me to search for deleted files.


So I can use `foremost`, a forensic program to recover lost files (https://en.wikipedia.org/wiki/Foremost_(software):

```bash
foremost -t all -i ../Renziks_Case/usb.img 


Foremost version 1.5.7 by Jesse Kornblum, Kris Kendall, and Nick Mikus
Audit File

Foremost started at Sat Mar  5 10:37:42 2022
Invocation: foremost -t all -i ../Renziks_Case/usb.img 
Output directory: /mnt/diskCTF/ctf/umdctf2022/renziks case/usbrecover/output
Configuration file: /etc/foremost.conf

File: ../Renziks_Case/usb.img
Start: Sat Mar  5 10:37:42 2022
Length: 1 GB (2003828736 bytes)
 
Num	 Name (bs=512)	       Size	 File Offset	 Comment 

0:	00003584.jpg 	     397 KB 	    1835008
1:	00004416.jpg 	      65 KB 	    2260992
2:	00004736.jpg 	      23 KB 	    2424832
3:	00004800.gif 	       2 KB 	    2457600 	  (540 x 540)
4:	00004608.png 	      41 KB 	    2359296 	  (256 x 223)
5:	00006272.png 	     384 KB 	    3211264 	  (1024 x 561)
6:	00007104.png 	      12 KB 	    3637248 	  (240 x 240)
7:	00007616.png 	      34 KB 	    3899392 	  (1920 x 1080)
Finish: Sat Mar  5 10:38:30 2022

8 FILES EXTRACTED
	
jpg:= 3
gif:= 1
png:= 4

Foremost finished at Sat Mar  5 10:38:30 2022
```

And I can see one more image: the `flag`.


![blue](/assets/img/UMDCTF_2022/00007616.png){: .image-50 }

---UMDCTF{Sn00p1N9_L1K3_4_Sl317h!}
