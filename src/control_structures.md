# Kontrollstrukturer (```if, for...`)
```if, else, elif, for, while, return, break, continue, yield```

``` python
def classify(val):
    if val > 1 and val < 3:
        return '~2'
    elif val >= 3:
        return 'huge number'
    else:
        return 'did not expect that...'
```

``` python
x = 5
while x: # 0 evaluates to False
    print x
    x -= 1
```

Den [inbyggda funktionen](https://docs.python.org/2.7/library/functions.html#) [enumerate](https://docs.python.org/2.7/library/functions.html#enumerate) används nedan:

``` python
>>> for i,c in enumerate('Hello World!'):
...     if 'o' == c:
...         print i
...         break
... 
4
```

``` python
>>> # declare a list (mutable) for the results
>>> positions = []
>>> for i,c in enumerate('Hello World!'):
...      if 'o' != c: continue
...      positions.append(i)
... 
>>> positions
[4, 7]
```

```yield``` är en speciell typ av *lat* returinstruktion:

``` python
>>> def all_but_char(s,c):
...     for x in s:
...         if not x == c:
...             yield x
... 
>>> all_but_char('Hello World!', 'o')
<generator object all_but_char at 0x2>
>>> ''.join(all_but_char('Hello World!', 'o'))
'Hell Wrld!'
```
