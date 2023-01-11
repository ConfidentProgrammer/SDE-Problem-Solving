## https://practice.geeksforgeeks.org/problems/sorted-insert-for-circular-linked-list/1?page=2&category[]=Linked%20List&sortBy=difficulty

## solution
public static Node sortedInsert(Node head,int data)
         {
            //add code here.
            Node tempHead = head;
            //getting tail;
            Node tail = getTail(head);
           
           
        if(data < head.data) {
            Node node = new Node(data);
            node.next = head;
            head = node;
            tail.next = head;
            return tail.next;
        }
            while(head.next != tempHead) {
               if((head.data < data && head.next.data >= data)) {

                   Node node = new Node(data);
                   Node headNext = head.next;
                   head.next = node;
                   node.next = headNext;
                   
                   break;
               }
               
                head=head.next;
            }
            
            return tail.next;
         }
         
         public static Node getTail(Node head)  {
             Node tail = head;
             while(tail.next != head) {
                 tail = tail.next;
             }
         //    System.out.println(tail.data);
             return tail;
         }