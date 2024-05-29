求找到兩個字符串的最大公約數。

```
class Solution {
    public String gcdOfStrings(String str1, String str2) {
        int stra=str1.length();
        int strb=str2.length();//宣告次輸入的陣列
        int max=Math.min(stra, strb);//回傳兩次輸入的最小值
        for(int i=max;i>=1;i--){
            if(stra % i == 0  && strb % i == 0 && str1.substring(0,i).equals(str2.substring(0,i)))
                //當兩段字串全被算入，餘數為零，substring的用處是定義回傳，equals的用法為將字串與指定字串比較，返回值為T/F
        {
        String tmp1=str1.substring(i)+str1.substring(0,i);
        String tmp2=str2.substring(i)+str2.substring(0,i);
        //將相同的放入同個字串
        if(tmp1.equals(str1)&&tmp2.equals(str2)){
            return str1.substring(0,i);
        }
        //如果兩邊對應的相同，回傳給str1
        }
        }
        return "";
        }
    }
```