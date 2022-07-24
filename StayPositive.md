**Problem**:

  Given an array of integers nums, you start with an initial positive value startValue.
  In each iteration, you calculate the step by step sum of startValue plus elements in nums (from left to right).
  Return the minimum positive value of startValue such that the step by step sum is never less than 1.

**Input**:-

arr = [-3,2,-3,4,2]

**Output**:- 

5

**Exaplination** :-

The minimum value ans can have is 1 and for that, we need to loop over the running sum throughtout the array and
store the minimum value of it at any point.This tells us the minimum value that the running sum will have at any point.

**Code:-**

```python
def minStar(arr):
  summation = 0
  ans = 0
  for ele in arr:
    summation +=ans
    ans = min(summation,ans)
  return -ans + 1 
```
