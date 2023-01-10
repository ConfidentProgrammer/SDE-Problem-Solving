## https://practice.geeksforgeeks.org/problems/union-of-two-linked-list/1?page=1&category[]=Linked%20List&sortBy=difficulty

## solution

	public static Node findUnion(Node head1,Node head2)
	{
	    //Add your code here.
	    Set<Integer> a = getSet(head1);
	    Set<Integer> b = getSet(head2);
	    System.out.println(a);
	    System.out.println(b);
	    //creating Node
	    Node result = new Node(0);
	    Node temp = result;
	    Set<Integer> combined = new HashSet<Integer>();
	    
	    combined.addAll(a);
	    combined.addAll(b);
	    System.out.println(combined);
	    for (Integer num : combined) {
             temp.next = new Node(num);
             temp = temp.next;
          //  result.next = temp;
        }
	    
	   return result.next;
	}
	
	public static Set<Integer> getSet(Node head) {
	    
//	    Map<Integer, Integer> hm = new Hashmap<Integer, Integer>();
	    Set<Integer> numbers = new HashSet<Integer>();
	    
	    //assigning into the hm;
	    while(head != null) {
	        numbers.add(head.data);
	        head = head.next;
	    }
	    
	    return numbers;
	}