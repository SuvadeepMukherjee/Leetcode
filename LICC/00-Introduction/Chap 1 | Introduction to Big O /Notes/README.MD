# Introduction to Big O

## Algorithm

- Set of instructions that a computer will follow step-by-step to solve a problem
- Algorithms should be deterministic .Given the same input the algorithm should always produce the same output 
- The algorithm should be correct for any arbitrary valid input

## Big O

- Describes the computational compexity of an algorithm 
- The Computational Complexity of an algorithm is split into 2 parts
- Time Complexity 
  - As the input size grows how much longer does the algorithm  take to complete
- Space Complexity 
  - As the input size grows how much more memory does the algorithm use 

## How Complexity Works ?

- Complexity is defined by a function
- The variables are defined by us and represent values that *change between different inputs* and these values should affect the algorithm 
- Example ➡️ length of an input array or string

Note ➡️ When dealing with integers the larger the integer , the more time operations like addition , multiplication or printing will take .While this is relevant in theory we typically ignore this fact because the difference is practically very small and we treat all integers the same