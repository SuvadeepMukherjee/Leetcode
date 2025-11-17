# Problems 

**Problem 1**:

Given an integer array `nums`, an array `queries` where `queries[i] = [x, y]` and an integer `limit`, return a boolean array that represents the answer to each query. A query is `true` if the sum of the subarray from `x` to `y` is less than `limit`, or `false` otherwise.

For example, given `nums = [1, 6, 3, 2, 7, 2]`, `queries = [[0, 3], [2, 5], [2, 4]]`, and `limit = 13`, the answer is `[true, false, true]`. For each query, the subarray sums are `[12, 14, 12]`.

```js
var answerQueries = function(nums,queries,limit){
  
}
```



**Solution**:

```js
var answerQueries = function(nums, queries, limit) {
    let prefix = [nums[0]];
    for (let i = 1; i < nums.length; i++) {
        prefix.push(nums[i] + prefix[prefix.length - 1]);
    }
    
    let ans = [];
    for (const [x, y] of queries) {
        let curr = prefix[y] - prefix[x] + nums[x];
        ans.push(curr < limit);
    }
    
    return ans;
};
```

Time Complexity : O(n)

Space Complexity : O(n)

---

**Problem 2**:

[Number of Ways to split array](https://leetcode.com/problems/number-of-ways-to-split-array/description/)

**Solution**:

```js
var waysToSplitArray = function(nums) {
    let prefix =[nums[0]]
    let n = nums.length;
    for(let i=1;i<nums.length;i++){
        prefix.push(nums[i]+prefix[prefix.length-1])
    }
    let ans =0;
    for(let i=0;i<n-1;i++){
        let leftSection = prefix[i];
        let rightSection = prefix[n-1]-prefix[i+1] + nums[i+1];
        if(leftSection>=rightSection){
            ans++;
        }
    }
    return ans;

};
```

Time Complexity : O(n)

Space Complexity : O(n)

---

Problem 3 

[Running Sum of 1D Array](https://leetcode.com/problems/running-sum-of-1d-array/description/)

**Solution**:

```js
var runningSum = function(nums) {
    let prefix =[nums[0]];
    for(let i=1;i<nums.length;i++){
        prefix.push(nums[i]+prefix[prefix.length-1])
    }
    return prefix;
};
```

Time Complexity : O(n)

Space Complexity : O(n)

---

Problem 4 

[Minimum value to get positive step by step](https://leetcode.com/problems/minimum-value-to-get-positive-step-by-step-sum/description/)

**Solution**:

```js
ar minStartValue = function(nums) {
   let minVal =0;
    let total =0;
    for(let i=0;i<nums.length;i++){
        total+=nums[i];
        minVal =Math.min(minVal,total)
    }
    return 1-minVal
};
```

Time Complexity : O(n)

Space Complexity : O(n)

---

Problem 5 

[K radius Subarray Averages](https://leetcode.com/problems/k-radius-subarray-averages/description/)

**Solution**:

```js
var getAverages = function(nums, k) {
    // When a single element is considered then its average will be the number itself only.
    if (k === 0) {
        return nums;
    }
    
    const windowSize = 2 * k + 1
    const n = nums.length;
    const averages = new Array(n).fill(-1);

    // Any index will not have 'k' elements in its left and right.
    if (windowSize > n) {
        return averages;
    }

    
    prefix =[nums[0]];
    for(let i=1;i<nums.length;i++){
        prefix.push(nums[i]+prefix[prefix.length-1])
    }
    
    // We iterate only on those indices which have at least 'k' elements in their left and right.
    // i.e. indices from 'k' to 'n - k'
    for (let i = k; i < (n - k); i++) {
        const leftBound = i - k, rightBound = i + k;
        const subArraySum = prefix[rightBound ] - prefix[leftBound] + nums[leftBound];
        const average = Math.floor(subArraySum / windowSize);
        averages[i] = average;
    }

    return averages;
};
```



Time Complexity : O(n)

Space Complexity :O(n)

---

Problem 6

[Find the Highest Altitude](https://leetcode.com/problems/find-the-highest-altitude/description/)

**Solution**:

```js
var largestAltitude = function(gain) {
    let prefix = [0];
    for(let i=0;i<gain.length;i++){
        prefix.push(gain[i]+prefix[prefix.length-1])
    }

    let max = -Infinity;
    for(let i=0;i<prefix.length;i++){
        if(prefix[i]>max){
            max=prefix[i]
        }
    }
    return max;
};
```

Time Complexity : O(n)

Space Complexity : O(n)

---

Problem 7 

[Find the highest Altitude](https://leetcode.com/problems/find-the-highest-altitude/)

**Solution**:

```js
var largestAltitude = function(gain) {
    let prefix = [0];
    for(let i=0;i<gain.length;i++){
        prefix.push(gain[i]+prefix[prefix.length-1])
    }

    let max = -Infinity;
    for(let i=0;i<prefix.length;i++){
        if(prefix[i]>max){
            max=prefix[i]
        }
    }
    return max;
};
```

Time Complexity : O(n)

Space Complexity : O(n)

---

Problem 8 

[Find Pivot Index](https://leetcode.com/problems/find-pivot-index/description/)

**Solution**:

```js 
var pivotIndex = function(nums) {
    let prefix =[nums[0]];
    for(let i=1;i<nums.length;i++){
        prefix.push(nums[i]+prefix[prefix.length-1])
    }

    for(let i=0;i<nums.length;i++){
        let left = i === 0 ? 0 : prefix[i - 1];
        let right = prefix[nums.length-1]-prefix[i];
        if(left===right)return i
    }
    return -1;
};
```

Time Complexity : O(n)

Space Complexity : O(n)
