**Linked List**
•	Each node is composed of a data and a reference/link to the next node in the sequence
•	Simple and very common data structure
•	They can be used to implement several other common data types: stacks, queues
•	The principal benefit of a linked list over a conventional array is that the list elements can easily be inserted or removed without reallocation or reorganization of the entire structure because the data items need not be stored in memory or on disk in one block
•	An array has to be declared in the source code, before compiling and running the program
•	On the other hand, simple linked lists by themselves do not allow random access to the data
•	Many basic operations such as obtaining the last node of the list , or finding a node that contains a give data, or locating the place where a new node should be inserted – may require sequential scanning of most or all of the list elements
	LinkedList	Arrays(ArrayList)
Indexing	O(n)	O(1)
Insert at the beginning	O(1)	O(n)
Waste Space	O(n)	0

•	Use linked lists if you want to insert/remove elements at the beginning
•	Use linked lists if the size is changing frequently. Otherwise use arrays.
•	Use arrays if you need random access: It can be done very quickly, in O(1) constant time

**Array List**
Consider 
87
6
2
59
-45
0
400
20

If we want to remove  -45 from the array, we delete -45 but we have to reconstruct our data structure
We have to keep swapping these items until  we reconstruct the entire array. 




87
6
2
59
0
400
20

Time Complexity for deleting an item from an array list: O(N)
It is not very slow though it is not as fast as a linked list.

**Linked List**
To remove 5 for  example




We just have to update the references so that the pointer from node 9 is going to point to node 8 
As shown below



It does this in constant time complexity O(1)
So when deleting an item, it is much faster for a linked list than for arraylist.When dealing with a problem that requires a lot of deletion and you have to choose between a linked list and an array, it is advisable to go for a linked list.

**Advantages of a Linked List**
•	Linked lists are dynamic data structures while arrays are not.
•	It can allocate the needed memory in run-time
•	Very efficient if we want to manipulate the first elements
•	Easy implementation
•	Can store items with different sizes; an array assumes every element to be exactly the same
•	It is easier for a linked list to grow organically. An array’s size needs to be known ahead of time, or re-created when it needs to grow.

**Disadvantages of  Linked Lists**
•	Waste memory because of the references
•	Nodes in a linked list must be read in order from the beginning as linked lists have sequential access. Array items on the other hand can be reached via indexes in O(1) time.
•	Difficulties arise in linked lists when it comes to reverse traversing. Singly linked lists are extremely difficult to navigate backwards. The solution however is to use doubly linked lists. Doubly linked lists despite being easier to read, lead to memory wastage in allocating space for a back pointer.
Inserting Items in a Linked List
Items can be inserted both at the beginning and at the end of a linked list
The last element always points to a null. 



So if we want to insert 2 to the end of the list we have to go through the list sequentially till the end of the list. 
So how do we decide that it is the end of the list?
When the item points to a null




Similarly if we want to insert 5 we have to go through the list till  we find the item pointing to null


**Conclusion**
We have to iterate through the whole list to insert the new item -> time complexity: O(N)
Insert Items at the beginning of a Linked List
In a linked list it is preferable to insert items at the beginning of a list. We do not have to go through the entire list. We just insert it at the beginning and update the references. This means, we point the node we want to insert to the reference of the next node and point it to the previous first node.
The time complexity for inserting an item at the beginning is very first. It is constant time complexity. 


 

**Deleting from a linked list**
•	It is the same as for insertion	


