[SEARCH A 2D MATRIX - II:](https://leetcode.com/problems/search-a-2d-matrix-ii/)

```c++

class Solution {
public:
    bool searchMatrix(vector<vector<int>>& matrix, int target) {
        int row = matrix.size();
        int col = matrix[0].size();

        int rowIndex = 0;
        int colIndex = col - 1; //taking last col no as mid val

        while ( rowIndex < row and colIndex >= 0){
            int element = matrix[rowIndex][colIndex];

            if ( element == target){
                return 1;
            }
            if (element < target){
                rowIndex++;
            }
            else {
                colIndex--;
            }
        }
        return 0;   
    }
};
