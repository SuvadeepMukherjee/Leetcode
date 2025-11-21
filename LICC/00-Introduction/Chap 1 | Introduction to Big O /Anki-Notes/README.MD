# Chap 1 | Big 0 

Anki 🏷️ 01-bigO

**Q1**:How do we calculate time and space complexity ?

**Solution**:

- Time and Space Complexity is defined by a function
- The variables are defined by us and they represent values that change between different inputs (like say the length of an array or string)
- Time and Space Complexity calculates how much more time or space our algorithm takes relative to input size
- Rules 
  - We ignore constants
  - We consider the complexity as the variables tend to infinity

**Q2**:What do you mean by O(1) space or time complexity ? 

**Solution**:

- It means the algorithm always uses the same amount of resources regardless of input size and is the fastest possible

**Q3**: Analyze the time complexity 

Given an integer array "arr" with length n 

```js
for(let i =0;i<arr.length;i++){
    console.log(i)
}
```

**Solution**:

- console logs cost O(1)
- for loop iterates n times

Time : O(n)

**Q4**: Analyze the time complexity ?

Given an integer array "arr" with length n 

```js
for(let i =0 ; i < arr.length;i++){
    for(let j=0;j<500000;j++){
        console.log(i)
    }
}
```

**Solution**:

- print costs O(1)
- inner for loop iterates 500,000 times ➡️ O(1)
- outer for loop iterates n times ➡️ O(n)

Time : O(n)

**Q5**:Given an integer array "arr" with length n 

```js
for(let i =0; i<arr.length;i++){
    for(let j =0;j<arr.length;j++){
        console.log(i*j)
    }
}
```

**Solution**:

- Multiplication cost O(1)
- Print costs O(1)
- inner for loop n times for each iteration of outer for loop (n times)

Time : O(n)

**Q6**: Given integer arrays "arr" with length n and "arr2" with length m 

```js
for(let i=0;i<arr.length;i++){
    console.log(i)
}

for(let i=0;i<arr.length;i++){
    console.log(i)
}

for(let j =0;j<arr2.length;j++){
    console.log(j)
}
```

**Solution**:

- First 2 loops : O(n)
- Final for loop : O(m)

Time :O(2n+m) = O(n+m)

**Q7**:Given an integer array "arr" with length n 

```js
for(let i=0;i<arr.length;i++){
    for(let j=i;j<arr.length;j++){
        console.log(arr[i]+arr[j])
    }
}
```

**Solution**:

- inner for loop is dependent on what iteration the outer for loop is currently on 
- Total iterations : 1+2+3+4+....+n =n*(n+1)/2 =(n^2 + n)/2 

Time Complexity : O(n^2)

**Q8**: Explain logarithmic time ? 

**Solution**:

- Somewhere in our algorithm the input is being reduced by a percentage at every step (in binary search input is halved at every step)
- O(logn) ➡️very very fast

**Q9**: In space complexity are the following true ? 

- We dont count the space used by the input 
- We dont count the space used by the output

**Solution**:

- We dont count the space used by the input
- We dont count the space used by the output 

**Q10**: Find the space complexity ? 

Given an integer array "arr" with length n 

```js
for(let i=0;i<arr.length;i++){
    console.log(i)
}
```

**Solution**:

Space : O(1)

**Q11**: Find the space Complexity ? 

Given an integer array "arr" with length n 

```js
let arr =[]
for(let i=0;i<arr.length;i++){
    arr.push(i*2)
}
```

**Solution**:

Space : O(n)

**Q12**: Find the space complexity ? 

Given an integer array "arr" with length n 

```js
let nums = []
let oneHundreth = n/100
for(let i=0;i<oneHundreth;i++){
    nums.push(arr[i])
}
```

**Solution**:

- Array nums stores the first 1% of numbers in arr 
- Space Complexity : O(n/100) =O(n)

**Q13**: Find the space Complexity ? 

Given 2 arrays arr and arr1 

```js
const n = arr.length
const m = arr2.length

const grid = Array.from({length:n},()=>Array(m).fill(0))

for(let i =0 ; i<n;i++){
    for(let j =0;j<m;j++){
        grid[i][j] = arr[i] * arr2[j]
    }
}
```

**Solution**:

Space : O(n*m)