 ## Third Largest Number

## https://practice.geeksforgeeks.org/problems/magical-string3653/1?page=6&status[]=unsolved&category[]=Strings&sortBy=difficulty

## solution

   static String magicalString(String S){
        // code here
        String s = "abcdefghijklmnopqrstuvwxyz";
        HashMap<String, String> hm = new HashMap<>();
        String res = "";
        for(int i = 0, j = 25  ; i<=25 && j>=0 ; ++i, --j) {
            hm.put(String.valueOf(s.charAt(i)), String.valueOf(s.charAt(j)));
          //  System.out.println(hm.get(String.valueOf(s.charAt(i))));
        }
//         for (String key : hm.keySet()) {
//         System.out.println(key+" "+hm.get(key));
//   }
        for(int i = 0 ; i<S.length() ; ++i) {
            String ch = String.valueOf(S.charAt(i));
            if(hm.containsKey(ch)) {
                res+=hm.get(ch);
            }
        }
        
        
        return res;
    }