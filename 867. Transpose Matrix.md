# 867. Transpose Matrix

## Problem <https://leetcode.com/problems/transpose-matrix>

## ✅ output is [[1,4,7],[2,5,8],[3,6,9]]

```cpp
void transpose(vector<vector<int>> &matrix) {
    int rows = matrix.size();
    int cols = matrix[0].size();

    vector<vector<int>> matrix2;
    for (int i = 0; i < cols; i++)
    {
        vector<int> v;
        for (int j = 0; j < rows; j++)
        {
            v.push_back(matrix[j][i]);
        }
        matrix2.push_back(v);
        v.clear();
    }

    for (int i = 0; i < cols; i++)
    {
        for (int j = 0; j < rows; j++)
        {
            cout << matrix2[i][j] << " ";
        }
        cout << endl;
    }

}

// Example 1:
// Input: matrix = [[1,2,3],[4,5,6],[7,8,9]]
// Output: [[1,4,7],[2,5,8],[3,6,9]]

// Example 2:
// Input: matrix = [[1,2,3],[4,5,6]]
// Output: [[1,4],[2,5],[3,6]]
```
