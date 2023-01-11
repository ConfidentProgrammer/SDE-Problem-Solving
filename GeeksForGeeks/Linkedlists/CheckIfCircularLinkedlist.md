## https://practice.geeksforgeeks.org/problems/circular-linked-list/1?page=1&category[]=Linked%20List&sortBy=difficulty

## solution

	    Node tempHead = head;
        
        
        while(head != null) {
           // System.out.println(head.data);
            if(head.next == tempHead) {
                return true;
            }
            head = head.next;
        }
        
        return false;
    }