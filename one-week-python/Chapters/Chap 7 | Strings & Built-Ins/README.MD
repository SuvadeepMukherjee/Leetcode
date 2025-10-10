# Chap 7 | Strings & Built-ins

## The len function

------

- The len() function will return the length of whatever item we pass to it 

```python
word = 'chicken'

print(len(word))

#7
```

## The input() Function

------

- The input() function will prompt a user to enter some input , converts it into a string and then returns it .We can use it to gather user input in our programs

- ```python
  age = input("how old are you ?")
  ```

## The type() function

------

- The type() function accepts an input object and will return the type of that object
  - `type("hi")` ➡️ `<class 'str'>`
  - `type(55)` ➡️ `<class 'int'>` 

## Casting Types

------

`int(12)` ➡️ `12`(integer)

`float("3.3")` ➡️ `3.3` (float)

`str(44.5)` ➡️ "44.5"

## f Strings

------

- f-Strings are an easy way to generate strings that contain interpolated expressions .Any code between curly braces{} will be evaluated and then the turned into a string and inserted into the overall string

`f"there are {24*60*60} seconds in a day"`  ➡️ "there are 86400 seconds in a day" 