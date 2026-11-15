TASK 2 DSA
THIS IS AN ALOGRITHM THAT WILL BE ABLE TO IMPLEMENT FACTORIALS OF ANY n NUMBER


a) Algorithm for each module

Stack module

init: set top = -1, which means the stack is empty.
isEmpty: return true if top == -1.
isFull: return true if top == MAX - 1.
push(value): if the stack is full, report overflow. Otherwise increase top by 1 and store the value at data[top].
pop: if the stack is empty, report underflow. Otherwise read data[top], decrease top by 1 and return the value.
peek: return data[top] without changing top.

Forward module (1 up to n)

Create an empty stack.
Push 1 (this is 1!).
For i = 2 to n:
Read the top of the stack, which is (i-1)!.
Multiply it by i to get i!.
Push i! onto the stack.
Pop the top of the stack, which is n!, and return it.

Backward module (n down to 1)

Create an empty stack.
For i = n down to 1, push i onto the stack.
Set result = 1.
While the stack is not empty:
Pop a value x.
Set result = result × x.
Return result, which is n!.

Main module

Read n and validate that 1 ≤ n ≤ 20.
Call the forward and backward modules.
Print both results and check that they are equal.
b) Stack as a data structure and its real-life applications

A stack is a linear data structure that follows the LIFO rule (Last In, First Out). The last element added is the first one removed, and all insertion and removal happens at one end called the top. It works like a pile of plates: you add a plate on top and you also take one from the top. The main operations are push (add), pop (remove), peek (view the top), isEmpty and isFull. Push and pop each take O(1) time.

Real-life applications:

Undo/Redo in text editors and graphics software. The latest action is the first to be undone.
Browser back button. Visited pages are stored on a stack.
Function calls and recursion. The operating system keeps a call stack of active functions, which is the same idea as the backward factorial.
Expression evaluation, such as converting infix to postfix and evaluating postfix.
Bracket matching in compilers, for example checking { [ ( ) ] }.
Backtracking, such as solving mazes or puzzles.
c) Implementation
Forward stack: it pushes 1!, 2!, ... n! in order, so n! ends up on top.
Backward stack: it pushes n down to 1, then pops and multiplies, which works like recursion unwinding.