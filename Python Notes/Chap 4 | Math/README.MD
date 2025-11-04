# Math

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


## 