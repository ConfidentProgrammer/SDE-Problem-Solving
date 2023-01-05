 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/kth-boom-number5609/1?page=1&difficulty[]=0&status[]=unsolved&category[]=Strings&sortBy=difficulty

## solution

 public static String BoomNumber(long K) {
        // // code here 
        // //System.out.print(isBoom(2123));
        // String res = "";
        // int counter = 0;
        // for(long i= 0 ; i<Math.pow(10,12) ; ++i) {
        //     if(isBoom(i)) {
        //       // System.out.println(i);
        //         counter++;
        //     }
        //     if(counter == K) {
        //         return Long.toString(i);
        //     }
        // }
        // return "";
        
        // Create an empty queue of strings
    Queue<String> q = new LinkedList<String>();
 
    // Enqueue an empty string
    q.add("");
 
    // counter for K'th element
    long count = 0;
 
    // This loop checks the value of count to
    // become equal to K when value of count
    // will be equals to k we will print the
    // Boom number
    while (count <= K)
    {
      // current Boom number
      String s1 = q.poll();
 
 
      // Store current Boom number before changing it
      String s2 = s1;
 
      // Append "2" to string s1 and enqueue it
      q.add(s1+"2");
      count++;
 
      // check if count==k
      if (count==K)
      {
        //System.out.println(s1); // K'th Boom number
        return s1;
       // break;
      }
 
      // Append "3" to string s2 and enqueue it.
      // Note that s2 contains the previous front
      q.add(s2+"3");
      count++;
 
      // check if count==k
      if (count==K)
      {
       // System.out.println(s2); // K'th Boom number
       return s2;
       // break;
      }
    }
    return "" ;
    }
    
    public static boolean isBoom(long K) {
         String s = Long.toString(K);
        
        // for(int i = 0 ; i<s.length() ; ++i) {
        //     if(s.charAt(i) != '2' && s.charAt(i) != '3') {
        //         return false;
        //     }
        // }
        
        // // return true;
        // String[] num = {"1", "4", "5", "6", "7", "8","9", "0"};
        
        // for(int i =0 ; i<num.length ; ++i) {
        //     if(s.contains(num[i])) {
        //         return false;
        //     }
        // }
        
        // return true;
        
        // String regex = "^[23]+$";
        // Pattern pattern = Pattern.compile(regex);
        // Matcher matcher = pattern.matcher(s);
        
        // if (matcher.find()) {
        //     return true;
        // } else {
        //   return false;
        // }
        return false;
    }
}
