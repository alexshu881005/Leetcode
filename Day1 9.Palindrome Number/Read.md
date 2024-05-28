Given an integer x, return true if x is a palindrome, and false otherwise.

這題希望判斷x是否為所謂的回文數，也就是所謂可以正讀反讀皆相同的數，若是X為回文數

```
class Solution {
    public boolean isPalindrome(int x) {
        if(x<0){
        return false;
        }
        int i,j=0,k;
        k=x;
        while(x>0){
        i=x%10;
        j=(j*10)+i;
        x=x/10;
        }
        if(j==k){
            return true;
        }
        else
            return false;
    }
}
```
