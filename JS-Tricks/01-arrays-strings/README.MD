# Arrays and Strings

**Q1**:Create a matrix with 2 rows and 3 columns ? 

resultingMatrix ➡️ `[[0,0,0],[0,0]]`

**Solution**:

```js
const grid = Array.from({length:2},()=>Array(3).fill(0))

Console.log(grid)
```