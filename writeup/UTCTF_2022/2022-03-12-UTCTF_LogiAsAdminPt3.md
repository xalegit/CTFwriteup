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

![blue](/assets/img/UTCTF_2022/loginasadmin_pt3_a.png){: .image-50 }


We are given a script file.

The Web page ask for a Username and a Password:

![blue](/assets/img/UTCTF_2022/loginasadmin_pt1_b.png){: .image-50 }


I open the script and I can see username and password:

![blue](/assets/img/UTCTF_2022/loginasadmin_pt1_c.png){: .image-50 }

so I can use them! 
But after entering the username and the password on the web page I get a: 
`Bad Request`
`The browser (or proxy) sent a request that this server could not understand.`

So I open again the script and see that's another variable in the form:
`request.form['isAdmin'] == "True"`

Then I use Zap and send an HTTP POST after setting the parameter isAdmin to True
![blue](/assets/img/UTCTF_2022/loginasadmin_pt1_d.png){: .image-50 }

and now I can see the Flag: `utflag{omg_why_not_upd8_pwd!?!}`
