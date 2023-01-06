 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/reverse-words-in-a-given-string5459/1

## solution

    String reverseWords(String S)
    {
        // code here 
        ArrayList<String> list = new ArrayList<>();
        String s = S+".";
        String temp = "";
        String res = "";
        int sLen = s.length();
        for(int i = 0 ; i<sLen ; ++i){
            if(s.charAt(i) != '.') {
                temp+=s.charAt(i);
            }else {
                list.add(temp);
                temp = "";
            }
        }
        
        int n = list.size() - 1;
        for(int i = n ; i>=0; --i){
             res+=list.get(i);
            if(i != 0) {
          
            res+=".";
            }
            
            
        }
        
        
       // System.out.print(list);
        return res;
    }