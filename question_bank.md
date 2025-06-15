# QUESTION BANK FOR PYTHON PROGRAMMING TECHNIQUES (TIU-UCA-MJ-T22201)

---

## 1. What are the Logical operators available in Python state with example? (2)

Python provides three logical operators:
- `and`: Returns True if both statements are true.
- `or`: Returns True if at least one statement is true.
- `not`: Reverses the result, returns False if the result is true.

**Example:**
```python
x = 5
y = 10
print(x > 0 and y > 0)  # True
print(x > 0 or y < 0)   # True
print(not(x > 0))       # False
```

> "Logical operators are used to combine conditional statements."

---

## 2. State with an example, the role of the following operators:
### i) `is`  ii) `in`  iii) `not in`  iv) `<<`  v) `>>` (5)

- `is`: Checks if two variables refer to the same object.
  ```python
  a = [1, 2]
  b = a
  print(a is b)  # True
  ```
- `in`: Checks if a value exists in a sequence.
  ```python
  print(3 in [1, 2, 3])  # True
  ```
- `not in`: Checks if a value does not exist in a sequence.
  ```python
  print(4 not in [1, 2, 3])  # True
  ```
- `<<`: Bitwise left shift operator.
  ```python
  print(2 << 2)  # 8 (2*2^2)
  ```
- `>>`: Bitwise right shift operator.
  ```python
  print(8 >> 2)  # 2 (8/2^2)
  ```

> "The `is` operator checks identity, not equality. `in` and `not in` are used for membership tests. `<<` and `>>` are used for bitwise operations."

---

## 3. Describe if-elif-else structure with an example. (5)

The `if-elif-else` structure is used for multi-way decision making in Python.

**Syntax:**
```python
if condition1:
    # code block
elif condition2:
    # code block
else:
    # code block
```

**Example:**
```python
num = 10
if num > 0:
    print("Positive")
elif num == 0:
    print("Zero")
else:
    print("Negative")
```

> "Use `elif` for multiple conditions. Only the first true condition's block is executed."

---

## 4. Take an age and find if he or she is Child or Teenage or Adult or Senior Citizen. (5)

**Program:**
```python
age = int(input("Enter age: "))
if age < 13:
    print("Child")
elif age < 20:
    print("Teenage")
elif age < 60:
    print("Adult")
else:
    print("Senior Citizen")
```

---

## 5. Take a year and find leap year or not. (5)

**Program:**
```python
year = int(input("Enter year: "))
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print("Leap Year")
else:
    print("Not a Leap Year")
```

> "A leap year is divisible by 4, but not by 100 unless also divisible by 400."

---

## 6. The marks obtained by a student in 3 different subjects are input through the keyboard. The student gets a division as per the following rules:
- Percentage >= 60: First division
- Percentage 50-59: Second division
- Percentage 40-49: Third division
- Percentage < 40: Fail
Write a program to calculate the division obtained by the student. (5)

**Program:**
```python
marks1 = float(input("Enter marks for subject 1: "))
marks2 = float(input("Enter marks for subject 2: "))
marks3 = float(input("Enter marks for subject 3: "))
percentage = (marks1 + marks2 + marks3) / 3
if percentage >= 60:
    print("First division")
elif percentage >= 50:
    print("Second division")
elif percentage >= 40:
    print("Third division")
else:
    print("Fail")
```

---

## 7. Describe range() function with an example. (3)

The `range()` function generates a sequence of numbers, commonly used in loops.

**Example:**
```python
for i in range(1, 6):
    print(i)
# Output: 1 2 3 4 5
```

> "range(start, stop, step) generates numbers from start to stop-1, incremented by step."

---

## 8. Write a program to print all odd non-prime numbers between 1 to 50. (5)

**Program:**
```python
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True
for i in range(1, 51):
    if i % 2 != 0 and not is_prime(i):
        print(i, end=' ')
```

---

## 9. Calculates the sum of digits of a number. (5)

**Program:**
```python
num = int(input("Enter a number: "))
sum_digits = 0
while num > 0:
    sum_digits += num % 10
    num //= 10
print("Sum of digits:", sum_digits)
```

