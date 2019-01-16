---
layout: article
title: "Get Elements by ID, Tag, Name, Class, CSS Selector"
date: 2019-01-16 10:45:00+0200
coverPhoto: https://i.ytimg.com/vi/pfiAD405Fqk/maxresdefault.jpg
---

Get Element by Matching the Value of the 「id」 Attribute

`document.getElementById(id_string)`
Return a (none-live) element object. Returns null if not found.

```JavaScript
	const elem = document .getElementById("xyz");

	elem.style.color="red"; // change color to red
```
Note: element id must be unique per HTML file. (embeded iframe counts as different HTML file.)

# Get Elements by Tag Name
document.getElementsByTagName(tag_name)
Return a live HTMLCollection.

The tag_name is `"div"`, `"span"`, `"p"`, etc.

```JavaScript
	const list = document .getElementsByTagName("p"); // get all p elements

	list.length; // show number of items

	list[0].style.color = "red"; // make the first one red
```

# Get Elements by Matching the Value of the 「class」 Attribute
document.getElementsByClassName("class_values")

Return a live HTMLCollection.
The class_values can be multiple classes separated by space. For example: "aa bb", and it'll get elements, where each element is in both class “aa” and “bb”.

```JavaScript
	// get element of class abc

	const list = document .getElementsByClassName("abc");

	list[0].style.color = "red"; // make the first one red
```

Note: a HTML element can belong to more than one class. Here's a example:

```HTML
	<p class="aa">1</p>

	<p class="bb">2</p>

	<p class="bb aa">3</p>

	<p class="bb cc aa">4</p>

	<script>document.getElementsByClassName("aa bb");</script>

	<!-- it'll get 3 and 4. -->
```

# Get Elements by Matching the Value of the 「name」 Attribute
document.getElementsByName("name_value")

Return a live HTMLCollection, of all elements that have the name="name_value" attribute and value pair.

Here's a sample HTML:

```HTML
	<p name="abc">1</p>
	<div class="zz" name="xyz">2</div>
	<div class="zz" name="xyz">3</div>

	<form>
	<input name="xyz" type="text" size="20">
	</form>
```

Here's JavaScript code that makes the first element with name="xyz" red.

```JavaScript
	// get element by value of the “name” attribute

	const xyz = document .getElementsByName("xyz");

	xyz[0].style.color="red"; // make the first one red
```
# Get Elements using CSS Selector Syntax
document.querySelector(css_selector)

Return a non-live HTMLCollection of the first element that match the CSS selector css_selector. The css_selector is a string of CSS syntax, and can be several selectors separated by comma.

document.querySelectorAll(css_selector)

Return a non-live HTMLCollection, of elements that match the CSS selector css_selector. The css_selector is a string of CSS syntax, and can be several selectors separated by comma.

```JavaScipt
	const xx = document .querySelectorAll("span.a, span.c");

	for (const i = 0; i < xx.length; i++) {
	    xx[i].style.color="red";
	}
``


