# Python for Coding Interviews - Neetcode

[Youtube Link](https://www.youtube.com/watch?v=0K_eZGS5NsU&t=922s)

## Variables

- Variables are dynamic

  ```python
  n=0
  
  m='abc'
  ```

- Multiple assignments

  ```python
  n,m=0,'abc'
  
  ```

- Increment

  ```python
  n=n+1 #good
  
  n+=1 #good
  
  n++ #bad
  ```

- None is null (absence of value)

  ```python
  n,m = 0,'abc'
  ```

  

## If Statements

- If statements dont need parenthesis or curly braces

  ```python
  n=1
  if n>2:
    n-=1
  elif n==2:
  	n*+2
  else:
    n+=2
  
  ```

- Parenthesis need for multiple-line conditions

  ```python
  # and = &&
  # or =||
  n,m = 1,2
  if((n>2 and n!=m) or n==m):
  	n+=1
  ```

## Loops

- while loops are similar 

  ```python
  n=0
  while n<5:
  	print(n)
  	n+=1
  ```

- For loops 

  - looping from i=0 to i=4 

    ```python
    for(i in range(5)):
    	print(i)
    ```

  - Looping from i=2 to i=5

    ```python
     for(i in range(2,6)):
     	print(i)
    ```

  - Looping from i=5 to i=2 

    ```python
    for(i in range(5,1,-1)):
    	print(i)
    ```

  - Syntax : `start,end,increment/decrement` 

## Math 

- Division is decimal by default  `print(5/2) ➡️ 2.5`

- Double slash rounds down `print(5//2) ➡️ 2`

- negative number will round down `print(-3//2) ➡️ -2`

- A workaround for rounding towards zero is to use decimal division and then convert to int `print(int(-3/2)) ➡️ -1`

- Modding is similar to most languages

  - `print(10%3) ➡️ 1 `

  - except for negative values `print(-10%3) ➡️ 2`

  - To be consistent with other language modulo

    ```
     import math
     print(math.fmod(-10,3))
     # -1
    ```

- More Math helpers 

  ```python
  import math
  print(math.floor(3/2)) ➡️ 1
  print(math.ceil(3/2)) ➡️ 2
  print(math.sqrt(2)) ➡️ 1.414
  print(math.pow(2,3)) ➡️ 8.0
  ```

- Python numbers 

  - Max/Min Int

    ```
     float("inf")
     float("-inf")
    ```

    

  - Python numbers are infinite so they never overflow 

    ```python
    import math
    print(math.pow(2,200)) ➡️ 1.6069380442589903e+60
    
    ```

  - But still less than infinity 

    ```python
    import math
    print(math.pow(2,200)) ➡️ 1.6069380442589903e+60
    print(math.pow(2,200)<float("inf"))
    ```


## Arrays 

- called lists in python 

  ```python
  arr =[1,2,3]
  print(arr)
  ```

- Can be used as a stack

  ```python
  arr=[1,2,3]
  arr.append(4)
  arr.append(5)
  print(arr)
  
  # [1,2,3,4,5]
  
  arr.pop()
  print(arr)
  #[1,2,3,4]
  arr.insert(1,7) # O(n)
  print(arr)
  #[1, 7, 2, 3, 4] 
  arr[0] = 0
  arr[3] = 0
  print(arr)
  
  # [0, 7, 2, 0, 4]
  ```

- Initialize arr of size n with default value of 1

  ```python
  n=5
  arr = [1]*n
  print(arr)
  #[1,1,1,1,1]
  
  ```

- length of an array 

  ```python
  n=5
  arr = [1]*n
  print(arr)
  #[1,1,1,1,1]
  print(len(arr))
  # 5
  ```

- Negative index on arrays 

- ```python
  arr =[1,2,3,4,5]
  print(arr[-1])
  # 5
  print(arr[-2])
  # 4
  ```

- Sublists

  ```python
  arr =[1,2,3,4,5]
  print(arr[1:3])
  # [2,3]
  print(arr[0:5])
  #[1,2,3,4,5]
  ```

- Unpacking 

- ```python
  a,b,c =[1,2,4]
  #print(a,b,c)
  # 1,2,3
  # should match the number of elements on the left side and right side of the array
  # a,b,c=[1,2] ❌
  ```

- Loop through arrays  

  ```python
  nums = [1,2,3]
  # using index
  for i in range(len(nums)):
      print(nums[i])
  # 1 2 3
  
  # without using index
  for n in nums:
    print(n)
  #1 2 3
  
  #with index and value 
  for i,n in enumerate(nums):
    print(i,n)
  # 0 1 , 1 2 , 2 3
  
  #Loop through multiple arrays simultenously with unpacking
  nums1 = [1,3,5]
  nums2 = [2,4,6]
  
  for n1,n2 in zip(nums1,nums2):
    print(n1,n2)
    
  # 1 2 ,3 4 ,5 6
    
  
  
  ```

## Sorting 

- Sorting numbers 

- ```python
  arr =[5,4,7,3,8]
  arr.sort()
  print(arr)
  
  # [3, 4, 5, 7, 8]
  
  arr.sort(reverse = True)
  print(arr)
  
  # [8, 7, 5, 4, 3]
  ```

- Sorting Strings 

  ```python
  arr =["bob","alice","jane","doe"]
  arr.sort()
  print(arr)
  
  # ['alice', 'bob', 'doe', 'jane']
  
  # By default will be sorted in alphabetical order 
  
  #Custom Sort 
  arr.sort(key = lambda x:len(x))
  print(arr)
  
  # ['bob', 'doe', 'jane', 'alice']
  ```

## List Comprehension 

```python
arr =[i for i in range(5)]
print(arr)

# [0,1,2,3,4]

arr2 = [i+i for i in range(5) ]
print(arr2)

# [0,2,4,6,8]
```

## 2D Lists

```python
arr =[[0]*4 for i in range(4)]
print(arr)

# [[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]]
```

## Strings

- Strings are similar to arrays 

- ```python
  s="abc"
  print(s[0:2])
  #ab
  ```

- Strings are immutable so adding to a string creates a new string 

  ```python
  s="abc"
  s+="def"
  print(s)
  
  # "abcdef"
  ```

- Valid numeric strings can be converted , similarly numbers can be converted to strings 

- ```python
  print(int("123")+int("123"))
  
  # 246
  
  print(str(123)+str(123))
  
  # 123123
  ```

- In rare cases you may need the ASCII value of a char 

  ```python
  print(ord("a"))
  
  # 97
  
  print(ord("b"))
  
  # 98
  ```

## Queue

```python
from collections import deque

queue = deque()
queue.append(1)
queue.append(2)
print(queue)
queue.popleft() # O(1)
print(queue)
 
queue.appendleft(1)
print(queue)

queue.pop()
print(queue)
```

## HashSet

```python
mySet = set()
# no duplicates
mySet.add(1)
mySet.add(2)
print(mySet)

print(len(mySet))
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

## HashMap(aka dict)

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

## Tuples

- Tuples are like arrays but immutable 

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

## Heaps