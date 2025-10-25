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