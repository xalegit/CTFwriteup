---
layout: post
category: writeups
title: "UTCTF 2022"
date: 2022-03-07
head_ctf_categories:
  - beginner
---
# beginner

## Login as Admin Pt 3

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt3_a.png)


We are given a script file.

The Web page ask for a Username and a Password:

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt3_b.png)


I open the script and I can see username and password:

![img_name](/assets/img/UTCTF_2022/loginasadmin_pt1_c.png)

so I can use them! 
But after entering the username and the password on the web page I get a: 
`Bad Request`
`The browser (or proxy) sent a request that this server could not understand.`

So I open again the script and see that's another variable in the form:
`request.form['isAdmin'] == "True"`

Then I use Zap and send an HTTP POST after setting the parameter isAdmin to True
![img_name](/assets/img/UTCTF_2022/loginasadmin_pt3_d.png)

and now I can see the Flag: `utflag{omg_why_not_upd8_pwd!?!}`

