# HashMap

```python
myMap ={}
myMap["alice"] = 88
myMap["bob"] = 77
# cant have duplicate keys
print(myMap)

print(len(myMap))

# Can modify values
myMap["alice"] = 80
print(myMap["alice"])

# Searching whether a key exists in a HashMap
print("alice" in myMap)
myMap.pop("alice")
print("alice" in myMap)

myMap = {"alice":90,"bob":70}
print(myMap)

#Dict Comprehension
myMap ={i:2*i for i in range(3)}
print(myMap)

#Looping through Maps
myMap = {"alice":90,"bob":70}
for key in myMap:
     print(key,myMap[key])

for val in myMap.values():
    print(val)

for key,val in myMap.items():
    print(key,val)
```