---

## 10. Print the following pattern for n=4: (5)
```
1
22
333
4444
```
**Program:**
```python
n = 4
for i in range(1, n+1):
    print(str(i) * i)
```

---

## 11. Write a program to calculate the sum of the following series: (5)
S = 1/2 + 2/3 + 3/4 + ... + n/(n+1) [n should be user input]

**Program:**
```python
n = int(input("Enter n: "))
sum_series = 0
for i in range(1, n+1):
    sum_series += i / (i+1)
print("Sum of series:", sum_series)
```

---

## 12. Difference between break and continue with example. (5)

- `break`: Exits the loop completely.
- `continue`: Skips the current iteration and continues with the next.

**Example:**
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

> "Use `break` to exit a loop early, `continue` to skip to the next iteration."

---

## 13. Define a function which will take principal amount, time in years and rate of interest in percentage as input and calculate the simple interest. All the three arguments have default values – 1000 (principal amount), 5 (time in years) and 10 (rate of interest in percentage). Call the function from main module with all possible ways and calculate the simple interest each time. (5)

**Program:**
```python
def simple_interest(principal=1000, time=5, rate=10):
    return (principal * time * rate) / 100

# Calling with all default values
print(simple_interest())
# Calling with one argument
print(simple_interest(2000))
# Calling with two arguments
print(simple_interest(2000, 3))
# Calling with all arguments
print(simple_interest(2000, 3, 8))
```
> "Default arguments allow a function to be called with fewer arguments than it is defined to accept."

---

## 14. Define a function which will calculate factorial of a number and call the function from main module with a value taken from user. (5)

**Program:**
```python
def factorial(n):
    result = 1
    for i in range(1, n+1):
        result *= i
    return result

num = int(input("Enter a number: "))
print("Factorial:", factorial(num))
```

---

## 15. Define a function which will accept name of a student and a set of sports that he/she likes and this function will display the student name and his/her favorite sports. Use variable length argument in the function parameter so that different student can have different number of favorite sports. (5)

**Program:**
```python
def fav_sports(name, *sports):
    print("Student Name:", name)
    print("Favorite Sports:", ', '.join(sports))

fav_sports("Amit", "Cricket", "Football")
fav_sports("Sara", "Tennis")
```
> "The *args syntax allows a function to accept any number of positional arguments."

---

## 16. What is function? What is the advantage and disadvantage of using function? (2+2+2)

- **Function:** A function is a block of code that performs a specific task and can be reused.
- **Advantages:**
  - Code reusability
  - Modularity
  - Easier debugging and maintenance
- **Disadvantages:**
  - Overuse can make code harder to follow
  - Function calls add overhead

> "Functions help organize code, but too many small functions can reduce readability."

---

## 17. Using lambda function to check whether a number is Positive, negative or zero. (3)

**Program:**
```python
check = lambda x: "Positive" if x > 0 else ("Negative" if x < 0 else "Zero")
num = int(input("Enter a number: "))
print(check(num))
```

---

## 18. Using lambda function to check whether the number is even or odd (3)

**Program:**
```python
even_odd = lambda x: "Even" if x % 2 == 0 else "Odd"
num = int(input("Enter a number: "))
print(even_odd(num))
```

---

## 19. What is the role of return and def keyword with respect to function? (2)

- `def`: Used to define a function in Python.
- `return`: Used to exit a function and return a value to the caller.

> "The `def` keyword starts a function definition. The `return` keyword sends a result back to where the function was called."

---

## 20. Define recursion. Differentiate it with iteration. (2+3)

- **Recursion:** When a function calls itself to solve a problem.
- **Difference:**
  - Recursion solves a problem by breaking it into smaller subproblems, calling itself.
  - Iteration uses loops to repeat code until a condition is met.
  - Recursion can be more elegant but may use more memory due to function call stack.

> "Recursion is best for problems that can be divided into similar subproblems."

---

## 21. Write a python program to print Fibonacci series using recursion (5)

