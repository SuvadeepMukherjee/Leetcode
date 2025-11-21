# Chap 1 | Theory

## Arrays

- arrays are dynamic in js 
- arrays are mutable in js 

## Mutable vs Immutable

- Mutable 
  - a type of data that can be changed
- Immutable
  - a type of data that cannot be changed

## Strings

- Strings are immutable in js 

## Why should we care whether something is mutable or immutable ? 

- lets say we have a mutable array `arr = [a,b,c]` and an immutable string `s = "abc"` and we want to change c into a d .We can easily do `arr[2]= d` but we cannot do `s[2]= "d"`
- As such if we wanted the string `abd` we need to create it entirely from scratch 
- So creating new versions just to modify one character is  very expensive and has  a time complexity of `O(n)`

## Time Complexity of various operations in arrays and strings 

| Operation                  | Array                   | String |
| -------------------------- | ----------------------- | ------ |
| Appending to end           | * O(1) (amortized O(1)) | O(n)   |
| Popping from end           | O(1)                    | O(n)   |
| Insertion , not from end   | O(n)                    | O(n)   |
| Deletion , not from end    | O(n)                    | O(n)   |
| Modifying an element       | O(1)                    | O(n)   |
| Random Access              | O(1)                    | O(1)   |
| Checking if element exists | O(n)                    | O(n)   |

amortized O(1) ➡️ Even though a single operation might occassionally take longer (like when the internal array needs to grow and allocate more memory  ) the average cost per operation over many operations remains constant time 