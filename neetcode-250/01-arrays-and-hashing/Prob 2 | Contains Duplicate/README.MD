# Contains Duplicate

Question can be found [here](https://leetcode.com/problems/contains-duplicate/description/)

**Solution**:

```python
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        hashset = set()
        for n in nums:
            if n in hashset:
                return True
            hashset.add(n)
        return False 
```

---

**Time & Space Complexity**:

Time Complexity: `O(n)` — we go through each element once, and checking or adding in a set takes `O(1)` on average.

Space Complexity: `O(n)` — in the worst case (no duplicates), we store all elements in the set.