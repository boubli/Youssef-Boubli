
---
layout: article
title: "Reverse Bit [CF]"
date: 2018-01-13 19:45:00+0200
coverPhoto: https://www.w3resource.com/w3r_images/python-19-reverse-the-digits-of-an-integer-unsigned.png
---

Author Question: **Giappi**

I have an integer number, which I want to reverse by following steps:

1. Convert the number into binary string.
2. Reverse binary string.
3. Convert the reversed binary string back to integer.

Can you help me write a function to do it ?

**Example**

For `x = 234`, the output should be `ReverseBit(x) = 87`.

`23410 = 111010102 => 010101112 = 8710`.

**Input/Output**

* **[input] integer x**
  A non-negative integer.

* **[output] integer**
  x reversed as described above.

**Solution:**

```python
def ReverseBit(x):
  x = bin(x).replace('0b', '')
  reverse_text = ''
  for l in range(len(x)-1, -1, -1):
      reverse_text = reverse_text + x[l]
  return int(reverse_text, 2)

>>> ReverseBit(234)
87
>>>
```