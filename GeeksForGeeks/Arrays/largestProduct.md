## Minimum Distance between numbers in array

## https://practice.geeksforgeeks.org/problems/largest-product/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

## solution


class GfG
{
    long findMaxProduct(int A[], int n, int k)
    {
        
	// Your code here	
	long prod = 1;
	long temp = 0;
	    for(int j = 0; j<(n+1)-k ; ++j) 
	    {
	        for(int i = j ; i<k+j ; ++i) {
	         prod *= A[i];
	        }
	        
	        if(prod > temp) {
	            temp = prod;
	        }
	        prod = 1;
	        //
	        
	    }
	
	
    	return temp;
    }
}