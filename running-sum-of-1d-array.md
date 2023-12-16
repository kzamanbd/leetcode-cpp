# 1480. Running Sum of 1d Array

## Problem <https://leetcode.com/problems/running-sum-of-1d-array>

```cpp
vector<int> runningSum(vector<int>& nums) {
    for (int i = 0; i < nums.size(); i++) {
        nums[i] = i == 0 ? nums[i] : nums[i] + nums[i - 1];
    }

    return nums;
}
```

## Input

```cpp
vector<int> v = {1, 2, 3, 4};
vector<int> result = runningSum(v);
for (int i = 0; i < result.size(); i++) {
    cout << result[i] << " ";
}
// Input: nums = [1,2,3,4]
// Output: [1,3,6,10]
// Explanation: Running sum is obtained as follows: [1, 1+2, 1+2+3, 1+2+3+4].
```
