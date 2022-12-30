 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/find-number-of-numbers/1?page=1&difficulty[]=-1&difficulty[]=0&status[]=unsolved&category[]=Arrays&sortBy=difficulty

## solution

public static int num(int a[], int n, int k)
            {
                 //Your code here
                 int count = 0;
                 String keyStr = k+"";
                 String whole = "";
                 
                 for(int i = 0 ; i<n ; ++i){
                     whole+=Integer.toString(a[i]);
                 }
                 
                 
                 char[] arrstr = whole.toCharArray();
                 
                 
                 for(int i = 0 ; i<arrstr.length ; ++i){
                    String s= ""+arrstr[i];
                    //System.out.println(s+" "+keyStr);
                   if(keyStr.equals(s)){
                       count++;
                   }
                 }
                 
                 return count;
            }