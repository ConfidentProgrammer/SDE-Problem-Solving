## Minimum Distance between numbers in array

## https://practice.geeksforgeeks.org/problems/minimum-distance-between-two-numbers/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

## solution


class Solution {
    int minDist(int a[], int n, int x, int y) {
        // code here
        int fx = -21;
        int fy = -21;
        int nx =0 ;
        int ny =0 ;
        int dis = n + 1;
       // ArrayList<Integer> dis = new ArrayList<Integer>();
        
        for(int i = 0 ; i<n ; ++i) {
            
            if(a[i] == x) {
               break;
            }else {
                nx++;
            }
        }
        for(int i = 0 ; i<n ; ++i) {
            
            if(a[i] == y) {
                break;
            }else {
                ny++;
            }
        }
        
        if(nx == n || ny == n) {
            return -1;
        }
        for(int i = 0 ; i<n ; ++i) {
            
            if(a[i] == x) {
                fx = i;
            }
            if(a[i] == y) {
                fy = i;
            }
            if(fx != -21 && fy!=-21) {
            dis = Math.min(dis, (Math.abs(fy - fx)));
           
        
        return dis == n+1 ? -1 : dis ;
    }
}