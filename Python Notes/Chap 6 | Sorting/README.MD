# Sorting

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

## 