這題簡單而言，就是將對應數字切換成字串，例如300就是變成CCC，5000的話字串會變成MMMMM，5432，MMMMMCDXXXII，以此類推，要注意到的是其中像是400會變成CD也就是D-C，部分的數字切換成字串會需要做成這種效果，所以在陣列中需要把所有的可能性都列出

```
class Solution {
    public String intToRoman(int num) {
        int[] values={1000,900,500,400,100,90,50,40,10,9,5,4,1};
        
        String[] romanNumber={"M","CM","D","CD","C","XC","L","XL","X","IX","V","IV","I"};
        StringBuffer test = new StringBuffer();
        int i = 0;
        while(num>0){
           if(num>= values[i])
             { 
             test.append(romanNumber[i]);
             num -=values[i];
             }else{
                i++;
             }
        }
        //while迴圈中判斷num變數只要比當前values[i]大，就減去values[i]，利用append做字串連接。
        return test.toString();
    }
}
```