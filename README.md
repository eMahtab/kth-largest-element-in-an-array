# kth-largest-element-in-an-array
## https://leetcode.com/problems/kth-largest-element-in-an-array

Find the kth largest element in an unsorted array. Note that it is the kth largest element in the sorted order, not the kth distinct element.

Example 1:

Input: [3,2,1,5,6,4] and k = 2
Output: 5

Example 2:

Input: [3,2,3,1,2,4,5,5,6] and k = 4
Output: 4

**Note: You may assume k is always valid, 1 ≤ k ≤ array's length.**

## Implementation : Sorting

```java
class Solution {
    public int findKthLargest(int[] nums, int k) {
        Arrays.sort(nums);
        int kthLargest = 0;
        for(int i = nums.length-1; k > 0; i--){
            kthLargest = nums[i];
            k--;
        }
        return kthLargest;
    }
}
```

