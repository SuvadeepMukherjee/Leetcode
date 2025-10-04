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

------

## Exponents

- To use exponents we use the following operator **

  ```python
  # 2 to the 10th power, or 1024
  print(2 ** 10)
  ```

------

## Modulo

- The modulo operator is indicated by `%` and gives the remainder of a division calculation. If the two numbers are  divisible, then the result of the modulo operation will be 0.

  ```python
  # Prints 4 because 29 / 5 is 5 with a remainder of 4
  print(29 % 5)
  ```

------

## Concatenation

- The `+` operator doesn’t just add two numbers, it can also “add” two strings! The process of combining two strings is called string concatenation

------

## Plus Equals

- Python offers a shorthand for updating variables .When you have a number saved in a variable and want to add to the current value of the variable we can use the += operator

------

## Multi-line Strings 

- By using three quote-marks (`"""` or `'''`) instead of one, we tell the program that the string doesn’t end until the next triple-quote

------

## User Input

- While we output a variable’s value using `print()`, we assign information to a variable using `input()`. The `input()` function requires a prompt message, which it will print out for the user before they enter the new information. For example:

  ```python
  likes_snakes = input("Do you like snakes? ")
  ```

  