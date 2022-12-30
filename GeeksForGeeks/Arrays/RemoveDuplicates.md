 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/remove-duplicate-elements-from-sorted-array/1?page=1&difficulty[]=0&status[]=unsolved&category[]=Arrays&sortBy=difficulty

## solution

 int remove_duplicate(int A[],int N){
        // code here
        // code here 
         ArrayList<Integer> res = new ArrayList<Integer>();
     //    int[] web = new int[1000];
         int n = 0;
        int temp = 0;
        for(int i = 0 ; i<N ; ++i) {
            
            if(A[i]!=temp) {
                temp = A[i];
                A[n] = temp; 
               //System.out.println(A[i]);
               n+=1;
            }        
        }
        
        return n;
    }