---
layout: post
category: writeups
title: "UTCTF 2022"
date: 2022-03-07
head_ctf_categories:
  - beginner
---
# beginner

## Login as Admin Pt 1

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt1_a.png){: .image-50 }


We are given a script file.
![img_name](/assets/img/UTCTF_2022/loginasadmin_pt1_b.png){: .image-50 }

The Web page ask for a Username and a Password:

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt1_c.png){: .image-50 }


I open the script and I see username, password and another variable: `cookie`

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt1_d.png){: .image-50 }


So I open the web page with my browser and go to Web Developer Tools and under the section Cookie I can see


![img_name](/assets/img/UTCTF_2022/loginasadmin_pt1_e.png){: .image-50 }

So I set the cookie isAdmin to True and opening again the web page I can see the flag: `utflag{t1m3_2_upd8_th@t_l@me_pwd}` 



