# Sliding Window

## Subarray 

- a contiguous section of an array can be described by a left and right bound![subarray](../../assets/subarray.png)

## Valid SubArrays 

A common pattern you'll see in array problems involves the idea of a  "valid" subarray. The problem description will either explicitly or  implicitly define what makes a subarray "valid". We can split it into  two parts:

1. A constraint metric. This is an attribute of a subarray.   - For example, the sum of the subarray, the number of unique  elements in the subarray, the frequency of a specific element, etc.
2. A numeric restriction on the constraint metric.

For example, let's say a problem declares a subarray is valid if it has a sum less than or equal to `10`. The constraint metric here is the sum of the subarray, and the numeric restriction is `<= 10`. A subarray is considered valid if its constraint metric conforms to the numeric restriction, i.e., the sum is less than or equal to `10`.