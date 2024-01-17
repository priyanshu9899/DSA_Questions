[ROTATE ARRAYS:](https://leetcode.com/problems/rotate-array/)

```c++

class Solution {
public:
    void rotate(vector<int>& nums, int k) {
        vector <int> temp (nums.size());
        for (int i = 0 ; i < nums.size() ; i++){
            if (nums[i] == k){
                for (int j = i; j < nums.size(); j++){
                    nums[j]=temp[j+1];
                }
            }
        }
        nums = temp;
    }
};
