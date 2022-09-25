## Lets try some simple python commands
### 1. Numbers
- The interpreter acts as a simple calculator: you can type an expression at it and it will write the value. Expression syntax is straightforward: the operators +, -, * and / work just like in most other languages.
  ```python
  >>> 2 + 2
  4
  >>> 50 - 5*6
  20
  >>> (50 - 5*6) / 4
  5.0
  >>> 8 / 5  # division always returns a floating point number
  1.6
  ```
- The integer numbers (e.g. 2, 4, 20) have type [int](https://docs.python.org/3/library/functions.html#int), the ones with a fractional part (e.g. 5.0, 1.6) have type [float](https://docs.python.org/3/library/functions.html#float). We will see more about numeric types later in the tutorial.
- Division (/) always returns a float. To do [floor division](https://docs.python.org/3/glossary.html#term-floor-division) and get an integer result (discarding any fractional result) you can use the // operator; to calculate the remainder you can use %:
  ```python
  >>> 17 / 3  # classic division returns a float
  5.666666666666667
  >>>
  >>> 17 // 3  # floor division discards the fractional part
  5
  >>> 17 % 3  # the % operator returns the remainder of the division
  2
  >>> 5 * 3 + 2  # floored quotient * divisor + remainder
  17
  ```
- ** operator is used to calculate powers
  ```python
  >>> 5 ** 2  # 5 squared
  25
  >>> 2 ** 7  # 2 to the power of 7
  128
  ```
- There is full support for floating point; operators with mixed type operands convert the integer operand to floating point:
  ```python
  >>> 4 * 3.75 - 1
  14.0
  ```
- In addition to int and float, Python supports other types of numbers, such as Decimal and Fraction. Python also has built-in support for complex numbers, and uses the j or J suffix to indicate the imaginary part (e.g. 3+5j).

### 2. Strings
- python string manipulations
```python
>>> 'spam eggs'  # single quotes
'spam eggs'
>>> 'doesn\'t'  # use \' to escape the single quote...
"doesn't"
>>> "doesn't"  # ...or use double quotes instead
"doesn't"
>>> '"Yes," they said.'
'"Yes," they said.'
>>> "\"Yes,\" they said."
'"Yes," they said.'
>>> '"Isn\'t," they said.'
'"Isn\'t," they said.'
>>> s = 'First line.\nSecond line.'  # \n means newline
>>> s  # without print(), \n is included in the output
'First line.\nSecond line.'
>>> print(s)  # with print(), \n produces a new line
First line.
Second line.
>>> 3 * 'un' + 'ium'
'unununium'
>>> word = 'Python'
>>> word[0]  # character in position 0
'P'
>>> word[5]  # character in position 5
'n'
>>> word[-1]  # last character
'n'
>>> word[-2]  # second-last character
'o'
>>> word[-6]
'P'
>>> word[0:2]  # characters from position 0 (included) to 2 (excluded)
'Py'
>>> word[2:5]  # characters from position 2 (included) to 5 (excluded)
'tho'
>>> word[:2]   # character from the beginning to position 2 (excluded)
'Py'
>>> word[4:]   # characters from position 4 (included) to the end
'on'
>>> word[-2:]  # characters from the second-last (included) to the end
'on'
>>> word[:2] + word[2:]
'Python'
>>> word[:4] + word[4:]
'Python'
>>> word[42]  # the word only has 6 characters
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: string index out of range
>>> word[4:42]
'on'
>>> word[42:]
''
>>> word[0] = 'J'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
>>> word[2:] = 'py'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
>>> s = 'supercalifragilisticexpialidocious'
>>> len(s)
34
```
also refer: [String Methods](https://docs.python.org/3/library/stdtypes.html#string-methods)

### 3. Lists
- List can be written as a list of comma-separated values (items) between square brackets. 
- Lists might contain *items of different types*, but usually the items all have the same type.
```python
>>> squares = [1, 4, 9, 16, 25]
>>> squares
[1, 4, 9, 16, 25]
>>> squares[0]  # indexing returns the item
1
>>> squares[-1]
25
>>> squares[-3:]  # slicing returns a new list
[9, 16, 25]
>>> squares[:]
[1, 4, 9, 16, 25]
>>> squares + [36, 49, 64, 81, 100]
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> cubes = [1, 8, 27, 65, 125]  # something's wrong here
>>> 4 ** 3  # the cube of 4 is 64, not 65!
64
>>> cubes[3] = 64  # replace the wrong value
>>> cubes
[1, 8, 27, 64, 125]
>>> cubes.append(216)  # add the cube of 6
>>> cubes.append(7 ** 3)  # and the cube of 7
>>> cubes
[1, 8, 27, 64, 125, 216, 343]
>>> letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
>>> letters
['a', 'b', 'c', 'd', 'e', 'f', 'g']
>>> # replace some values
>>> letters[2:5] = ['C', 'D', 'E']
>>> letters
['a', 'b', 'C', 'D', 'E', 'f', 'g']
>>> # now remove them
>>> letters[2:5] = []
>>> letters
['a', 'b', 'f', 'g']
>>> # clear the list by replacing all the elements with an empty list
>>> letters[:] = []
>>> letters
[]
>>> a = ['a', 'b', 'c']
>>> n = [1, 2, 3]
>>> x = [a, n]
>>> x
[['a', 'b', 'c'], [1, 2, 3]]
>>> x[0]
['a', 'b', 'c']
>>> x[0][1]
'b'

#3d matrix
>>> r1 = [1,4,7]
>>> r2 = [9,43,87]
>>> r3 = [99,55,97]
>>> m1 = [r1,r2,r3]
>>> m2 = [r1+r2+r3]
m1
m2
m2[0]
m2[0:2]
m2[1:2]

[[1, 4, 7], [9, 43, 87], [99, 55, 97]]
[[1, 4, 7, 9, 43, 87, 99, 55, 97]]
[1, 4, 7, 9, 43, 87, 99, 55, 97]
[[1, 4, 7, 9, 43, 87, 99, 55, 97]]
[]
```

#### Lets start with - Fibonacci Series
```python
>>> # Fibonacci series:
... # the sum of two elements defines the next
... a, b = 0, 1
>>> while a < 10:
...     print(a)
...     a, b = b, a+b
...
0
1
1
2
3
5
8
```






