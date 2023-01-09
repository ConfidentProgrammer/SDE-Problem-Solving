## https://practice.geeksforgeeks.org/problems/linked-list-insertion-1587115620/1?page=1&category[]=Linked%20List&sortBy=difficulty

## solution
Node insertAtBeginning(Node head, int x)
    {
        // code here
        Node node = new Node(x);

        node.next = head;

        
        return node;
    }
    
    //Function to insert a node at the end of the linked list.
    Node insertAtEnd(Node head, int x)
    {
        // code here
        Node last = new Node(x);
    
        if(head == null) {
            head = last;
        }
        
        Node node = head;
        while(node.next != null) {
            
            node = node.next;
        }
        node.next = last;
        last.next = null;
        
        return head;
        
        
    }