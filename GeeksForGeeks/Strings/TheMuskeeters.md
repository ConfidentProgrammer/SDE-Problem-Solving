 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/the-muskteers3519/1?page=6&status[]=unsolved&category[]=Strings&sortBy=difficulty


## solution

    static boolean checkTogether(String str){
        int start = 0;
        int end = 0;
        
        if(!str.contains("0")) {
            return false;
        }else {
            
          //finding first index 
          for(int i =0 ; i<str.length() ; ++i){
              if(str.charAt(i) == '0'){
                  start = i;
                  break;
              }
          }
          
          //finding last index 
          for(int i =str.length()-1 ; i>=0 ; --i){
              if(str.charAt(i) == '0'){
                  end = i;
                  break;
              }
          }
          
          for(int i = start ; i<end ; ++i){
              if(str.charAt(i) == '1'){
                  return false;
              }
          }
          
          
        }