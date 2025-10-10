# Chap 6 | A Little Bit More On Strings

## String Slice

------

```python
str ="I <3 Cats"

print(str[2:6])

#"I <3 Cats"
```

Syntax is string[starting_index(inclusive),ending_index(exclusive)]

The resulting string is a new string , original string is unaffected

```python
animal = "catdog"

print(animal[2:4]) 

#td

print(animal[3;6])

#dog

print(animal[3:99])

#dog

print(animal[3:])

#dog

print(animal[0:3])

#cat

print(animal[:3])

#cat

str ="I <3 Cats"

print(str[2:8:2])

#< a
```

Syntax is starting_index(inclusive), ending_index(exclusive),step

if we omit starting_index it takes from begining , if we omit ending_index or give a ending_index far greater than total index it will go towards end 

## Escape Characters

------

- Newline `\n`
- Double Quote `\"`
- Tab `\t`
- Single quote `\'`
- Backslash `\\`