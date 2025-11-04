# Arrays

- called lists in python 

  ```python
  arr =[1,2,3]
  print(arr)
  ```

- Can be used as a stack

  ```python
  arr=[1,2,3]
  # append => add to end
  # Time Complexity of append is O(1)
  arr.append(4)
  arr.append(5)
  print(arr)
  
  # [1,2,3,4,5]
  # pop => remove from end
  arr.pop()
  print(arr)
  #[1,2,3,4]
  # insert => insert at a specific position
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

## 