# Classes

```python
class myClass:
	#Constructor
  def __init__(self,nums):
    self.nums = nums
    self.size = len(nums)
    
  #self keyword required as param
  def getLength(self):
    return self.size
  
  def getDoubleLength(self):
    return 2 * self.getLength()
    
```

