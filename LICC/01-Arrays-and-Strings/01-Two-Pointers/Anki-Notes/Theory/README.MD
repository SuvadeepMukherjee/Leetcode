# Two Pointers

**Q**:Convert this algorithm to pseudocode 

"Start the pointers at the edges of the input .Move them towards each other until they meet"

What will be the Time Complexity of the algorithm ? 

**Solution**:

```js
function fn(arr) {
    let left = 0;
    let right = arr.length - 1;

    while (left < right) {
			Do Some Logic here depending on the problem 
      Do Some more Logic here to decide one of the following:
				1.Left++
      	2.Right--
      	3.Both Left++ and Right--
    }

    
}

```

Time Complexity : We will never have more than O(n) iterations for the while loop because the pointers start n away from each other and move at least one step closer in every  iteration. Therefore, if we can keep the work inside each iteration at O(1)O(1), this technique will result in a linear runtime, which is usually the best possible runtime.

**Q**:Convert this algorithm to pseudocode 

Problem has 2 iterables in the input , for example 2 arrays 

"Move along both inputs simultenously until all elements have been checked"

**Solution**:

```js
function fn(arr1, arr2) {
    let i = 0;
    let j = 0;

    while (i < arr1.length && j < arr2.length) {
        // Do some logic here depending on the problem
        // Do some more logic here to decide on one of the following:
        // 1. i++
        // 2. j++
        // 3. Both i++ and j++
    }

    // Step 4: make sure both iterables are exhausted
    // Note that only one of these loops would run
    while (i < arr1.length) {
        // Do some logic here depending on the problem
        i++;
    }

    while (j < arr2.length) {
        // Do some logic here depending on the problem
        j++;
    }
}

```

Time Complexity : Similar to the first method we looked at, this method will have a linear time complexity of O(n+m) if the work inside the while loop is O(1), where `n = arr1.length` and `m = arr2.length`. This is because at every iteration, we move at least one pointer forward, and the pointers cannot be moved forward more than `n + m` times without the arrays being exhausted.