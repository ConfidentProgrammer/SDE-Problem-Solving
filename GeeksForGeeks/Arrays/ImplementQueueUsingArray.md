## Implement Stack using array

## https://practice.geeksforgeeks.org/problems/implement-queue-using-array/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

## solution

	//Function to push an element x in a queue.
	void push(int x)
	{
	    // Your code here
	    if(rear == 0) {
	        arr[0] = x;
	        rear += 1;
	    }else {
	        arr[rear] = x;
	        rear+=1;
	    }
	} 

    //Function to pop an element from queue and return that element.
	int pop()
	{
		// Your code here
		if(rear == front ) {
		    return -1;
		}else {
		    int temp = arr[front];
		  //  for(int i = 0 ; i<rear-1 ; ++i){
		  //      arr[i] = arr[i + 1] ;
		  //  }
		    
	      //  rear-=1;
		    return arr[front++];
		    
		}
	} 