**Program:**
```python
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)

n = int(input("Enter number of terms: "))
for i in range(n):
    print(fibonacci(i), end=' ')
```

---

## 22. Write a python program to print Factorial using recursion (5)

**Program:**
```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n-1)

num = int(input("Enter a number: "))
print("Factorial:", factorial(num))
```

---

## 23. Define a recursive function to find out sum of digits of a number (number should be user input). (5)

**Program:**
```python
def sum_digits(n):
    if n == 0:
        return 0
    else:
        return n % 10 + sum_digits(n // 10)

num = int(input("Enter a number: "))
print("Sum of digits:", sum_digits(num))
```

---

## 24. Difference between class and object. (3)

- **Class:** A blueprint or template for creating objects. It defines attributes and methods.
- **Object:** An instance of a class. It represents a specific entity with values assigned to the attributes defined by the class.

> "A class is like a blueprint, and an object is like a house built from that blueprint."

---

## 25. Define the following: a) Abstraction b) Encapsulation (3+3)

- **Abstraction:** Hiding the complex implementation details and showing only the necessary features of an object.
  > "Abstraction helps in reducing programming complexity and effort."
- **Encapsulation:** Wrapping up data and methods into a single unit (class) and restricting access to some of the object's components.
  > "Encapsulation is implemented using private and public access specifiers."

---

## 26. What is inheritance? Advantages of Inheritance. Types of Inheritance. (2+2+3)

- **Inheritance:** The process by which one class (child) acquires the properties and behaviors (methods) of another class (parent).
- **Advantages:**
  - Code reusability
  - Method overriding
  - Easier code maintenance
- **Types of Inheritance:**
  - Single Inheritance
  - Multiple Inheritance
  - Multilevel Inheritance
  - Hierarchical Inheritance
  - Hybrid Inheritance

---

## 27. Frame class Account with object variable account holder's name, account number and balance. Create multiple objects of Account class and perform withdraw, deposit and check balance operations on that account. Also, keep track of how many accounts you have created by using a class variable. (5)

**Program:**
```python
class Account:
    count = 0  # Class variable
    def __init__(self, name, acc_no, balance):
        self.name = name
        self.acc_no = acc_no
        self.balance = balance
        Account.count += 1
    def deposit(self, amount):
        self.balance += amount
    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
        else:
            print("Insufficient balance")
    def check_balance(self):
        print(f"Balance for {self.name}: {self.balance}")

# Creating objects
acc1 = Account("Amit", 101, 5000)
acc2 = Account("Sara", 102, 3000)
acc1.deposit(1000)
acc2.withdraw(500)
acc1.check_balance()
acc2.check_balance()
print("Total accounts created:", Account.count)
```

---

## 28. Frame a Student class with object variable student name, roll and marks. Create two student objects and display their details. (5)

**Program:**
```python
class Student:
    def __init__(self, name, roll, marks):
        self.name = name
        self.roll = roll
        self.marks = marks
    def display(self):
        print(f"Name: {self.name}, Roll: {self.roll}, Marks: {self.marks}")

s1 = Student("Amit", 1, 85)
s2 = Student("Sara", 2, 90)
s1.display()
s2.display()
```

---

## 29. Frame a base class Person which contains object variable name and age of a person. It should have a display_person() method which will display details of a person. Frame another two classes Student and Teacher (both should inherit the base class Person) which will contain roll and marks (for Student) and subject and experience (for Teacher). Student class should contain display_student() method which will display student record and Teacher class should contain display_teacher() method which will display teacher record. Write a program in python to test the above classes. (10)

**Program:**
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def display_person(self):
        print(f"Name: {self.name}, Age: {self.age}")

class Student(Person):
    def __init__(self, name, age, roll, marks):
        super().__init__(name, age)
        self.roll = roll
        self.marks = marks
    def display_student(self):
        self.display_person()
        print(f"Roll: {self.roll}, Marks: {self.marks}")

class Teacher(Person):
    def __init__(self, name, age, subject, experience):
        super().__init__(name, age)
        self.subject = subject
        self.experience = experience
    def display_teacher(self):
        self.display_person()
        print(f"Subject: {self.subject}, Experience: {self.experience} years")

