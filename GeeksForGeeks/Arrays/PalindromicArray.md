## Palindromic Array

## https://practice.geeksforgeeks.org/problems/palindromic-array-1587115620/1?page=1&category[]=Arrays&category[]=OOP&sortBy=difficulty

## solution
	public static int palinArray(int[] a, int n)
           {
               
                for(int i = 0 ; i<n ; ++i) {
                   boolean ans = isPalin(a[i]);
                   
                   if(!ans) {
                       return 0;
                   }
                  }
                  
                 return 1;
                
           }
           
    public static boolean isPalin(int n){
        String str = Integer.toString(n);
        int temp = 0;
        for(int i = 0, j=str.length()-1 ; i<str.length() && j>=0   ; --j, ++i){
            if(str.charAt(i) == str.charAt(j)){
                temp+=1;
            }
        }
        //System.out.println(temp+" "+str.length());
        if(temp == str.length()){
            return true;
        }
        return false;
    }