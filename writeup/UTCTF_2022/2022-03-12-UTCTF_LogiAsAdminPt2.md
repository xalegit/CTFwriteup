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

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt2_a.png)


We are given a script file.

The Web page ask for a Username and a Password:

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt2_b.png)

but the login button is disabled.

I open the script and I see username, password

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt2_c.png)


So I open the web page with my browser and go to Web Developer Tools: under the section Inspector I can see the login button disable, so
I enable it

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt2_d.png)

and so the login button is enabled

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt1_e.png)

After entering the username and the password on the web page I can see the the flag: `u{*re@lly*gott@_upd8_th@t_pwd}` 