# Testing
s = Student("Amit", 20, 1, 85)
t = Teacher("Sara", 35, "Math", 10)
s.display_student()
t.display_teacher()
```

---

## 30. Explain Method overriding with an example. (5)

- **Method Overriding:** When a child class provides a specific implementation of a method that is already defined in its parent class.

**Example:**
```python
class Animal:
    def speak(self):
        print("Animal speaks")
class Dog(Animal):
    def speak(self):
        print("Dog barks")

d = Dog()
d.speak()  # Output: Dog barks
```
> "Method overriding allows a subclass to provide a specific implementation of a method."

---

## 31. Which special method is automatically called to create objects in Python? What does self keyword represent? (2+2)

- The `__init__` method is automatically called to create objects (constructor).
- `self` represents the instance of the class and is used to access variables and methods of the class.

---

## 32. Reverse a string using Slicing. (3)

**Program:**
```python
s = input("Enter a string: ")
print("Reversed string:", s[::-1])
```

---

## 33. Take a string and check Palindrome or not. (5)

**Program:**
```python
s = input("Enter a string: ")
if s == s[::-1]:
    print("Palindrome")
else:
    print("Not Palindrome")
```

---

## 34. Explain the following string methods with example: a) isalnum() b) upper() c) lower() d) startswith() e) endswith() Each carries 2 mark

- `isalnum()`: Returns True if all characters are alphanumeric.
  ```python
  print("abc123".isalnum())  # True
  ```
- `upper()`: Converts all characters to uppercase.
  ```python
  print("hello".upper())  # HELLO
  ```
- `lower()`: Converts all characters to lowercase.
  ```python
  print("HELLO".lower())  # hello
  ```
- `startswith()`: Checks if string starts with a specified value.
  ```python
  print("hello".startswith("he"))  # True
  ```
- `endswith()`: Checks if string ends with a specified value.
  ```python
  print("hello".endswith("lo"))  # True
  ```

---

## 35. Differentiate between list aliasing and list cloning with example. (5)

- **List Aliasing:** Assigning a list to another variable creates an alias, both refer to the same list.
  ```python
  a = [1, 2, 3]
  b = a
  b[0] = 10
  print(a)  # [10, 2, 3]
  ```
- **List Cloning:** Creating a copy of the list so that changes in one do not affect the other.
  ```python
  a = [1, 2, 3]
  b = a[:]
  b[0] = 10
  print(a)  # [1, 2, 3]
  print(b)  # [10, 2, 3]
  ```
> "Aliasing means both variables point to the same list, cloning creates a new list."

---

## 36. Write a program that uses list comprehension to create a list which contains sum of squares of one even number and one odd number where the even number will come from the numbers 1 to 5 and the odd number will come from the numbers 6 to 10. (5)

**Program:**
```python
even = [x for x in range(1, 6) if x % 2 == 0]
odd = [y for y in range(6, 11) if y % 2 != 0]
sum_squares = [e**2 + o**2 for e in even for o in odd]
print(sum_squares)
```

---

## 37. Write a program that uses list comprehension to create a list which contains cubes of all even numbers from the numbers 1 to 20. (3)

**Program:**
```python
even_cubes = [x**3 for x in range(1, 21) if x % 2 == 0]
print(even_cubes)
```

---

## 38. Implement a STACK using a list. (5)

**Program:**
```python
stack = []
# Push
stack.append(10)
stack.append(20)
stack.append(30)
print("Stack after pushes:", stack)
# Pop
print("Popped element:", stack.pop())
print("Stack after pop:", stack)
```
> "A stack is a LIFO (Last In First Out) data structure."

---

## 39. Implement a QUEUE using a list. (5)

**Program:**
```python
queue = []
# Enqueue
queue.append(10)
queue.append(20)
queue.append(30)
print("Queue after enqueues:", queue)
# Dequeue
print("Dequeued element:", queue.pop(0))
print("Queue after dequeue:", queue)
```
> "A queue is a FIFO (First In First Out) data structure."

---

## 40. Write a program that uses filter() function to filter out only even numbers from a list. (3)

**Program:**
```python
lst = [1, 2, 3, 4, 5, 6]
evens = list(filter(lambda x: x % 2 == 0, lst))
print(evens)
```

---

## 41. Write a program that uses map() function to print the square value of each element in a list. (3)

**Program:**
```python
lst = [1, 2, 3, 4, 5]
squares = list(map(lambda x: x**2, lst))
print(squares)
```

---

## 42. Write a program that uses filter() function to create a list of numbers from 1 to 50 that are either divisible by 3 or divisible by 6. (5)

**Program:**
```python
nums = list(range(1, 51))
result = list(filter(lambda x: x % 3 == 0 or x % 6 == 0, nums))
print(result)
```

---

## 43. Write a program to find multiplication of all values in a list using reduce() function. (3)

**Program:**
```python
from functools import reduce
lst = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, lst)
print(product)
```

---

## 44. Explain the following list methods with example: (2)
### a) append() b) insert() c) remove() d) count() e) extend() f) index()

- `append()`: Adds an element at the end of the list.
  ```python
  lst = [1, 2]
  lst.append(3)
  print(lst)  # [1, 2, 3]
  ```
- `insert()`: Inserts an element at a specified position.
  ```python
  lst.insert(1, 5)
  print(lst)  # [1, 5, 2, 3]
  ```
- `remove()`: Removes the first occurrence of a value.
  ```python
  lst.remove(5)
  print(lst)  # [1, 2, 3]
  ```
- `count()`: Returns the number of times a value appears.
  ```python
  print(lst.count(2))  # 1
  ```
- `extend()`: Adds all elements of an iterable to the end of the list.
  ```python
  lst.extend([4, 5])
  print(lst)  # [1, 2, 3, 4, 5]
  ```
- `index()`: Returns the index of the first occurrence of a value.
  ```python
  print(lst.index(3))  # 2
  ```

---

## 45. Difference between del(), pop() and remove(). (3)

- `del()`: Deletes an element at a specific index or deletes the entire list.
- `pop()`: Removes and returns an element at a given index (default is last).
- `remove()`: Removes the first occurrence of a value.

> "`del` is for index or whole list, `pop` returns the value, `remove` is for value."

---

## 46. Difference between sort() and sorted(). (3)

- `sort()`: Sorts the list in place and returns None.
- `sorted()`: Returns a new sorted list from the elements of any iterable.

> "Use `sort()` to modify the original list, `sorted()` to keep the original unchanged."

---

## 47. Difference between list and tuple. (3)

- **List:** Mutable, can be changed after creation, uses square brackets [].
- **Tuple:** Immutable, cannot be changed after creation, uses parentheses ().

> "Lists are mutable, tuples are immutable."

---

## 48. Write a program that defines a list of countries that are members of SAARC. Take one country name from user and check whether that country is a member of SAARC or not. (3)

**Program:**
```python
saarc = ["Afghanistan", "Bangladesh", "Bhutan", "India", "Maldives", "Nepal", "Pakistan", "Sri Lanka"]
country = input("Enter country name: ")
if country in saarc:
    print("Member of SAARC")
