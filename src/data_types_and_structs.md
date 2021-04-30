# Datatyper och strukturer


[Inbyggda funktioner](https://docs.python.org/2.7/library/functions.html)

*"The principal built-in types are numerics, sequences, mappings, files, classes, instances and exceptions"*

### Numeriska
```int, float, long, complex```
``` python
i = 12
f = 12.3
l = 5L
```
### Sekvenser
[Sequence Types](https://docs.python.org/2.7/library/stdtypes.html#sequence-types-str-unicode-list-tuple-bytearray-buffer-xrange)

list (mutable):
``` python
a = [1,2,'3']
```

tuple (immutable):
``` python
>>> b = (1,2,3)
>>> type(b)
<type 'tuple'>
>>> len(b)
3
>>> b[0]
1
>>> b[0] = 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
```

### Mappningar
dict (mutable):
``` python
>>> c = {'a': [1,2,'3'], 'b': (1,2,3)}
>>> c['b']
(1, 2, 3)
>>> c['f'] = 'Hello'
>>> c.keys()
['a', 'b', 'f']
c[(1,2)] = 'hashable as key'

>>> c[[1,2]] = 'unhashable as key'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unhashable type: 'list'
```

### None (builtin constant)
``` python
>>> x = None
>>> x is None
True
>>> x == None
True
>>> x == 0
False
>>> if x:
...     print 'helo'
... else:
...     print 'goodbye'
... 
goodbye
```

### Text
... är också en sekvens (immutable)


```str```

``` python
>>> s = 'Hello World!'
>>> len(s)
12
>>> s[2]
'l'
```

unicode

```
chcp 1252
java -jar jython-standalone-2.7.2.jar
```

``` python
>>> unicode('åäö', encoding='latin1')
u'\xe5\xe4\xf6'
```

[String Methods](https://docs.python.org/2.7/library/stdtypes.html#string-methods)

#### Text formattering
[Format String Syntax](https://docs.python.org/2.7/library/string.html#format-string-syntax)

``` python
>>> 'Hello {}!'.format('World')
Hello World!

>>> # old school
>>> 'Hello %s!' % 'World'

```
##### Övning
Beskriv med kodexempel steg för steg vad som sker här:
``` python
print('# {0:}\n# {1:^78s}\n# {0:}'.format('~-'*39, '   '.join('Hello World!'.upper())))
```

### bool
``` Python
# builtin constants
True
False
```
``` Python
>>> if -1: print 'a'
... 
a

>>> not 0
True
```

