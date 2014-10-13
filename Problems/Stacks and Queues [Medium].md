##Stacks/Queues [Medium]

######Queue with two stacks
Implement a queue with two stacks so that each queue operations takes a constant amortized number of stack operations.

Alternatively: design a stack using 2 queues

######Stack with max
Create a data structure that efficiently supports the stack operations (push and pop) and also a return-the-maximum operation. Assume the elements are real numbers so that you can compare them. 

######King and Knight
Given a king and a knight on an infinite chessboard (no boundary), each takes turn to move (i.e. the king moves first, then the knight can move, then the king moves again and so on). Find the minimum number of moves until they meet at the same square. What is the time and space complexity of your solution?

######Implement Peek min/max/middle on a stack
Add three additional methods to a generic stack data structure. Write a peek for the min, max and middle value. This should not change the original stack. Assume all items in the stack are of the same type or have a compare function for the respective language.

######Infix to Postfix Conversion
Given an expression in infix notation return it in postfix notation. An infix expression is one in which operators are located between their operands. In postfix notation, the operator immediately follows its operands. ‘X + Y’ becomes ‘XY+’ in postfix notation.
Example:	3+4 → 3 4 +
(300+23)*(43-21)/(84+7) → 300 23 + 43 21 - * 84 7 + /


######Topological sort
Given a set of tasks and their dependency graph (i.e. edge (u, v)  means that task u depends on task v and must be completed after v; tasks can have multiple dependencies). Assume that there is no circular dependency, return an execution order of these tasks such that the dependencies are satisfied. 

Example: 
Input: 1 => 2; 3=>1; 2 => 4; 3=>4
Output: 4, 2, 1, 3

Note: There can be many possible orders, just need to return one. The number of tasks <= 10,000.

######Duplicate parenthesis
Give an algorithm for finding duplicate parenthesis in a expression. 
{{ (( a + b ) * (( c + d ))) }}
Tower of Hanoi
In the classic problem of the Towers of Hanoi, you have 3 towers and N disks of different sizes which can slide onto any tower. The puzzle starts with disks sorted in ascending order of size from top to bottom (i.e., each disk sits on top of an even larger one). You have the following constraints:			
(1) Only one disk can be moved at a time.
(2) A disk is slid off the top of one tower onto the next rod.
(3) A disk can only be placed on top of a larger disk.
Write a program to move the disks from the first tower to the last using Stacks. 
				
######Reverse a Stack using recursion
You can use only functions available with the stack push(), pop(), top(), isEmpty()

######Implement LRU Cache
How to implement LRU caching scheme? What data structures should be used?
We are given total possible page numbers that can be referred. We are also given cache (or memory) size (Number of page frames that cache can hold at a time). The LRU caching scheme is to remove the least recently used frame when the cache is full and a new page is referenced which is not there in cache. 

