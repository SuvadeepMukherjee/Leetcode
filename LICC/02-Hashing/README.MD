# Hashing 

## Data Structures

- A data structure is a format for organizing data in an efficient way 
- We can split data structures into things : interface and the implementation 
- Interface is like a contract that specifies how we can interact with the data structure for example if we want to append an element to the end of a dynamic array we use the built in `.push()` method 
- Implementation is the code that actually makes the data structure work 

## Hash Function 

-  A hash function is a function that takes an input and deterministically  converts it to an integer that is less than a fixed size set by the  programmer. Inputs are called **keys** and the same input will always be converted to the same integer.

## Hash Maps

- A hash function converts any key into an integer 
- This lets us use an array's O(1) access even when the index isnt a number 
- Combining a hash function with an array gives us a map
- maps store key-value pairs 
- maps allow :
  - O(1) insert 
  - O(1) delete 
  - O(1) update
  - O(1) lookup 
-  maps are ordered - iteration guarantee insertion order