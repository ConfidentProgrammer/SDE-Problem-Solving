## Print Alternate number

## https://practice.geeksforgeeks.org/problems/print-alternate-elements-of-an-array/1?page=1&category[]=Arrays&category[]=OOP&sortBy=difficulty

## solution

class GfG
{
    public static void print(int arr[], int n)
    {
        // your code here
        for(int i = 0 ; i<n ; i+=2){
            System.out.print(arr[i]+" ");
        }
        
    }
}