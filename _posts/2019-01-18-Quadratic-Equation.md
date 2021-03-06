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