# Chap 1 | Theory

**Q1**: Fill in the blanks 

arrays are ___ (dynamic/static) and ______ (mutable/immutable)  in JS 

**Solution**:

arrays are dynamic and mutable in JS 

**Q2**: Explain mutable vs immutable ? 

**Solution**:

Mutable ➡️ a type of data that can be changed

Immutable ➡️ a type of data that cannot be changed

**Q3**: Why should we care about something being mutable or immutable in JS ? 

**Solution**:

Lets say we have a mutable array `arr = ['a','b','c']` and an immutable string s ="abc" and we want to change c into a d .We can easily do arr[2] = d but we cannot do s[2] = 'd' .As such if we wanted the string s='abd' we need to create it entirely from scratch .So creating new versions just to modify one character is very expensive and has a time complexity of O(n)

**Q4**: Are strings immutable in JS ?
**Solution**:

Strings are immutable in JS 

**Q5**: Explain amortized O(1)

**Solution**:

- Even though a single operation might occasionally take longer (like when the internal array needs to grow and allocate more memory) the average cost per operation over many operations remain constant time 
- appending to the end of an array is amortized O(1) in JS 

**Q6**: Arrat and String Time Complexity of various operations

**Solution**:



| Operation                  | Array          | String |
| -------------------------- | -------------- | ------ |
| Appending to end           | amortized O(1) | O(n)   |
| Popping from end           | O(1)           | O(n)   |
| Insertion, not from end    | O(n)           | O(n)   |
| Deletion , not from end    | O(n)           | O(n)   |
| Modifying an element       | O(1)           | O(n)   |
| Random access              | O(1)           | O(1)   |
| Checking if element exists | O(n)           | O(n)   |

