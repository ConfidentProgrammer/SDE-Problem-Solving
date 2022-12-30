 ## FindIndex

## https://practice.geeksforgeeks.org/problems/binary-search-1587115620/1?page=1&difficulty[]=-1&difficulty[]=0&status[]=unsolved&category[]=Arrays&sortBy=difficulty

## solution
    int binarysearch(int arr[], int n, int k) {
        // code here
        int start = 0;
        int end  = n-1;
        int mid = 0;
        
        while(start <= end) {
            mid = start + (end-start)/2;
            if(arr[mid] == k) {
                 return mid;
            }
            if(arr[mid] < k) {
                start = mid + 1;
            }
            if(arr[mid] > k) {
                end = mid - 1;
            }
            
        }
       return -1;
    }