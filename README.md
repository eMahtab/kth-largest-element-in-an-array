# kth-largest-element-in-an-array
## https://leetcode.com/problems/kth-largest-element-in-an-array

Find the kth largest element in an unsorted array. Note that it is the kth largest element in the sorted order, not the kth distinct element.
```
Example 1:

Input: [3,2,1,5,6,4] and k = 2
Output: 5

Example 2:

Input: [3,2,3,1,2,4,5,5,6] and k = 4
Output: 4
```
**Note: You may assume k is always valid, 1 ≤ k ≤ array's length.**

## Implementation 1 : Sorting

```java
class Solution {
    public int findKthLargest(int[] nums, int k) {
        Arrays.sort(nums);
        return nums[nums.length - k];
    }
}
```
## Implementation 2 : Heap

```java
class Solution {
    public int findKthLargest(int[] nums, int k) {
       PriorityQueue<Integer> heap = new PriorityQueue<Integer>();
        // just keep k largest elements in the min heap
	        for (int n: nums) {
	          heap.add(n);
	          if (heap.size() > k)
	            heap.poll();
	        }
        
	   return heap.poll();    
    }
}
```

# References :
https://www.youtube.com/watch?v=3d0ORD8Qnk8
