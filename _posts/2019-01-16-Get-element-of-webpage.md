---
layout: article
title: "How to get data from inspect element of a webpage using Python"
date: 2019-01-15 20:45:00+0200
coverPhoto: https://cdn-images-1.medium.com/max/1600/1*WHf2-YddJQ1wdBGOvAo8Gw.gif
---

# Question :
```Text
I'd like to get the data from inspect element using Python. I'm able to download
the source code using BeautifulSoup but now I need the text from inspect element 
of a webpage. I'd truly appreciate if you could advise me how to do it.
Edit: By inspect element I mean, in google chrome, right click gives us an option
called inspect element which has code related to each element of that particular page.
I'd like to extract that code/ just its text strings.
```
<script type="text/javascript">
    google_ad_client = "ca-pub-5692999531908344";
    google_ad_slot = "7496712842";
    google_ad_width = 970;
    google_ad_height = 250;
</script>
<!-- Git -->
<script type="text/javascript"
src="//pagead2.googlesyndication.com/pagead/show_ads.js">
</script>

If you want to automatically fetch a web page from Python in a way that runs Javascript, you should look into Selenium. It can automatically drive a web browser (even a headless web browser such as PhantomJS, so you don't have to have a window open).

In order to get the HTML, you'll need to evaluate some javascript. Simple sample code, alter to suit:

```python
	from selenium import webdriver

	driver = webdriver.PhantomJS()
	driver.get("http://google.com")

	# This will get the initial html - before javascript
	html1 = driver.page_source

	# This will get the html after on-load javascript
	html2 = driver.execute_script("return document.documentElement.innerHTML;")
```

`Note 1:` If you want a specific element or elements, you actually have a couple of options -- parse the HTML in Python, or write more specific JavaScript that returns what you want.

`Note 2:` if you actually need specific information from Chrome's tools that is not just dynamically generated HTML, you'll need a way to hook into Chrome itself. No way around that.

