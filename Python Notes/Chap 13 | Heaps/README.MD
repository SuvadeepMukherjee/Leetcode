# Heaps

```python
import heapq
minHeap =[]
heapq.heappush(minHeap,3)
heapq.heappush(minHeap,2)
heapq.heappush(minHeap,4)

# min is always at index 0
print(minHeap[0])

while len(minHeap):
    print(heapq.heappop(minHeap))

# No max heap by default , work around is min heap and multiply by -1 when push and pop 

maxHeap =[]
heapq.heappush(maxHeap, -3)
heapq.heappush(maxHeap,-2)
heapq.heappush(maxHeap,-4)

# max is always at index 0
print(-1 * maxHeap[0])

while len(maxHeap):
    print(-1 * heapq.heappop(maxHeap))
    
# Build heap from initial values
arr =[2,1,8,4,5]
heapq.heapify(arr) # O(1)
```

