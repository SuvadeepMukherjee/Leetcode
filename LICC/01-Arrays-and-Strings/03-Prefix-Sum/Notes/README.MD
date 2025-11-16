# Prefix Sum 

prefix[i] is the sum of all elements up to the index i .For example given `nums=[5,2,1,6,3,8]` we would have `prefix = [5,7,8,14,17,25]`

Prefix sum allow us to find the sum of any subarray in O(1). Sum of the subarray from i to j (inclusive) is `prefix[j]-prefix[i]+nums[i]`

Building a prefix sum : 

```js
let prefix = [nums[0]];

for (let i = 1; i < nums.length; i++) {
  prefix.push(nums[i] + prefix[prefix.length - 1]);
}
```

