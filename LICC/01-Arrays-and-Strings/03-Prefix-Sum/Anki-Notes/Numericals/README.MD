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



