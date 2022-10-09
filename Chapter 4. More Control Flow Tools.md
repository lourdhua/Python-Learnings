### 1. if statements
An if statement consists of a boolean expression followed by one or more statements.
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
* There can be zero or more elif parts, and the else part is optional.
* An if … elif … elif … sequence is a substitute for the switch or case statements
* If you’re comparing the same value to several constants(switch case), or checking for specific types or attributes, you may also find the match statement useful
### 2. for Statements
* Python's for loop is used to iterate over a sequence (i.e., a list, a tuple, a dictionary, a set, or a string) - in the order that they appear in the sequence.
* This differs from the for loop functionality of other programming languges, where we use iteration step and halting condition (in C)
  ```python
  >>> # Measure some strings:
  ... words = ['cat', 'window', 'defenestrate']
  >>> for w in words:
  ...     print(w, len(w))
  ...
  cat 3
  window 6
  defenestrate 12
  ```
* Code that modifies a collection while iterating over that same collection can be tricky to get right. 
* Instead, it is usually more straight-forward to loop over a copy of the collection or to create a new collection:
  ```python
  # Create a sample collection
  users = {'Hans': 'active', 'Éléonore': 'inactive', '景太郎': 'active'}

  # Strategy:  Iterate over a copy
  for user, status in users.copy().items():
      if status == 'inactive':
          del users[user]

  # Strategy:  Create a new collection
  active_users = {}
  for user, status in users.items():
      if status == 'active':
          active_users[user] = status
  ```
  ### 3. range() function
  ```python
  >>> for i in range(5):
  ...     print(i)
  ...
  0
  1
  2
  3
  4

  >>> list(range(5, 10))
  [5, 6, 7, 8, 9]

  >>> list(range(0, 10, 3))
  [0, 3, 6, 9]

  >>> list(range(-10, -100, -30))
  [-10, -40, -70]

  >>> a = ['Mary', 'had', 'a', 'little', 'lamb']
  >>> for i in range(len(a)):
  ...     print(i, a[i])
  ...
  0 Mary
  1 had
  2 a
  3 little
  4 lamb

  >>> range(10)
  range(0, 10)

  sum(range(4))    #0+1+2+3
  6
  ```
  
