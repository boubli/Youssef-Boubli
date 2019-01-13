
---
layout: article
title: "Remove all files .pyc with recrusive method"
date: 2018-01-13 19:45:00+0200
coverPhoto: https://github.com/boubli/Youssef-Boubli/blob/gh-pages/contents/images/2019/01/Opencv-python.png?raw=true
---



This method simple but important. Example in your project dir is like this:

{% highlight ruby %}
project_dir/
           __init__.py
           __init__.pyc
           something.py
           something.pyc
           ...
           core/
               __init__.py
               __init__.pyc
               build.py
               build.pyc
{% endhighlight %}

Deleting the `.pyc` files one by one would be spending a lot of time. and you will be bored. There is sample how to handle it.

```
$ find your_dir -name *.pyc -delete
```

OR, if you work inside current directory.

```
$ find . -name *.pyc -delete
```