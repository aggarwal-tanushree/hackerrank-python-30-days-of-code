### Task
Complete the insert function in your editor so that it creates a new Node (pass _data_ s the Node constructor argument) and inserts it at the tail of the linked list referenced by the _head_ parameter. Once the new node is added, return the reference to the _head_ node.

Note: The _head_ argument is null for an empty list.

### Input Format
The first line contains T, the number of elements to insert.
Each of the next _T_ lines contains an integer to insert at the end of the list.

### Output Format
Return a reference to the _head_ node of the linked list.


### Sample Input

```txt

STDIN   Function
-----   --------
4       T = 4
2       first data = 2
3
4
1       fourth data = 1

```

### Sample Output

```txt

2 3 4 1

```

## My Solution

```py

class Node:
    def __init__(self,data):
        self.data = data
        self.next = None 
class Solution: 
    def display(self,head):
        current = head
        while current:
            print(current.data,end=' ')
            current = current.next

    def insert(self,head,data): 
    #Complete this method
        if head is None:
            head = Node(data)
        else:
            curr = head
            while curr.next:
                 curr = curr.next
            curr.next = Node(data)
        return head
    
mylist= Solution()
T=int(input())
head=None
for i in range(T):
    data=int(input())
    head=mylist.insert(head,data)    
mylist.display(head); 	  

```
