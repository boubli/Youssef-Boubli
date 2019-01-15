---
layout: article
title: Variables and value
date: 2019-01-15 19:45:00+0200
coverPhoto: https://ilearnthis.com/wp-content/uploads/2018/09/Variables-python.png
---
# Lesson 2 Variables and Values Variables and Values
Before you begin the second lesson you need to [read Python Lesson Index](http://www.google.com)

# Variables
Are the names of their values can change the length of the implementation of the program it does not take a fixed value, but we can change it whenever we want in Python language can choose the names of variables in all letters and even numbers, but the first variable must be a letter, not a number.
```python
	>>> 3x = ‘Python 3 Boubli’
```
The variable starts with a number that is wrong and correct is :
```python
	>>> X3 = ‘Python 3 Boubli’
```

 *Also, we can not use special characters to name variables such as # @ / $.
 *Also, you can not name variables with reserved names in the following list:
```terminal
and  

assert

break

class

continue

def

del

elif

else

except

exec

finally

for

from

global

if

import

in

is

lambda

not

or

pass

print

raise

return

try

while

yield
```

# Values
Is the information that we enter or assign to variables in the program so that we can save them in the memory of the device.

# Examples
An example is to assign a text value to a variable and then print that value

```python
	>>> X = ‘Python 3 Boubli’

	>>> Print x
```
`outout is :`

```python
	Python 3 Boubli
```
Note When you assign a text value to the variable, we use the quotation mark with the value.
An example is to base a numeric value on a variable and then print this value

```python
	>>> X = 1200

	>>> Print x
```
`outout is :`

```python
	1200
```

Note When assigning numeric values to a variable, we do not need to use the quotation mark with the value.
Example of assigning more than a textual and numerical value to more than one variable and printing the numerical results next to the text :


```python
	>>> a = ‘I’

	>>> b = ‘am’

	>>> c = 10

	>>> d = 12

	>>> e = ‘years’

	>>> f = ‘old’

	>>> print a ,b , c + d ,e , f

```

`output is :`

```python
	I am 22 years old
```

Note that a numerical and text output result can be printed with one print command on a single line.
Example of assigning one value to more than one variable on the same line and printing variable values

```python
	>>> x = y = 10

	>>> print x
```

`output is :`

```python
	8

	>>> print y
```
Note You can assign one value to more than one variable on a single line.
Example of assigning more than one variable value to one line and printing values of variables
```python
	>>> a , b = 10 , 15

	>>> print a
```


`output is :`

```python
	15
```

Note that more than one value can be assigned to a variable on the same line.
Same as the previous example, but this example computes the age :

```python
	>>> Birthyear , ThisYear = 1988 , 2009

	>>> Age = ThisYear – Birthyear

	>>> print ‘your age is:’ , Age
```

`output is :`

```python
	Your age is : 21
```

Thus, we may know the Variables and Values in Python.
Our next lesson will be about (if) and how to use it.