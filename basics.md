# Python Basics Cheat Sheet

## Operators

- **Arithmetic:** `+`, `-`, `*`, `/`, `//`, `%`, `**`
  ```python
  print(2 + 3, 2 - 3, 2 * 3, 5 / 2, 5 // 2, 5 % 2, 2 ** 3)  # 5 -1 6 2.5 2 1 8
  ```
- **Comparison:** `==`, `!=`, `<`, `>`, `<=`, `>=`
  ```python
  print(2 == 2, 2 != 3, 2 < 3, 2 > 1, 2 <= 2, 3 >= 2)  # True True True True True True
  ```
- **Logical:** `and`, `or`, `not`
  ```python
  x, y = 5, 10
  print(x > 0 and y > 0)  # True
  print(x > 0 or y < 0)   # True
  print(not(x > 0))       # False
  ```
- **Identity:** `is`, `is not`
  ```python
  a = [1, 2]; b = a
  print(a is b)  # True
  print(a is not b)  # False
  ```
- **Membership:** `in`, `not in`
  ```python
  print(3 in [1, 2, 3])      # True
  print(4 not in [1, 2, 3])  # True
  ```
- **Bitwise:** `&`, `|`, `^`, `~`, `<<`, `>>`
  ```python
  print(2 << 2)  # 8 (2*2^2)
  print(8 >> 2)  # 2 (8/2^2)
  ```

## Control Structures

- **if-elif-else:**
  ```python
  num = 10
  if num > 0:
      print("Positive")
  elif num == 0:
      print("Zero")
  else:
      print("Negative")
  ```
- **while loop:**
  ```python
  i = 0
  while i < 3:
      print(i)
      i += 1
  ```
- **for loop with range():**
  ```python
  for i in range(1, 6):
      print(i)
  # Output: 1 2 3 4 5
  # range(start, stop, step) generates numbers from start to stop-1
  ```
- **break and continue:**
  ```python
  for i in range(1, 6):
      if i == 3:
          break
      print(i)  # Output: 1 2
  for i in range(1, 6):
      if i == 3:
          continue
      print(i)  # Output: 1 2 4 5
  ```

## Input and Output

- **input():**
  ```python
  name = input("Enter your name: ")
  print("Hello,", name)
  ```

## Functions

- **Defining and calling:**
  ```python
  def add(a, b):
      return a + b
  print(add(2, 3))
  ```
- **Default arguments:**
  ```python
  def greet(name="World"):
      print("Hello,", name)
  greet()         # Hello, World
  greet("Alice")  # Hello, Alice
  ```
- **Variable-length arguments:**
  ```python
  def show(*args):
      for item in args:
          print(item)
  show(1, 2, 3)
  ```
- **Lambda (anonymous) functions:**
  ```python
  square = lambda x: x * x
  print(square(5))
  ```
- **Recursion:**
  ```python
  def factorial(n):
      if n == 0:
          return 1
      else:
          return n * factorial(n-1)
  print(factorial(5))
  ```

## Data Types and Structures

- **List:**
  ```python
  lst = [1, 2, 3]
  lst.append(4)
  lst.insert(1, 5)
  lst.remove(5)
  print(lst[0], lst[-1])
  print(lst.count(2), lst.index(3))
  lst2 = lst[:]
  lst3 = lst.copy()
  ```
- **List comprehension:**
  ```python
  squares = [x**2 for x in range(5)]
  odds = [x for x in range(10) if x % 2 != 0]
  ```
- **Tuple:**
  ```python
  t = (1, 2, 3)
  print(t[0])
  # t[0] = 5  # Error: tuples are immutable
  ```
- **Set:**
  ```python
  s = {1, 2, 3}
  s.add(4)
  s.remove(2)
  print(3 in s)
  # Set operations
  a = {1, 2, 3}; b = {3, 4, 5}
  print(a | b)  # Union
  print(a & b)  # Intersection
  print(a - b)  # Difference
  print(a.issubset(b), a.issuperset(b))
  ```
- **Dictionary:**
  ```python
  d = {'a': 1, 'b': 2}
  d['c'] = 3
  d['a'] = 10
  del d['b']
  print(list(d.keys()), list(d.values()))
  ```

## Useful Built-in Functions

- **enumerate():**
  ```python
  for idx, val in enumerate(['a', 'b', 'c']):
      print(idx, val)
  ```
- **zip():**
  ```python
  a = [1, 2, 3]
  b = ['x', 'y', 'z']
  for x, y in zip(a, b):
      print(x, y)
  ```
- **filter(), map(), reduce():**
  ```python
  lst = [1, 2, 3, 4]
  print(list(filter(lambda x: x % 2 == 0, lst)))  # [2, 4]
  print(list(map(lambda x: x**2, lst)))           # [1, 4, 9, 16]
  from functools import reduce
  print(reduce(lambda x, y: x * y, lst))          # 24
  ```

## Strings

- **Slicing and reversing:**
  ```python
  s = "hello"
  print(s[1:4])   # ell
  print(s[::-1])  # olleh
  ```
- **Common string methods:**
  ```python
  s = "abc123"
  print(s.isalnum())
  print(s.upper())
  print(s.lower())
  print(s.startswith("ab"))
  print(s.endswith("23"))
  ```

## Classes and Objects (Basics)

- **Class definition and object creation:**
  ```python
  class Person:
      def __init__(self, name):
          self.name = name
      def greet(self):
          print("Hello, my name is", self.name)
  p = Person("Alice")
  p.greet()
  ```

---

This covers the most essential Python basics for beginners, with code examples for each concept.
