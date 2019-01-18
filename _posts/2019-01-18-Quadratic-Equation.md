---
layout: article
title:  Quadratic equation python
date: 2019-01-18 19:45:00+0200
coverPhoto: https://community-cdn-digitalocean-com.global.ssl.fastly.net/assets/tutorials/images/large/python.png?1511822742
---

The standard form of a quadratic equation is:


```python
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

<button><a href="#">download</a></button>

`output is :`

```cmd
	The solution are (-2-1j) and (-2+1j)
	[Finished in 0.1s]
```