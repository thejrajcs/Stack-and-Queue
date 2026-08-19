Stack and Queue: Concepts, Algorithms, Easy Examples and Python Codes
1. Introduction to DSA
DSA stands for Data Structures and Algorithms. A data structure is a way to store and organize data,
while an algorithm is a step-by-step procedure used to solve a problem.
Examples include Array, Linked List, Stack, Queue, Tree, Graph and Hash Table.
2. Stack
A Stack is a linear data structure that follows LIFO (Last In, First Out). The element inserted last is
removed first.
Easy example: A stack of plates. If Plate 1, Plate 2 and Plate 3 are placed one above another, Plate 3 is
removed first.
3. Stack Operations
Operation Meaning
Push
Pop
Add an element
Remove the top element
Peek
IsEmpty
Size
See the top element
Check whether stack is empty
Find number of elements
4. Push Algorithm
Purpose: Add an element to the stack.
Step 1: Check whether stack is full.
Step 2: If full, display "Stack Overflow".
Step 3: Otherwise add the element at the top.
Step 4: Increase top by 1.
Step 5: Stop.
Example: [10, 20] fi Push 30 fi [10, 20, 30]
5. Pop Algorithm
Purpose: Remove the top element.
Step 1: Check whether stack is empty.
Step 2: If empty, display "Stack Underflow".
Step 3: Otherwise remove the top element.
Step 4: Decrease top by 1.
Step 5: Stop.
Example: [10, 20, 30] fi Pop fi 30 is removed fi [10, 20]
DSA Stack and Queue Report | Page 1
6. Peek Algorithm
Purpose: View the top element without removing it.
Step 1: Check whether stack is empty.
Step 2: If empty, display "Stack is empty".
Step 3: Otherwise display the top element.
Step 4: Stop.
Example: Stack = [10, 20, 30], Peek = 30.
7. Stack Python Code
stack = []
stack.append(10)
stack.append(20)
stack.append(30)
print("Stack:", stack)
print("Top element:", stack[-1])
stack.pop()
print("After pop:", stack)
Output: Stack: [10, 20, 30] | Top element: 30 | After pop: [10, 20]
Python: append() = Push, pop() = Pop, stack[-1] = Peek.
8. Applications of Stack
Stack is used in browser Back operations, Undo/Redo, function calls, expression evaluation, parentheses
checking, backtracking and DFS.
Browser example: Google fi YouTube fi GitHub. Pressing Back returns to YouTube first.
9. Queue
A Queue is a linear data structure that follows FIFO (First In, First Out). The element inserted first is
removed first.
Easy example: People standing in a line at a ticket counter. The person who comes first gets served first.
10. Queue Operations
Operation Meaning
Enqueue
Dequeue
Front
Rear
Add an element
Remove an element
First element
Last element
IsEmpty
Size
Check whether queue is empty
Number of elements
11. Enqueue Algorithm
DSA Stack and Queue Report | Page 2
Purpose: Add an element to the queue.
Step 1: Check whether queue is full.
Step 2: If full, display "Queue Overflow".
Step 3: Otherwise add the element at the rear.
Step 4: Move rear forward.
Step 5: Stop.
Example: [10, 20] fi Enqueue 30 fi [10, 20, 30]
12. Dequeue Algorithm
Purpose: Remove the first element from the queue.
Step 1: Check whether queue is empty.
Step 2: If empty, display "Queue Underflow".
Step 3: Otherwise remove the front element.
Step 4: Move front forward.
Step 5: Stop.
Example: [10, 20, 30] fi Dequeue fi 10 is removed fi [20, 30]
13. Queue Python Code
from collections import deque
queue = deque()
queue.append(10)
queue.append(20)
queue.append(30)
print("Queue:", queue)
print("Front element:", queue[0])
queue.popleft()
print("After dequeue:", queue)
Output: Queue: deque([10, 20, 30]) | Front element: 10 | After dequeue: deque([20, 30])
Python: append() = Enqueue, popleft() = Dequeue, queue[0] = Front.
14. Applications of Queue
Queue is used in printer queues, ticket booking, CPU scheduling, customer service, call centers, network
requests and BFS.
Printer example: Document 1, Document 2 and Document 3 are printed in the same order in which they
entered.
15. Stack vs Queue
Feature
Stack
Principle
LIFO
Queue
FIFO
Insertion
Removal
Example
Main operation
Top
Top
Stack of plates
Push
Rear
Front
People in a line
Enqueue
DSA Stack and Queue Report | Page 3
Feature
Stack
Remove operation Pop
Queue
Dequeue
Graph use
DFS
BFS
16. Stack Using Class in Python
class Stack:
    def __init__(self):
        self.items = []
    def push(self, item):
        self.items.append(item)
    def pop(self):
        if self.items:
            return self.items.pop()
        return "Stack is empty"
    def peek(self):
        if self.items:
            return self.items[-1]
        return "Stack is empty"
