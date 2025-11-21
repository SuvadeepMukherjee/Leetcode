# Recursion Anki Notes

Anki ➡️ 02-recursion 

**Q1**:Print from 1 ➡️ 3 using recursion and draw the recursion tree

**Solution**:

```js
function printFn(i){
    if(i > 3) return 
    console.log(i)
    printFn(i+1)
    return
}

printFn(1)
```

**Q2**:Write the code for fibonacci series using recursion and draw the recursion tree 

**Solution**:

```js
function fibonacci(i){
    if(i<=1) return i;
    let oneBack = fibonacci(i-1);
    let twoBack = fibonacci(i-2);
    return oneBack + twoBack 
}

console.log(fibonacci(5))
```

**Q3**:Draw the recursion tree and tell what will be logged to the console ? 

```js
function printFn(i){
    if(i > 3) return 
    console.log(i)
    printFn(i+1)
    console.log(`End of call where i =${i}`)
    return
}

printFn(1)
```

**Solution**:

The following will be logged to the console ➡️

`1, 2 , 3 , End of call where i =3 , End of call where i = 2 , End of call where i =1`  
