## Print Element in Linkedlist

## https://practice.geeksforgeeks.org/problems/print-linked-list-elements/1?page=1&category[]=Linked%20List&sortBy=difficulty

## solution


    // for empty list
    void display(Node head)
    {
        //add code here.
        Node node = head;
        while(node != null) {
            System.out.print(node.data+" ");
            node = node.next;
        }
        
    }