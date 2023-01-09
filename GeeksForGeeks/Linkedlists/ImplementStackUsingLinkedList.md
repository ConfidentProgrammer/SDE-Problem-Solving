## https://practice.geeksforgeeks.org/problems/implement-stack-using-linked-list/1?page=1&category[]=Linked%20List&sortBy=difficulty

## solution

void push(int a) 
    {
        // Add your code here
        StackNode node = new StackNode(a);
        
        node.next = top;
        top = node;
        
        
        
    }
    
    //Function to remove an item from top of the stack.
    int pop() 
    {
        // Add your code here
        if(top == null) {
            return -1;
        }
        
        StackNode topNode = top;
 
        top = topNode.next;
        return topNode.data;
        
    }