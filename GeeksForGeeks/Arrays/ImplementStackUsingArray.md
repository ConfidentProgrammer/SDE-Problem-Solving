## Implement Stack using array

## https://practice.geeksforgeeks.org/problems/implement-stack-using-array/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

## solution

    void push(int a)
	{
	    // Your code here
	    if(top == -1){
	        arr[0] = a;
	        top = 0;
	    }else {
	        int temp = arr[top];
	        arr[top+1] = a;
	        top+=1;
	    }
	} 
	
    //Function to remove an item from top of the stack.
	int pop()
	{
        // Your code here
       if(top == -1){
           return -1;
       }else {
           int temp = arr[top];
           arr[top] = -1;
           top-=1;
           return temp;
       }
      
	}