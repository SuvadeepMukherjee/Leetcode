# Arrays and Strings

**Q1**:Create a matrix with 2 rows and 3 columns ? 

resultingMatrix ➡️ `[[0,0,0],[0,0]]`

**Solution**:

```js
const grid = Array.from({length:2},()=>Array(3).fill(0))

Console.log(grid)
```

**Q2**:What will be the output  ? 

```js
let arr =[2,3]

const result =  arr.push(1)
console.log(result)
console.log(arr)
```

**Solution**:

`arr.push(1)`  will append the element at the end of the array , it will return the new length of the array so the result will be the following : `3 , [ 2, 3, 1 ]`