s = Stack()
s.push(10)
s.push(20)
s.push(30)
print(s.items)
print(s.peek())
print(s.pop())
print(s.items)
Output: [10, 20, 30] fi 30 fi 30 fi [10, 20]
17. Queue Using Class in Python
class Queue:
    def __init__(self):
        self.items = []
    def enqueue(self, item):
        self.items.append(item)
    def dequeue(self):
        if self.items:
            return self.items.pop(0)
        return "Queue is empty"
    def front(self):
        if self.items:
            return self.items[0]
        return "Queue is empty"
q = Queue()
q.enqueue(10)
q.enqueue(20)
q.enqueue(30)
print(q.items)
print(q.front())
DSA Stack and Queue Report | Page 4
print(q.dequeue())
print(q.items)
Output: [10, 20, 30] fi 10 fi 10 fi [20, 30]
18. Stack and Queue in Graph Algorithms
DFS (Depth First Search) generally uses a Stack. It explores deeply before coming back.
Example: A connected to B and C; B connected to D and E. A possible DFS order is A fi B fi D fi E fi C.
BFS (Breadth First Search) uses a Queue. It visits nodes level by level.
For the same graph, a possible BFS order is A fi B fi C fi D fi E.
19. Time Complexity
Operation
Time
Stack Push
O(1)
Stack Pop
Stack Peek
O(1)
O(1)
Queue Enqueue using deque O(1)
Queue Dequeue using deque O(1)
Queue Front
O(1)
O(1) means the operation takes approximately constant time.
20. Important Terms
Stack Overflow: Trying to add an element to a full stack.
Stack Underflow: Trying to remove an element from an empty stack.
Queue Overflow: Trying to add an element to a full queue.
Queue Underflow: Trying to remove an element from an empty queue.
21. Easy Way to Remember
STACK fi LIFO fi Plates fi DFS
QUEUE fi FIFO fi Line fi BFS
22. Interview Questions
Q. What is a Stack? A linear data structure that follows LIFO.
Q. What is a Queue? A linear data structure that follows FIFO.
Q. What is Push? The operation used to add an element to a stack.
Q. What is Pop? The operation used to remove the top element from a stack.
Q. What is Enqueue? The operation used to add an element to a queue.
DSA Stack and Queue Report | Page 5
Q. What is Dequeue? The operation used to remove the first element from a queue.
Q. Which data structure is used in DFS? Stack.
Q. Which data structure is used in BFS? Queue.
Q. What is LIFO? Last In, First Out.
Q. What is FIFO? First In, First Out.
23. Conclusion
Stack and Queue are two important linear data structures in DSA. A Stack follows LIFO and works like a
stack of plates. A Queue follows FIFO and works like people standing in a line.
Remember: Stack fi Push, Pop, Peek. Queue fi Enqueue, Dequeue, Front. These concepts provide a
strong foundation for Linked Lists, Trees, Graphs, BFS, DFS, Recursion an