else:
    print("Not a member of SAARC")
```

---

## 49. Write a program to remove all duplicate objects from a list. (5)

**Program:**
```python
lst = [1, 2, 2, 3, 4, 4, 5]
unique_lst = list(set(lst))
print(unique_lst)
```
> "Using set() removes duplicates but does not preserve order."

---

## 50. Write a program that creates a list of ten random integers. Then create two lists- Odd list and even list that has all odd and even values in the list respectively. (5)

**Program:**
```python
import random
lst = [random.randint(1, 100) for _ in range(10)]
odds = [x for x in lst if x % 2 != 0]
evns = [x for x in lst if x % 2 == 0]
print("Original list:", lst)
print("Odd list:", odds)
print("Even list:", evns)
```

---

## 51. State the enumerate () function with an example. (3)

- `enumerate()` adds a counter to an iterable and returns it as an enumerate object.
  ```python
  lst = ['a', 'b', 'c']
  for index, value in enumerate(lst):
      print(index, value)
  # Output: 0 a  1 b  2 c
  ```

---

## 52. State with an example how zip() function works. (3)

- `zip()` combines two or more iterables (lists, tuples, etc.) element-wise.
  ```python
  questions = ["Name", "Age"]
  answers = ["Amit", 20]
  for q, a in zip(questions, answers):
      print(q, ":", a)
  # Output: Name : Amit  Age : 20
  ```

---

## 53. Write a program that has two sequences. First which stores some questions and second stores the corresponding answers. Use the zip() function to form a valid question answer series. (5)

**Program:**
```python
questions = ["What is your name?", "What is your age?"]
answers = ["Amit", "20"]
for q, a in zip(questions, answers):
    print(q, a)
