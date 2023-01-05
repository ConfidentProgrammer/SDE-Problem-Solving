 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/roll-the-characters-of-a-string2127/1?page=1&difficulty[]=0&status[]=unsolved&category[]=Strings&sortBy=difficulty


## solution

   String findRollOut(String s,long roll[], int N)
    {
 
    char[] chars = s.toCharArray();
   String res = "";
    // for first character
    // int ascii = s.charAt(0);
    
    // chars[0]= (char)(ascii+(N%26));
    
    // System.out.print(chars[0]);
    //Arrays.sort(roll);
    for(int i = 0  ; i<N ; ++i) {
        for(int j = 0 ;j < roll[i]; ++j) {
           // int ascii = s.charAt(j);
            if(chars[j] == 'z') {
                chars[j] = 'a';
            }else {
            chars[j] += 1; //(char)(ascii+(1%26)); 1     
            }
           
        }
    }

     res =  String.valueOf(chars);
    return res;
    }