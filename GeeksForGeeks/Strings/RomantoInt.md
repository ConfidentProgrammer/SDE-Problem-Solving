 ## Third Largest Number

## https://leetcode.com/problems/roman-to-integer/submissions/872837776/

## solution

   public int romanToInt(String s) { // 1234 == 1000 + 200 + 30 + 4
        int res = 0;
        Map<String, Integer> hm = new HashMap<>();
        String[] romans = {"I", "V" , "X" , "L", "C","D", "M", "IV", "IX", "XL", "XC", "CD", "CM"};
        int[] integers = {1,5,10,50,100,500,1000,4,9,40,90,400,900};
        int n= s.length();
        for(int i = 0 ; i<13 ; ++i)
                hm.put(romans[i], integers[i]);
        for(int i =0 ; i<n; i++){
            String key = String.valueOf(s.charAt(i));
            if(i + 1 < s.length()) {
            if(s.charAt(i) == 'I' && s.charAt(i+1) == 'V') {
                res+=4;
                i+=1;
                
            }
            else if(s.charAt(i) == 'I' && s.charAt(i+1) == 'X') {
               res+=9;
                i+=1;
               
            }
            else if(s.charAt(i) == 'X' && s.charAt(i+1) == 'L') {
                res+=40;
                i+=1;
                
            }
            else if(s.charAt(i) == 'X' && s.charAt(i+1) == 'C') {
                res+=90;
                i+=1;
                
            }
           else if(s.charAt(i) == 'C' && s.charAt(i+1) == 'D') {
                res+=400;
                i+=1;
             
            }
           else if(s.charAt(i) == 'C' && s.charAt(i+1) == 'M') {
                res+=900;
                i+=1;
            }else {
                res+=hm.get(String.valueOf(s.charAt(i)));
            }
            }else {
                res+=hm.get(String.valueOf(s.charAt(i)));
            }
            
        }
        return res;
    }