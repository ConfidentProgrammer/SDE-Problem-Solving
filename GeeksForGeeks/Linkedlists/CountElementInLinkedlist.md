## Count nodes in linkedlist

## https://practice.geeksforgeeks.org/problems/count-nodes-of-linked-list/1?page=1&category[]=Linked%20List&sortBy=difficulty

## solution

 public static int getCount(Node head)
    {
        
        //Code here
        int n=0;
        Node node = head;
        
        while(node != null) {
            n+=1;
            node = node.next;
        }
        //System.out.print(n);
        
        return n;
    }
    