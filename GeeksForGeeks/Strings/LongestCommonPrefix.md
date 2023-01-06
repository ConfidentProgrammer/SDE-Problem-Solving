 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/longest-common-prefix-in-an-array5129/1

## solution

String longestCommonPrefix(String arr[], int n){
        // code here
        
        
        //checking if Common present
        String res = arr[0];
        for(int i = 1 ; i<=n-1 ;++i) {
            res = findCommonPrefix(res, arr[i]);
        }
        
        if(res.length() == 0) {
            return "-1";
        }
        
        return res;
        }
       
        String findCommonPrefix(String s1, String s2) {
        int n1 = s1.length();
        int n2 = s2.length();
        String result = "";
        for(int i = 0, j = 0 ; i<=n1-1 && j<=n2-1  ; ++j,++i) {
            if(s1.charAt(i) != s2.charAt(j)) {
                break;
            }
            
            result+=s1.charAt(i);
        }
        
        return result;
    }
    }
