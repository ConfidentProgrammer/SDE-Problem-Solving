## print fib using iterative method
  public static void main(String[] args) {
       int n = 15;
       int[] arr = new int[n];
       arr[0] = 1;
       arr[1] = 1;
       int count = 0;
       for(int i = 2 ; i<n ; ++i) {
           arr[i] = arr[i-2] + arr[i-1];
           System.out.println(arr[i]);
       }
          
    }

## print fib using the recursion
public static void main(String[] args) {
       for(int i = 0  ; i<23 ; ++i)
            System.out.print(printFib(i)+" ");
}
public static int printFib(int n) {
        if(n <= 1) return 1;
        
        return printFib(n - 2) + printFib(n - 1);
        
}