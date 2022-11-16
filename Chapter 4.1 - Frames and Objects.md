### 1. Global Frames
In programming language you have something called **Stack**; In python when you call a function, you create something called a *stack frame*.
This frame is just a table with list of all the variables local to your function.
Note: Defining a function doesnt create a stack, its the calling of the function that create it.
* one-line if clause:
  ```python
  var = 100
  if ( var == 100 ) : print "Value of expression is 100"
  print "Good bye!"
  ```
  ```python
  >>> x = int(input("Please enter an integer: "))
  Please enter an integer: 42
  >>> if x < 0:
  ...     x = 0
  ...     print('Negative changed to zero')
  ... elif x == 0:
  ...     print('Zero')
  ... elif x == 1:
  ...     print('Single')
  ... else:
  ...     print('More')
  ...
  More
  ```
* [pytutor](https://pythontutor.com/render.html#mode=display)
