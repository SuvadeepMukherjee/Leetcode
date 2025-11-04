# Tuples

```python
tup =(1,2,3)
print(tup)

#We can index them 
print(tup[0])
print(tup[-1])

# But we cant modify them 
# tup[0] = 0 # Cant do this

# tuples can be used as keys for hash map/set
myMap ={(1,2):3}
print(myMap[(1,2)])

mySet = set()
mySet.add((1,2))
print((1,2) in mySet)

# lists cant be keys 
# myMap[[3,4]] = 5 # illelegal
```

