---
layout: article
title: "Python Permutations"
date: 2018-01-13 19:45:00+0200
coverPhoto: https://github.com/boubli/Youssef-Boubli/blob/gh-pages/contents/images/2019/01/Opencv-python.png?raw=true
---

This simply how to implement the module of permutations in python.

{% highlight ruby %}
>>> from itertools import permutations
>>> perms = [''.join(p)+"@gmail.com" for p in permutations('abc', 3)]
>>> for x in range(0, len(perms)):
...     print (perms[x])
... 
abc@gmail.com
acb@gmail.com
bac@gmail.com
bca@gmail.com
cab@gmail.com
cba@gmail.com
>>> 
{% endhighlight %}