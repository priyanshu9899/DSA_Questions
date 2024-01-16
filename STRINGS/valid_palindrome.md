[VALID PAINDROME:](https://leetcode.com/problems/valid-palindrome/)

```c++

class Solution {
private:
    bool valid(char ch ) {
        if ( (ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z') || 
        (ch >= '0' && ch <='9')){
            return 1;
        }
        return 0;
    }

    char toLowerCase(char ch){
        if((ch >= 'a' && ch <= 'z') || (ch >= 0 && ch <=9))
        return ch;
        else {
            char temp = ch - 'A' + 'a';
            return temp;
        }
    }

     bool checkPalindrome(string s) {
        int st = 0, e = s.length()-1;
        for (int i = 0; i < s.size(); i++){
            if ( toLowerCase(s[st]) != toLowerCase(s[e]) ){
                return 0;
            }
            else {
                st++;
                e--;
            }
        }
        return 1;
    }

public:
    bool isPalindrome(string s){
        string temp = "";
        for (int j = 0 ; j < s.length(); j++){
            if (valid(s[j])){
                temp.push_back(s[j]);
            }
        }
        
        return checkPalindrome(temp);
    }

};
