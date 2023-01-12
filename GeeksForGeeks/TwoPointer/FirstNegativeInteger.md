
## https://practice.geeksforgeeks.org/problems/first-negative-integer-in-every-window-of-size-k3345/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

## solution

public long[] printFirstNegativeInteger(long A[], int N, int K) // N-(K-1)
    {
        ArrayList<Long> res = new ArrayList<>(); 
        int counter = 0;
        for(int i = 0 ; i<N-(K-1) ; ++i) {
            for(int j = i ; j<K+i ; ++j) {
                if(A[j]<0) {
                    res.add(A[j]);
                    break;
                }
                counter++;
            }
            if(counter == K) {
               res.add(Long.valueOf(0)); 
            }
            counter = 0;
           //System.out.println();
        }
        
        long[] arr = res.stream().mapToLong(i -> i).toArray();
        return arr;
    }