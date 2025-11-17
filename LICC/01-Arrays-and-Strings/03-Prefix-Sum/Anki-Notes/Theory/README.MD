# Prefix Sum Theoretical Notes

**Q**:What is the sum of subarray from i to j (inclusive) and what is the time complexity of the operation ? 

**Solution**:

- Sum of subarray from i to j (inclusive) is `prefix[j] - prefix[i]+ nums[i]`
- Sum of subarray from i to j (inclusive) is `prefix[j]- prefix[i-1]`

Time Complexity : O(1)

**Q**:Write the code to build a prefix sum and what is the time complexity to build a prefix sum  ?

**Solution**:

```js
let prefix = [nums[0]];

for (let i = 1; i < nums.length; i++) {
  prefix.push(nums[i] + prefix[prefix.length - 1]);
}
```

Time Complexity : O(n)