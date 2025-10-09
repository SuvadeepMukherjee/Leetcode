# Chap 5 | Strings Basics

## Strings

---

- Strings are a textual datatype and must be wrapped in quotes

  ```python
  first_name = "Suvadeep"
  #str
  print(type(first_name))
  ```

## Variables are Dynamic Typed

---

- In Python variables are dynamic typed

- ```python
  age = 85
  age ="eighty five"
  ```

## Concatenation

---

- We can concatenate strings together by using the plus sign

## Multiplication

---

- We can also multiply a string by a number which will repeat that string

- ```python
  print("ha"*4)

  # "hahahaha"

  print(3*"hi)

  # "hihihi"
  ```

## String Indexing

---

- Strings are 0 indexed

- The last character has an index of -1 , the left of last -2 and so on -3,-4,-5 ,....

  ```python
  msg ="I <3 Cats"

  print(msg[0])

  # I

  print("first_name[99]")

  # String index out of range
  ```

## None

---

- None is a special value in Python that denotes the lack of value .It is not the same as zero or an empty string (those are still values)

  ```python
  print(type(None))

  #NoneType
  ```
