 ## FindIndex

## https://practice.geeksforgeeks.org/problems/find-index4752/1?page=1&category[]=Arrays&category[]=OOP&sortBy=difficulty

## solution
   
   
    static int[] findIndex(int a[], int N, int key) 
    { 
        //code here.
        int fromRight = 1000;
        int fromLeft  = 1000;
        int[] indices={-1,-1};
        
        //left
        for(int i = 0 ; i<N ;++i){
            if(a[i] == key) 
            {
                fromLeft = i ;
                break;
            }
        }
        
        //right
        for(int j = N-1 ; j>=0 ; --j){
            if(a[j] == key){
                fromRight = j ;
                break;
            }
        }
        
       // System.out.println(fromLeft+" "+fromRight);
       if(fromRight != 1000 && fromLeft != 1000) {
        indices[0] = fromLeft;
        indices[1] = fromRight;   
       }
        
        return indices;
    
}