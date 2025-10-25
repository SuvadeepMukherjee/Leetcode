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

    