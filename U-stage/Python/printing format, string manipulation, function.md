# 1. Printing Formats
- Many ways to use variables when printing. Here I write the easiest and the newest way to print output, which is 'f-string'
- I think this is important because even the students who are fluent in Python does not know the detailed syntax for printing
- Just write 'f' before the string and place variables inside { }. So simple, right?
```
   name = 'JK'
   age = '39'
   print(f"Hello, {name}. Are you {age} years old?")
   >>> Hello, JK. Are you 39 years old?
```
- Left align is the default. To right align, write
```
   print(f"{name:>10}")
   >>>         JK
```
- Adding multiple letters
```
   print(f"{name:*>5}")
   >>>*****JK
   print(f"{name:*^10}")
   >>>*****JK*****
```
- Specifying the length of the float under the decimal
```
   n = 0.123456
   print(f'{n:.3f}')
   >>> 0.123
```

# 2. String Manipulation
- Python has a powerful edge over other languages in terms of string manipulation due to its built-in functions. Knowing the capabilites and the functions of Python is important to use Python up to its full potential. 
- Below are some useful functions that I am not used to using
```
   s = 'hello world'
   s.capitalize()
   >>> 'Hello world'
   
   s.title()
   >>> 'Hello World'
   
   s.find('W')
   >>> 6
   
   s.startswith('hel')
   >>> True
   
   s.endswith('rld')
   >>> True
   
   s = ' hello world '
   s.strip()
   >>> 'hello world'
   
   s = ' hello world '
   s.rstrip()
   >>> ' hello world'
```
- You can put r before a string to not use escape symbol and instead print it
```
   print(r'Hello \n World!")
   >>> 'Hello \n World!"
```
# 3. Function
## a. Function Type Hints
- Type is specified, thus better statbility of the system
- Better documentation
- Can debug before running the program using editors such as mypy, IDE, and linter
```
   def f(var: str) -> str:
      return var + '!'
```
## b. docstring
- Better documentation
```
   def sqaure(x):
   '''Returns the sqaure of x'''
      return x**2
```



