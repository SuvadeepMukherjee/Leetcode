# Strings

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

## 