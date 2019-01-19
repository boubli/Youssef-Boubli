---
layout: article
title:  Quadratic equation python
date: 2019-01-18 19:45:00+0200
coverPhoto: http://programaenlinea.net/wp-content/uploads/2018/03/python-Webinar.jpg
---

The standard form of a quadratic equation is:


```text
	ax2 + bx + c = 0, where
	a, b and c are real numbers and
	a ≠ 0
```
# Source Code
Download source code [Here](https://raw.githubusercontent.com/boubli/Youssef-Boubli/gh-pages/source%20code/Quadratic%20Equation.py)

```python
	# Solve the quadratic equation < ax**2 + bx + c = 0 >

	# import complex math module
	import cmath

	a = 1
	b = 4
	c = 5

	# To take coefficient input from the users
	#a = float(input('Enter a: ')) 
	#b = float(input('Enter b: ')) 
	#c = float(input('Enter c: ')) 

	# calculate the discriminant
	d = (b**2) - (4*a*c)

	# find two solutions
	sol1 = (-b-cmath.sqrt(d))/(2*a)
	sol2 = (-b+cmath.sqrt(d))/(2*a)

	print('The solution are {0} and {1}'.format(sol1,sol2))
```


`output is :`

```text
	The solution are (-2-1j) and (-2+1j)
	[Finished in 0.1s]
```


<style type="text/css">
	/* This widget was published by AllBloggerTricks.com */

.abt-author_info{
float:left;
width:550px;
padding:15px;
border:1px solid #ccc;
margin-bottom:15px;
margin-top:15px;
background:#eee;color:#000;
}
.abt-author_info:hover{
background:#eee;
border:1px solid #ccc;
-webkit-box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
-moz-box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
}
.abt-author_info h3{
color:#000;
margin-bottom:10px;
}
.abt-author_info h3:hover{
border : 1px solid #EEEEEE;
-webkit-box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
-moz-box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
}
.abt-author_photo{
float:right;
margin:0 0 0 10px;
}
.abt-author_photo img{
border:1px solid #666;
-webkit-transition:-webkit-transform .15s linear;
-moz-transition:-moz-transform .15s linear;
-o-transition:-o-transform .15s linear;transition:transform .15s linear;
-webkit-box-shadow:0 3px 6px rgba(0,0,0,.25);
-moz-box-shadow:0 3px 6px rgba(0,0,0,.25);
box-shadow:0 3px 6px rgba(0,0,0,.25);
padding:5px 5px 5px 5px;-webkit-transform:rotate(+2deg);
-moz-transform:rotate(+2deg);-ms-transform:rotate(+2deg);
-o-transform:rotate(+2deg);transform:rotate(+2deg);float:left;
}
.abt-author_photo img:hover{
background:#FFFFFF;
border : 1px solid #EEEEEE;
-webkit-box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
-moz-box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
box-shadow:0px 0px 10px  rgba(0, 0, 0, .3);
-webkit-transform:rotate(-1deg);
-moz-transform:rotate(-1deg);
-ms-transform:rotate(-1deg);
-o-transform:rotate(-1deg);
transform:rotate(-1deg);
}
ul.abt-social{
list-style:none;
margin:10px;
overflow:hidden;
}
.abt-social li{
float:right;
background:none !important;
padding:0 !important;
margin:0 8px;
}
.abt-social li a{
display:block;
width:40px;
height:40px;
background:url("https://2.bp.blogspot.com/-IMM_B7aaLQA/T7ObAft4GbI/AAAAAAAADN0/mT6xK72Xe9I/s1600/social.png") no-repeat transparent;
text-indent:-99999em !important;
}
.abt-social li a:hover{
padding:0 !important;
}
.abt-social li.rssicon a{
background-position:0 0;
}
.abt-social li.twicon a{
background-position:-50px 0;
}
.abt-social li.fbicon a{
background-position:-100px 0;
}
.abt-social li.gicon a{
background-position:-150px 0;
}
.abt-social li.rssicon a:hover{
background-position:0 -50px;
}
.abt-social li.twicon a:hover{
background-position:-50px -50px;
}
.abt-social li.fbicon a:hover{
background-position:-100px -50px;
}
.abt-social li.gicon a:hover{
background-position:-150px -50px;
}
.abt-linediv{
margin-top:25px;
height:0px;
clear:both;
display:block;
border-top:1px solid #fefefe;
border-bottom:1px solid #CCCCCC;
}
.abt-emailbutton{
background:#f7f8f9;
background:-webkit-gradient(linear,left top,left bottom,color-stop(#f7f8f9,0),color-stop(#e9e9e9,1));
background:-webkit-linear-gradient(top, #f7f8f9 0%, #e9e9e9 100%);
background:-moz-linear-gradient(top, #f7f8f9 0%, #e9e9e9 100%);
background:-o-linear-gradient(top, #f7f8f9 0%, #e9e9e9 100%);
background:linear-gradient(top, #f7f8f9 0%, #e9e9e9 100%);
filter:progid:DXImageTransform.Microsoft.gradient( startColorstr='#f7f8f9', endColorstr='#e9e9e9',GradientType=0 );
border:1px solid #ddd;
-webkit-border-radius:4px;
-moz-border-radius:4px;
border-radius:4px;
padding:6px 12px;
margin:0;-webkit-box-shadow:0 1px 0 #f9f9f9 inset, 1px 1px 1px rgba(223,223,223,0.4);
-moz-box-shadow:0 1px 0 #f9f9f9 inset, 1px 1px 1px rgba(223,223,223,0.4);box-shadow:0 1px 0 #f9f9f9 inset, 1px 1px 1px rgba(223,223,223,0.4);
color:#888;
text-shadow:0 1px 0 #fff;
line-height:1.2;
cursor:pointer;
font-size:13px;
}
.abt-emailbutton:hover{
background:#f1f1f1;
background:-webkit-gradient(linear,left top,left bottom,color-stop(#f1f1f1,0),color-stop(#e0e0e0,1));
background:-webkit-linear-gradient(top, #f1f1f1 0%, #e0e0e0 100%);
background:-moz-linear-gradient(top, #f1f1f1 0%, #e0e0e0 100%);
background:-o-linear-gradient(top, #f1f1f1 0%, #e0e0e0 100%);
background:linear-gradient(top, #f1f1f1 0%, #e0e0e0 100%);filter:progid:DXImageTransform.Microsoft.gradient( startColorstr='#f1f1f1', endColorstr='#e0e0e0',GradientType=0 );
text-decoration:none !important;
}
.abt-email{
clear:both;
width:250px;
margin:10px 0;
float:left;
}
.abt-emailform{
position:relative;
width:250px;
margin:0 auto;
}
.abt-emailinput{
width:200px;
height:18px;
margin:0 auto;
padding:8px 40px 8px 10px;border:1px solid #ddd;
-webkit-border-radius:4px;-moz-border-radius:4px;
border-radius:4px;font-family:georgia;
font-style:italic;
-webkit-box-shadow:1px 1px 2px #dfdfdf;
-moz-box-shadow:1px 1px 2px #dfdfdf;
box-shadow:1px 1px 2px #dfdfdf;
font-size:14px;color:#666;
}
.abt-emailbutton{
-webkit-border-top-right-radius:4px;
-webkit-border-bottom-right-radius:4px;
-moz-border-radius-topright:4px;
-moz-border-radius-bottomright:4px;
border-top-right-radius:4px;
border-bottom-right-radius:4px;
-webkit-border-top-left-radius:0px;
-webkit-border-bottom-left-radius:0px;
-moz-border-radius-topleft:0px;
-moz-border-radius-bottomleft:0px;
border-top-left-radius:0px;border-bottom-left-radius:0px;
padding:9px;
position:absolute;
right:-2px;
top:0;
display:block;
line-height:16px;
}
.abt-emailbutton{
padding:8px !important;
}
.abt-emailform, .abt-emailinput{
width:98% !important;
-webkit-box-sizing:border-box;
-moz-box-sizing:border-box;
box-sizing:border-box;
height:auto;
}

/* This widget was published by AllBloggerTricks.com */
</style>

<div class='abt-author_info'>
<div class='abt-author_photo'>
<img alt='author' height='150' src='https://avatars0.githubusercontent.com/u/26576840?s=460&v=4' width='90'/>
</div>
<h2 style='color:#444;font-family:verdana;text-shadow: 3px 3px 3px 3px #ABABAB;'>This Post Was Written By :</h2>
<p>Youssef Boubli.</p>
<div class='abt-linediv'/>
<div class='abt-email'>
<small style='text-align:center;'>Get Free Email Updates to your Inbox!</small>
<form action='https://feedburner.google.com/fb/a/mailverify' class='abt-emailform' method='post' onsubmit='window.open(&apos;https://feedburner.google.com/fb/a/mailverify?uri=FeedUsername&apos;, &apos;popupwindow&apos;, &apos;scrollbars=yes,width=550,height=520&apos;);return true' target='popupwindow'>
<input name='uri' type='hidden' value='FeedUsername'/>
<input name='loc' type='hidden' value='en_US'/>
<input class='abt-emailinput' name='email' onblur='if (this.value == &quot;&quot;) {this.value = &quot;Enter your email...&quot;;}' onfocus='if (this.value == &quot;Enter your email...&quot;) {this.value = &quot;&quot;}' type='text' value='Enter your email...'/>
 <input class='abt-emailbutton' title='' type='submit' value='SignUp'/>
</form>
</div>
<ul class='abt-social'>
<li class='rssicon'>
<a href='http://feeds.feedburner.com/'>Rss</a>
</li><li class='twicon'>
<a href='https://twitter.com/youssf_vlog'>Twitter</a>
</li><li class='fbicon'>
<a href='https://facebook.com/boubli.programmer'>Facebook</a>
</li><li class='gicon'>
<a href='https://plus.google.com/'>Google +</a>
</li>
</ul>
</div>