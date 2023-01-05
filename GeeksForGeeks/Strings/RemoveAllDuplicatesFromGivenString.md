 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/remove-all-duplicates-from-a-given-string4321/1?page=1&difficulty[]=0&status[]=unsolved&category[]=Strings&sortBy=difficulty


## solution

   String removeDuplicates(String str) {
        // code here
        String result = "";
        String duplicates = "";
        
        for(int i = 0 ; i<str.length() ; ++i) {
            if(!duplicates.contains(String.valueOf(str.charAt(i)))) {
                result+=str.charAt(i);
                duplicates+=str.charAt(i);
            }
        }
        
        return result;
    }