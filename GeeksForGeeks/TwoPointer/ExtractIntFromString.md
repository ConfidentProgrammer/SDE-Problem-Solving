## https://practice.geeksforgeeks.org/problems/extract-the-integers4428/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

## solution


ArrayList<String> extractIntegerWords(String s) 
    { 
        // code here
        String numbers = "1234567890";
        StringBuilder temp = new StringBuilder();
        ArrayList<String> res = new ArrayList<String>();
        
        
        for(int i=0 ; i<s.length() ; ++i) {
            String ch =  String.valueOf(s.charAt(i));
            if(numbers.contains(ch)) {
                temp.append(ch); // temp+=ch;
                
            }else {
                if(temp.length() != 0){ // temp!=""
                    res.add(temp.toString());
                    
                }
                temp.setLength(0); //temp = ""
            }
            
            
        }
       if(temp.length() != 0){
           res.add(temp.toString());
       }
        return res;
    }