## Implement Stack using array

## https://practice.geeksforgeeks.org/problems/replace-all-0s-with-5/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

## solution

  int convertfive(int num) {
        // Your code here
        String s1 = "" + num;
        String s2 = "";
        //char[] strarr = s1.toCharArray();
        
        //System.out.print(strarr);
        
        for(int i = 0 ; i<s1.length()  ; ++i) {
            if(s1.charAt(i) == '0') {
                s2+='5';
            }else {
                s2+=s1.charAt(i);
            }
        }
       // System.out.print(s2);
        return Integer.parseInt(s2);
    }