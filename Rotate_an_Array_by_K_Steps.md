# Rotate An Array by K Steps

## Problem <https://leetcode.com/problems/rotate-array>

## ✅ output is [5, 6, 7, 1, 2, 3, 4]

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{

    int n;
    cin >> n;
    int arr[n];
    for (int i = 0; i < n; i++)
    {
        cin >> arr[i];
    }

    int k;
    cin >> k;

    while (k > 0)
    {
        int j = 0;
        int last = arr[n - 1];
        for (j = n - 1; j > 0; j--)
        {
            arr[j] = arr[j - 1];
        }
        arr[j] = last;
        k--;
    }

    for (int i = 0; i < n; i++)
    {
        cout << arr[i] << " ";
    }
    return 0;
}
```
