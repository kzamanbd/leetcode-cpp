# 1287. Element Appearing More Than 25% In Sorted Array

## Problem: <https://leetcode.com/problems/element-appearing-more-than-25-in-sorted-array/description/>

## ✅ output is 6

```cpp
int findSpecialInteger(vector<int> &arr)
{
    int size = arr.size();
    int count = 1;
    int element = arr[0];
    for (int i = 0; i < arr.size(); i++)
    {
        if (arr[i] == element)
        {
            count++;
        }
        else
        {
            count = 1;
        }
        if (count > size / 4)
        {
            return arr[i];
        }
        element = arr[i];
    }

    return element;
}
```

## Input

```cpp
vector<int> v = {1, 2, 2, 6, 6, 6, 6, 7, 10};
int result = findSpecialInteger(v);
cout << result;

// output is 6

```
