## https://practice.geeksforgeeks.org/problems/node-at-a-given-index-in-linked-list/1?page=1&category[]=Linked%20List&sortBy=difficulty

## solution

{
       //Your code here
       Node nod = node ;
       int n = 1;
       int res = 0;
       while(nod != null) {
           if(n == ind) {
               res = nod.data;
               break;
           }
           nod = nod.next;
           n++;
       }
       
       return res;
    }