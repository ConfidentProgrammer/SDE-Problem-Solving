## https://practice.geeksforgeeks.org/problems/intersection-of-two-arrays2404/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

## solution


// User function Template for Java

class Solution {
    // Function to return the count of the number of elements in
    // the intersection of two arrays.
    public static int NumberofElementsInIntersection(int a[], int b[], int n, int m) {
        // Your code here
        Set<Integer> s1= new HashSet<Integer>();
        Set<Integer> s2= new HashSet<Integer>();
        int count = 0;
        for(int i = 0 ; i<n ; ++i) {
            s1.add(a[i]);
        }
        for(int i = 0 ; i<m ; ++i) {
            s2.add(b[i]);
        }
        
        for(Integer num : s1) {
            if(s2.contains(num)) count++;
        }
        
        return count;
    }
};
