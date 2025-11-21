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

## Calculating Complexity 

- Roughly our function calculates the number of operations or amount of memory (depending on if we are analyzing time or space complexity respectively) our algorithm consumes relative to the input size
- Time complexity is not meant to be an exact representation of the number of operations
- Rules
  - We ignore constants 
    -  O(9999n) =O(8n)=O(n)=O(n/500)
  - We consider the complexity as the variables tend to infinity 
    - O(2^n + n^2 - 500n) = O(2^n)
- The best complexity is O(1) called constant time or constant space .It means that the algorithm ALWAYS uses the same amount of resources regardless of input

## Analyzing Time Complexity 

Given an integer array "arr" with length n 

```js
for(let i=0;i<arr.length;i++){
    console.log(i)
} 
```

**Solution**:

- console log cost O(1)
- for loop iterates n times 

Time : O(n)

---

Given an integer array "arr" with length n 

```js
for(let i=0;i<arr.length;i++){
    for(let j=0;j<5000000;j++){
        console.log(i)
    }
    
}
```

**Solution**:

- console log cost O(1)
- inner loop iterates 500,000 times ➡️ O(1)
- outer for loop iterates n times ➡️ O(n)

Time Complexity : O(n)

---

Given an integer array "arr" with length n 

```js
for(let i=0;i<arr.length;i++){
    for(let j=0;j<arr.length;j++){
        console.log(i * j)
    }
    
}
```

**Solution**:

- multiplication : O(1)
- console log costs O(1)
- inner for loop iterates n times for each iteration of the outer for loop , outer for loop iterates n times

Time Complexity :O(n^2)

---

Given an integer array "arr" with length n and "arr2" with length m 

```js
for(let i=0;i<arr.length;i++){
    console.log(i)
}

for(let i=0;i<arr.length;i++ ){
    console.log(i)
}

for(let j=0;j<arr2.length;j++){
    console.log(j)
}
```

**Solution**:

- First 2 for loops : O(n)
- Final for loop : O(m)

Time Complexity : O(2n + m ) = O(n+m)

---

Given an integer array "arr" with length n 

```js
for(let i=0;i<arr.length;i++){
    for(let j=i;j<arr.length;j++){
        console.log(arr[i] + arr[j])
    }
}
```

**Solution**:

- inner for loop is dependent on what iteration the outer for loop is currently on 
  - first time - n 
  - second time - n-1
  - third  time - n-2 

- Total iteratons = 1+2+3 +4 +....+n = n(n+1)/2= (n^2 + n)/2

Time Complexity : O(n^2) 

## Logarithmic time 

- Somewhere in our algorithm the input is being reduced by a percentage at every step (in binary search input is halved at every time)
- O(log n) ➡️ very fast 💨

## Rules of  Space Complexity 

- We dont count the space used by the input 
- We dont count the space used by the output 

## Analyzing Space Complexity 

Given an integer array "arr" with length n 

```js
for(let i=0;i<arr.length;i++){
    console.log(i)
}
```

**Solution**:

Space : O(1)

---

Given an integer array with length n 

```js
let arr =[]
for(let i=0;i<arr.length;i++){
    arr.push(i*2)
} 
```

**Solution**:

Space : O(n)

---

Given an integer array "arr" with length n 

```js
let nums =[]
let oneHundreth = n/100
for(let i=0;i<oneHundreth ;i++){
    nums.push(arr[i])
}
```

**Solution**:

Array nums stores the first 1% of numbers in arr

Space Complexity : O(n/100)=O(n)

---

```js
const n = arr.length;
const m  = arr2.length
const grid = Array.from({length:n},()=>Array(m).fill(0))

for(let i=0;i<n;i++){
    for(let j=0;j<m;j++){
        grid[i][j] = arr[i]* arr2[j]
    }
}


```

Space Complexity :O(n*m)