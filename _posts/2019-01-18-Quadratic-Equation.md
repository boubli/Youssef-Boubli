---
layout: article
title:  Quadratic equation python
date: 2019-01-18 19:45:00+0200
coverPhoto: https://community-cdn-digitalocean-com.global.ssl.fastly.net/assets/tutorials/images/large/python.png?1511822742
---

The standard form of a quadratic equation is:


```text
	ax2 + bx + c = 0, where
	a, b and c are real numbers and
	a ≠ 0
```
# Source Code

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

<style type="text/css">
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

	.btn {
	  background-color: DodgerBlue;
	  border: none;
	  color: white;
	  padding: 12px 30px;
	  cursor: pointer;
	  font-size: 20px;
	}

	/* Darker background on mouse-over */
	.btn:hover {
	  background-color: RoyalBlue;
	}
</style>

Download source code : 
<button class="btn"><i class="fa fa-download"></i><a href="#">Download</a></button>

`output is :`

```text
	The solution are (-2-1j) and (-2+1j)
	[Finished in 0.1s]
```