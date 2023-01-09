## https://practice.geeksforgeeks.org/problems/intersection-of-two-sorted-linked-lists/1?page=1&category[]=Linked%20List&sortBy=difficulty

## solution
   Node newHead = new Node(0);  //0
            
            //newHead.next = null;
            Node temp = newHead; //0
            Node h1 = head1;
            Node h2 = head2;
            
  
            
            while(h1!=null && h2!=null) {
                if(h1.data < h2.data) {
                    h1 = h1.next;
                }else if(h1.data > h2.data) {
                    h2 = h2.next;
                }else if(h1.data == h2.data) {
                    //creating temp linkedList
                    temp.next = new Node(h2.data);
                    temp = temp.next;
                 //   newHead.next = temp;
                    //newHead = temp;
                    h1 = h1.next;
                    h2 = h2.next;
                }
            }
            
            return newHead.next;