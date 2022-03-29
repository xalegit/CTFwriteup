---
layout: post
category: writeups
title: "UTCTF 2022"
date: 2022-03-07
head_ctf_categories:
  - beginner
---
# beginner

## Login as Admin Pt 2

![blue](/assets/img/UTCTF_2022/loginasadmin_pt1_a.png){: .image-50 }


We are given a script file.

The Web page ask for a Username and a Password:

![blue](/assets/img/UTCTF_2022/loginasadmin_pt1_b.png){: .image-50 }

but the login button is disabled

I open the script and I see username, password

![blue](/assets/img/UTCTF_2022/loginasadmin_pt1_c.png){: .image-50 }


So I open the web page with my browser and go to Web Developer Tools under the section Inspector I can see the login button disable, so
I enable it

![blue](/assets/img/UTCTF_2022/loginasadmin_pt1_d.png){: .image-50 }

and so the login button is enabled

![blue](/assets/img/UTCTF_2022/loginasadmin_pt1_e.png){: .image-50 }

After entering the username and the password on the web page I can see the the flag: `u{*re@lly*gott@_upd8_th@t_pwd}` 


