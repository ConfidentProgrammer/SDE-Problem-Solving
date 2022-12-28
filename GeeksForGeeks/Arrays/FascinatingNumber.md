## Fascinating Number

## https://practice.geeksforgeeks.org/problems/fascinating-number3751/1?page=1&category[]=Arrays&sortBy=difficulty

## solution

    boolean fascinating(long n) {
        // code here
        String s1 = Long.toString(n*2);
        String s2 = Long.toString(n*3);
        String result = Long.toString(n)+s1+s2;
        char a[] = result.toCharArray();
        Arrays.sort(a);
        String str = new String(a);
        //System.out.print(result);
        if(str.equals("123456789")) {
            //System.out.print("Fascinating");
            return true;
        }else {
          //  System.out.print("Not Fascinating");
            return false;
        }
        
    }