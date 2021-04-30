# Funktioner

## ```void``` - inget returvärde:
``` python
def print_msg(s):
    print('Hello', s)
```

```
>>> def print_msg(s):
...     print('Hello', s)
...
>>> print_msg('World')
('Hello', 'World')
```

## ```return```
``` python
def create_msg(s):
    return 'Hello {}!'.format(s)
```