# kth-largest-element-in-an-array
## https://leetcode.com/problems/kth-largest-element-in-an-array


# Implementation : Sorting

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

