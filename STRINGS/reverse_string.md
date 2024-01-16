[REVERSE STRING:](https://leetcode.com/problems/reverse-string/description/)

```c++

class Solution {
public:
    void reverseString(vector<char>& s) {
        int st = 0 , e = s.size()-1;
        while(st<=e){
            swap(s[st++], s[e--]);
        }
       
    }
};
