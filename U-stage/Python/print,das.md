# 1. Printing Formats
- Many ways to use variables when printing. Here I write the easiest and the newest way to print output, which is 'f-string'
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