```

---

## 54. Describe the following functions with an example a)filter() b)map() c)reduce() [3 mark each]

- `filter()`: Filters elements based on a function.
  ```python
  lst = [1, 2, 3, 4]
  evens = list(filter(lambda x: x % 2 == 0, lst))
  print(evens)  # [2, 4]
  ```
- `map()`: Applies a function to all elements.
  ```python
  squares = list(map(lambda x: x**2, lst))
  print(squares)  # [1, 4, 9, 16]
  ```
- `reduce()`: Applies a rolling computation to sequential pairs.
  ```python
  from functools import reduce
  product = reduce(lambda x, y: x * y, lst)
  print(product)  # 24
  ```

---

## 55. Differentiate between append() and insert() with respect to list.

- `append()`: Adds an element at the end of the list.
- `insert()`: Inserts an element at a specified position in the list.

---

## 56. Differentiate between list and set. (3)

- **List:** Ordered, allows duplicate elements, mutable.
- **Set:** Unordered, does not allow duplicates, mutable.

---

## 57. Describe the following set operations using functions and operators
### a) union b) intersection c) difference d) issubset e) issuperset [each 2 mark]

- **Union:** Combines all elements from both sets.
  ```python
  a = {1, 2, 3}
  b = {3, 4, 5}
  print(a | b)  # {1, 2, 3, 4, 5}
  print(a.union(b))
  ```
- **Intersection:** Elements common to both sets.
  ```python
  print(a & b)  # {3}
  print(a.intersection(b))
  ```
- **Difference:** Elements in one set but not the other.
  ```python
  print(a - b)  # {1, 2}
  print(a.difference(b))
  ```
- **issubset:** Checks if all elements of one set are in another.
  ```python
  print({1, 2}.issubset(a))  # True
  ```
- **issuperset:** Checks if a set contains all elements of another set.
  ```python
  print(a.issuperset({1, 2}))  # True
  ```

---

## 58. Define dictionary in python. Differentiate it with a list. (2+3)

- **Dictionary:** An unordered collection of key-value pairs.
- **Difference:**
  - List: Ordered, accessed by index.
  - Dictionary: Unordered, accessed by key.

---

## 59. Describe the following operations on dictionary
### a) add an item b) modify an item c) delete an item d) return a list of keys e) return a list of value [2 mark each]

- **Add an item:**
  ```python
  d = {}
  d['a'] = 1
  print(d)
  ```
- **Modify an item:**
  ```python
  d['a'] = 2
  print(d)
  ```
- **Delete an item:**
  ```python
  del d['a']
  print(d)
  ```
- **Return a list of keys:**
  ```python
  d = {'a': 1, 'b': 2}
  print(list(d.keys()))
  ```
- **Return a list of values:**
  ```python
  print(list(d.values()))
  ```

---

## 60. WAP that creates a dictionary of cubes of odd numbers in the range 1-10. (3)

**Program:**
```python
cubes = {x: x**3 for x in range(1, 11) if x % 2 != 0}
print(cubes)
```

---

## 61. Create a user defined module which contains a function that will calculate maximum of two numbers. WAP in main module that will take two integer values from user and find out the larger of the two values using the above function. (5)

**max_module.py:**
```python
def maximum(a, b):
    return a if a > b else b
