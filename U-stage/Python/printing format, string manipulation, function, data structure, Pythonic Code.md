# 1. Printing Formats
- Many ways to use variables when printing. Here I write the easiest and the newest way to print output, which is 'f-string'
- I think this is important because even the students who are fluent in Python does not know the detailed syntax for printing
- Just write 'f' before the string and place variables inside { }. So simple, right?
```
   >>> name = 'JK'
   >>> age = '39'
   >>> print(f"Hello, {name}. Are you {age} years old?")
   Hello, JK. Are you 39 years old?
```
- Left align is the default. To right align, write
```
   >>> print(f"{name:>10}")
            JK
```
- Adding multiple letters
```
   >>> print(f"{name:*>5}")
   *****JK
   >>> print(f"{name:*^10}")
   *****JK*****
```
- Specifying the length of the float under the decimal
```
   >>> n = 0.123456
   >>> print(f'{n:.3f}')
   0.123
```

# 2. String Manipulation
- Python has a powerful edge over other languages in terms of string manipulation due to its built-in functions. Knowing the capabilites and the functions of Python is important to use Python up to its full potential. 
- Below are some useful functions that I am not used to using
```
   >>> s = 'hello world'
   >>> s.capitalize()
   Hello world
   
   >>> s.title()
   Hello World
   
   >>> s.find('W')
   6
   
   >>> s.startswith('hel')
   True
   
   >>> s.endswith('rld')
   True
   
   >>> s = ' hello world '
   >>> s.strip()
   hello world
   
   >>> s = ' hello world '
   >>> s.rstrip()
    hello world
```
- You can put r before a string to not use escape symbol and instead print it
```
   >>>print(r'Hello \n World!")
   Hello \n World!
```
# 3. Function
## a. Function Type Hints
- Type is specified, thus better statbility of the system
- Better documentation
- Can debug before running the program using editors such as mypy, IDE, and linter
```
>>> def f(var: str) -> str:
...     return var + '!'
```
## b. docstring
- Better documentation
```
>>> def sqaure(x):
...     '''Returns the sqaure of x'''
...     return x**2
```
# 4. Data Structure
- Stack
   * last in first out
   * can be implemented using append() and pop() with list
- Queue
   * first in first out
   * can be implemented using append() and pop(0) with list
- Set
   * no repetition of same value
   * Below are some useful operations for set data structure
   ```
      >>> s = set([1,2,3])
      >>> s.add(1)
      >>> s
      {1, 2, 3}
      >>> s.remove(1)
      >>> s
      {2, 3}
      >>> s.update([4,5])
      >>> s
      {1,2,3,4,5}
      >>> s.discard(3)
      >>> s
      {1,2,4,5}
      >>> s2 = set([3,4,5])
      >>> s1.union(s2)
      {1,2,3,4,5}
      >>> s1.intersection(s2)
      {3}
      >>> s1.difference(s2)
      {1,2}
- Deque
   * Can implement both stack and queue
   * more efficient than list
   * supports all functions for list
# 5. Pythonic Code
- This was the most impressive part of the lecture. I found out that I naturally adopted some pythonic syntaxes while trying to make my coding more concise and efficent
- Pythonic Code is usually shorter and faster
## a. Split and Join
```
>>> 'python java javascript'.split()
['python', 'java', 'javascript']
>>> asd = 'python java javascript'.split()
>>> ' '.join(asd)
python java javascript
```
## b. List Comprehension
```
>>> even_under10 = [i for i in range(10) if i % 2== 0]
>>> even_under10
[0, 2, 4, 6, 8,]
```
## c. Enumerate and Zip
```
>>> for ind, val in enumerate(['Hello', 'World']):
...     print(ind, val)
0 Hello
1 World

>>> a_lst = ['a1', 'a2']
>>> b_lst = ['b1', 'b2']
>>> for a, b in zip(a_lst, b_lst):
...     print(a, b)
a1 b1
a2 b2
```
## d. Generator
- Generator produces the element only when the element should be used
```
   gen = (x for x in range(100))
```
## e. Using Asterisk in Functions
- *args (arguments) and **kwargs (keyword arguements)
- if *args is used as a parameter, it could receive none to many variables. If many arguments, receive as tuple
- if **kwargs is used, it receives values as dictionary (name of value and value)
