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

  