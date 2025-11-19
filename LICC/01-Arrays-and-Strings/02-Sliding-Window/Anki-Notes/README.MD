# Sliding Window 

Tag 🏷️Anki 

**Q**:What is a Subarray ? 

**Solution**:

A subarray is a contiguous section of an arary which can be described by a left and right bound

![subarray](../../assets/subarray.png)

**Q**:What does the term "valid subarray" mean in array problems , and what two components define it ? 

**Solution**:

A “valid subarray” is one that meets a specific condition defined by the problem. It has two parts:

1. **Constraint metric** — an attribute of the subarray (e.g., sum, number of unique elements, frequency of an element).
2. **Numeric restriction** — a rule applied to that metric (e.g., sum ≤ 10).

A subarray is valid if its metric satisfies the restriction.

**Q**:Write the pseudocode for sliding window and its time complexity ? 

**Solution**:

```js
        
        
function fn(arr){
  let left = 0;
  for(let right = 0; right<arr.length;right++){
    // Do Some Logic to add elements at arr[right] to window
    
  }
  
  while (WINDOW_IS_INVALID){
    //Do some logic to remove element at arr[left] from window
    left++
  }
  Do some logic to update the answer
}
```

Time Complexity : O(n)

**Problem 1**:

Given an array of positive integers `nums` and an integer `k`, find the length of the longest subarray whose sum is less than or equal to `k`

```js
var findLength = function(nums, k) {
    
}

```

**Solution**:

```js
var findLength = function(nums, k) {
    // curr is the current sum of the window
    let left = 0, curr = 0, ans = 0;
    for (let right = 0; right < nums.length; right++) {
        curr += nums[right];
        while (curr > k) {
            curr -= nums[left];
            left++;
        }
        
        ans = Math.max(ans, right - left + 1);
    }
    
    return ans;
}
```

Time Complexity : O(n)

Space Complexity : O(1)

---

**Problem 2**:

You are given a binary string `s` (a string containing only `"0"` and `"1"`). You may choose up to one `"0"` and flip it to a `"1"`. What is the length of the longest substring achievable that contains only `"1"`?

For example, given `s = "1101100111"`, the answer is `5`. If you perform the flip at index `2`, the string becomes `1111100111`.

```js
var findLength = function(s) {
}
```

**Solution**:

```js
var findLength = function(s) {
    // curr is the current number of zeros in the window
    let left = 0, curr = 0, ans = 0;
    for (let right = 0; right < s.length; right++) {
        if (s[right] == "0") {
            curr++;
        }
        
        while (curr > 1) {
            if (s[left] == "0") {
                curr -= 1;
            }
            left++;
        }
        
        ans = Math.max(ans, right - left + 1);
    }
    
    return ans;
}
```

Time Complexity :O(n)

Space Complexity :O(1)

**Problem 3**:

[SubArray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/description/)

**Solution**:

```js
var numSubarrayProductLessThanK = function(nums, k) {
    if(k<=1)return 0;
    let left =0;
    let curr =1;
    let ans = 0;
    for(let right =0;right<nums.length;right++){
        curr*=nums[right];
        while(curr>=k){
            curr/=nums[left];
            left++;
        }
        ans += right - left +1;
    }
    return ans;
};
```

Time Complexity : O(n)

Space Complexity : O(1)
