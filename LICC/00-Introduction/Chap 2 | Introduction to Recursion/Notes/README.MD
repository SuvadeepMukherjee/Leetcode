# Chap 2 | Recursion

## Recursion

- Recursion is implemented using a function that calls itself 

## Recursion to print from 1 to 3

- Code

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

## Recursion for Fibonacci

- Code

  ```js
  function fibonacci(i){
      if(i<=1) return i;
      let oneBack = fibonacci(i-1);
      let twoBack = fibonacci(i-2);
      return oneBack + twoBack 
  }
  
  console.log(fibonacci(5))
  ```

  