```
**main.py:**
```python
from max_module import maximum
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print("Maximum:", maximum(a, b))
```

---

## 62. State the difference between local and global variables with a snippet of code. (5)

- **Local variable:** Defined inside a function, accessible only within that function.
- **Global variable:** Defined outside all functions, accessible anywhere in the code.

**Example:**
```python
global_var = 10

def func():
    local_var = 5
    print("Local:", local_var)
    print("Global:", global_var)

func()
print("Global outside function:", global_var)
```

---

## 63. Create your own module and use that module in another module to solve a particular problem. (5)

**math_utils.py:**
```python
def add(a, b):
    return a + b
```
**main.py:**
```python
from math_utils import add
print(add(3, 4))
```

---

## 64. Use the numpy module to perform the following operations
### a) inverse of a matrix b) rank of a matrix c) transpose of a matrix d) multiplication of two matrices e) find out determinant of a matrix [Each 2 mark]

**Program:**
```python
import numpy as np
A = np.array([[1, 2], [3, 4]])
# a) Inverse
print(np.linalg.inv(A))
# b) Rank
print(np.linalg.matrix_rank(A))
# c) Transpose
print(A.T)
# d) Multiplication
B = np.array([[5, 6], [7, 8]])
print(np.dot(A, B))
# e) Determinant
print(np.linalg.det(A))
```

---

## 65. WAP using numpy module to create a 3×3 identity matrix. (2)

**Program:**
```python
import numpy as np
print(np.identity(3))
```

---

## 66. WAP using numpy module to create a 3×2 matrix whose every element is filled with the number 2. (2)

**Program:**
```python
import numpy as np
print(np.full((3, 2), 2))
```

---

## 67. WAP using numpy module to create a 3×3 matrix whose every element is filled with random integers numbers between 5-9. (2)

**Program:**
```python
import numpy as np
print(np.random.randint(5, 10, (3, 3)))
```

---

## 68. WAP in Python using matplotlib to create a pie chart showing how hours in a day are spent on the basis of the activities like 'Sleeping', 'Eating', 'Working' and 'Playing'. (5)

**Program:**
```python
import matplotlib.pyplot as plt
activities = ['Sleeping', 'Eating', 'Working', 'Playing']
hours = [8, 2, 8, 6]
plt.pie(hours, labels=activities, autopct='%1.1f%%')
plt.title('Daily Activities')
plt.show()
```

---

## 69. WAP in Python to create a scatter plot using matplotlib that shows the number of hours students spend practicing programming over a week and their corresponding scores in a weekly coding test. (5)

**Program:**
```python
import matplotlib.pyplot as plt
hours = [1, 2, 3, 4, 5, 6, 7]
scores = [50, 55, 60, 65, 70, 75, 80]
plt.scatter(hours, scores)
plt.xlabel('Hours Practiced')
plt.ylabel('Test Score')
plt.title('Practice vs Test Score')
plt.show()
```

---

## 70. WAP in Python to create a bar graph using matplotlib that represents the marks obtained by a student in five subjects: English, Math, Science, History, and Computer Science. (5)

**Program:**
```python
import matplotlib.pyplot as plt
subjects = ['English', 'Math', 'Science', 'History', 'Computer Science']
marks = [85, 90, 78, 88, 92]
plt.bar(subjects, marks)
plt.xlabel('Subjects')
plt.ylabel('Marks')
plt.title('Marks in Subjects')
plt.show()
```

---

## 71. Differentiate between testing and debugging. (3)

- **Testing:** The process of finding errors in a program by running it with test data.
- **Debugging:** The process of identifying, analyzing, and removing errors from a program.

> "Testing finds bugs, debugging fixes them."

---

## 72. Differentiate between black-box and white-box testing. (5)

- **Black-box testing:** Testing without knowledge of the internal code structure. Focuses on input and output.
- **White-box testing:** Testing with knowledge of the internal code structure. Focuses on code logic and paths.

> "Black-box: tester does not see code. White-box: tester examines code logic."

---

**END OF QUESTION BANK ANSWERS**
