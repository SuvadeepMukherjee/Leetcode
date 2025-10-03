# Hello World

------

## Comments

- Python interprets anything after a # as a comment

  ```python
  #This variable will be used to count the number of times anyone tweets the word persnickety
  
  persnickety_count = 0 
  ```

------

## Print

- In Python the print() function is used to tell a computer to talk 

- The message to be printed should be surrounded by quotes

  ```python
  #from Mary Shelley's Frankenstein
  
  print("There is something at work in my soul , which i do not understand")
  ```

------

## Strings

- In Python a string is either surrounded by double quotes("Hello world!") or single quotes('Hello world!')
- It doesn't matter which kind we use , but we need to be consistent with one

------

## Variables

- In Python we assign variables by using the equals sign

  ```python
  message_string = "Hello there"
  ```

------

## Errors

- Two common errors that we encounter while writing Python are `SyntaxError` and `NameError`.
  - `SyntaxError` means there is something  wrong with the way your program is written — punctuation that does not  belong, a command where it is not expected, or a missing parenthesis can all trigger a `SyntaxError`.
  - A `NameError` occurs when the Python  interpreter sees a word it does not recognize. Code that contains  something that looks like a variable but was never defined will throw a `NameError`

------

## Numbers

- An *integer*, or `int`, is a whole number. It has no decimal point and contains all counting  numbers (1, 2, 3, …) as well as their negative counterparts and the  number 0.
- A *floating-point number*, or a `float`, is a decimal number.

------

## Calculations

- Python performs the arithmetic operations of addition, subtraction, multiplication, and division with `+`, `-`, `*`, and `/`.
- Python converts all `int`'s to `float`s before performing division
- Division can throw its own special error: `ZeroDivisionError`. Python will raise this error when attempting to divide by 0.

------

## Changing Numbers

- Performing arithmetic on variables does not change the variable - you can only update a variable using the = sign