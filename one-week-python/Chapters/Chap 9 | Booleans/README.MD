# Chap 9 | Booleans

## Booleans

------

- Booleans are another basic Python type.There are only 2 possible values: `True` and `False`

Note ➡️ Notice the capitalisation

## Comparision Operators

------

`>` ➡️ Greater than

`<` ➡️ Less Than

`>=` ➡️ Greater Than or Equal To

`<=` ➡️ Less Than or Equal to

a>b ➡️ Truthy if a is greater than b 

a<b ➡️ Truthy if a is less than b

a>=b ➡️ Truthy if a is greater than or equal to b

a <=b ➡️ Truthy if a is less than or equal to b

## Equality Operators

------

== ➡️ Equal to 

!= ➡️ Not Equal to 

**Identity**

- `is` ➡️ Evaluates to true if a and b both refer to the same object in memory 
- `is not` ➡️ Evaluates to True if a and b do NOT refer to the same object in memory

## Truthiness & Falsyness

------

- Every value is inherently Truth-y or False-y in python
- False-y 
  - False
  - 0.0
  - 0 
  - None
  - range(0)
  - Empty Strings
  - Empty Data Structures
- Truthy
  - Everything Else!

## in

------

- The "in" operator looks to see if an items is a member of a sequence .Soon we'll see other sequence types 



> "a" in "bat"
>
> True 

## ord()

------

- Python uses Unicode for encoding characters used in the string data type .The function ord() will return the number for any characters 

ord('a') ➡️ 97

ord("A") ➡️ 65