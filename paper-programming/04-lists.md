# Tracing Lists

## 4.1
```python
a = [5, 2, 4, 6, 3]
c = ["a", "b", "c", "d", "e", "f"]
b = ""
for d in a:
    b += c[d]

print(b)
```




## 4.2
```python
a = ["hello", "hat", "bat", "shell", "tv", "livingroom", "heavy"]
for b in a:
    c = 0
    if b[0] == "h":
        c += 1

print(c)
```

## 4.3
### Trace with inputs: `3`, `2`, `5`, `4`, `3`
```python
a = []
for _ in range(5):
    b = int(input())
    a.append(b) 

print(a)
```

## 4.4
```python
marks = [100, 98, 65, 48, 25, 43, 85, 77, 75]
i = 0
while i < len(marks):
    mark = marks[i]
    print(mark)
    if mark < 50:
        marks.remove(mark)
    i += 1

print(marks)
```

## 4.5
```python
a = [100, 98, 65, 48, 25, 43, 85, 77, 75]
b = []
c = 0
while c < len(a):
    d = a[c]
    if d >= 50:
        b.append(d)
    c += 1
print(b)
```

## 4.6
```python
friends = ["Jim", "David", "Sally", "Jesse", "Sally", "Raphael"]
for_removal = "Sally"
i = 0
while i < len(friends):
    if friends[i] == for_removal:
        del friends[i]
        break
    i += 1
print(friends)
```

## 4.7
```python
friends = ["Jim", "David", "Sally", "Jesse", "Sally", "Raphael"]
for_removal = "Sally"
i = 0
while i < len(friends):
    if friends[i] == for_removal:
        del friends[i]
    else:
        i += 1

print(friends)
```


