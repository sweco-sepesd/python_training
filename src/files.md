# Filer - IO

```python
fp = r"C:\Users\p19749\projekt\20210429_pythonkurs\python\agenda.txt"
fin = open(fp)
for l in fin:
    if not len(l.strip()): continue
    print(l.strip())
```

```python
fp = r"C:\Users\p19749\projekt\20210429_pythonkurs\python\agenda.txt"
it = (
    '{:03d} `{}`{}'.format(i, l.strip()[:20], ['', '...'][len(l)>20]) 
    for i,l in enumerate(open(fp)) 
    if l.strip()
)
print('\n'.join(it))
```
