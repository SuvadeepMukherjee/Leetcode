# HashSet

```python
mySet = set()
# no duplicates
#adding to a set T:O(1)
mySet.add(1)
mySet.add(2)
print(mySet)

print(len(mySet))
#checking if a number exists in a set T:O(1)
print(1 in mySet)
print(2 in mySet)
print(3 in mySet)

mySet.remove(2)
print(2 in mySet)

#list to set
print(set([1,2,3]))

#Set Comprehension
mySet ={i for i in range(5)}
print(mySet)
```

