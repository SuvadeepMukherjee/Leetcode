# Chap 14 | Loops Part 1

## While Loop

------

```python
while expression:
	statement
```

Loop repeats as long as expression is True

```python
answer = input("Please say hi")

while answer!="hi":

    print("Rude .Say hi....")

print("Thank you .Hi to you too!")
```

## For Loop

------

```python
for item in itterable:

	statement


```

Example:

```python
word ="Hello"

for char in word:

    print(char)
```

## The range() Function

------

```python
for num in range(start(inclusive),end(exclusive),step):

	print(num)
  
  
for num in range(start(inclusive),end(exclusve)):
  print(num)
#step defaults to 1 

for num in range(end(exclusive)):
  print(num)
# start defaults to 1 and step defaults to 1 

```



 