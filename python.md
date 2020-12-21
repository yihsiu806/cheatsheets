# Python Cheatsheet

```
def main():
    pass

if __name__ == '__main__':
    main()
```

```
print(val1, val2)
```

## Variable Name
```
[_0-9a-zA-Z]
```

## Type Conversion
```
int(val)
float(val)
string(val)
```

## Length
```
len(str)
len(list)
```

## in
```
val in list
val in dict
```

## is
```
if thing is None:
    print("It's no thing")
```

## String
```
'Single line string'

'''
multiple
line
string
'''
```

## List
```
l = []
l = list()
```

```
list[0]
list[2:5]
```

```
list.append()
list.pop()
list.sort()
list.copy()
```

```
list.attend(list)
list.insert(3, val)
list.remove(val)
del list[3]
```

## Tuple

Function arguments are passed as tuples.

```
t = ()
t = tuple()
```

```
a, b = (b, a)
```

## Dictionary
```
d = {}
d = dict()
```

```
d['key'] = value
d.get('key')
del d['key']
d.update(dict)
d.clear()
d.copy()
```

```
d.keys()
d.values()
d.items()
```

## Set
```
s = set()
s = {1, 2, 3}
```

## zip
```
for i1, i2 in zip(l1, l2):
    print(i1, i2)
```

## range
```
for x in range(0, 5):
    print(x)
```

## List Comprehension
```
[ expression for item in iterable if condition ]
```

```
my_list = [ num for num in range(1,6) if num % 2 == 1 ]
```

## Dictionary Comprehension
```
{ key_expression: value_expression for expression in iterable }
```

```
my_dict = { letter: word.count(letter) for letter in word }
```

## Generator Comprehension
```
num = (num for num in range(1,6))
```

## Function
```
def my_func():
    pass
```

```
my_func(18, name='yihsiu')
18 is positional argument
name='yihsiu' is keyword argument
```

### Default Parameter Values
```
def my_func(age=18, name=None):
    pass
```

### Group positional arguments to tuple
```python
def my_func(req1, req1, *args):
    print('Remaining arguments: ', args)
```

### Group keyword arguments to dictionary
```python
def my_func(**kwargs):
    print('Arguments: ', kwargs)

my_func(val1='1', val2='2')
```

### lambda
Anonymous function.
```
lambda word: word.capitalize() + '!'
```

## Generators
For saving memory space.
Generator comprehension.
Generator function.

```python
def my_range(first=0, last=10, step=1):
    num = first
    while num < last:
        yield num
```

## Decorators