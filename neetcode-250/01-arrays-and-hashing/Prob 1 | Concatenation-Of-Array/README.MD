## Concatenation of Array 

Problem can be found [here](https://leetcode.com/problems/concatenation-of-array/description/)

**Solution**:

```python
class Solution:
    def getConcatenation(self, nums: List[int]) -> List[int]:
        ans =[]
        for i in range(2):
            for n in nums:
                ans.append(n)
        return ans
```

---

**Time and Space Complexity**:

Time Complexity: `O(n)` — we loop through the list twice (2 × n operations). Each `append()` is O(1).

Space Complexity: `O(n)` — we create a new list `ans` that holds twice the elements of `nums`.