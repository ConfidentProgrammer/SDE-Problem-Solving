 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/third-largest-element/1?page=1&difficulty[]=-1&difficulty[]=0&status[]=unsolved&category[]=Arrays&sortBy=difficulty

## solution

    int thirdLargest(int a[], int n)
    {
	    // Your code here
	    int x=0,y=0,z = 0;
	    
	    for(int i = 0 ; i<n ; ++i){
	        if(a[i]>x){
	            z = y;
	            y = x;
	            x = a[i];
	        }
	       if(a[i]!=x && a[i]>y){
	           z = y;
	           y = a[i];
	           
	       }
	       if(a[i]<x && a[i]<y && a[i]>z) {
	           z = a[i];
	       }
	//   System.out.println(i);     
	    }
	 // System.out.print(x+" "+y+" "+z);
	    return z;
    }