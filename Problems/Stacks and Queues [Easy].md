##Stacks/Queue [Easy]


######Balanced Parentheses
Write a function which checks if parentheses in a given expression are balanced.
Example: 	(5+6)*(7+8)/(4+3)  - balanced parentheses
		(4+5)*(2+(4-7)       - not balanced parentheses
		(7+8)*{3-[5+6]*4}   - balanced parentheses

######Ascending Order
Write a program to sort a stack in ascending order (with biggest items on top). You may use at most one additional stack to hold items, but you may not copy the elements into any other data structure (such as an array). The stack supports the following operations: push, pop, peek, and isEmpty. 

######Postfix expression
Given an expression in postfix notation evaluate it. In postfix notation operands are followed by operations. For example, X+Y becomes XY+ in postfix notation.
Example:	5 6 + → 11
		23 17 + 45 5 - - → 0

######Snake
You’re to write a game to paint a snake on the screen. At every time interval, the player must move the head of the snake in any of the 3 directions (other than going backward), the body of the snake will move along. The game is over when the snake hits its own body or the screen boundary. Design the API and data structure to use.

class Snake:
    def __init__(self, snake_length, board_length,
 tail_start, orientation):
        self.queue = Queue(snake_length)
        self.board_length = board_length

    def is_backward(self, next_pos):
       
    def is_losing_move(self, next_pos):
        # check if hit end
        # check if run into body 

    def make_move(direction):

######Permutations / Combinations
Print all permutations of N elements in an array.
Print all combinations of N elements in an array (each element is chosen at most once in any combination).             

######Find Moving Averages and Maximums
Given an infinite stream of numbers in time order, at any given time:
Find moving averages of the last K numbers.
Find the maximums of the last K numbers (maybe medium problem)

######Design a Queue using an array
Develop the push | pop | peek | isEmpty functions for a queue using an array as the internal data structure.
Removing all elements recursively
Write a recursive function that will remove all the elements in a stack and/or if you have time, write a recursive function that removes all elements in a queue.

######Design a Stack using an array
Develop the push | pop | peek | isEmpty functions for a stack using an array as the internal data structure.
 
######Implement two stacks in an array
Create a data structure twoStacks that represents two stacks. Implementation of twoStacks should use only one array, i.e., both stacks should use the same array for storing elements. Following functions must be supported by twoStacks.
push1(int x) –> pushes x to first stack
push2(int x) –> pushes x to second stack
pop1() –> pops an element from first stack and return the popped element
pop2() –> pops an element from second stack and return the popped element
Implementation of twoStack should be space efficient.

######Find the first circular tour that visits all petrol pumps
Suppose there is a circle. There are n petrol pumps on that circle. You are given two sets of data.
1. The amount of petrol that petrol pump will give.
2. Distance from that petrol pump to the next petrol pump.
Calculate the first point from where a truck will be able to complete the circle (The truck will stop at each petrol pump and it has infinite capacity). Expected time complexity is O(n). Assume for 1 litre petrol, the truck can go 1 unit of distance.
For example, let there be 4 petrol pumps with amount of petrol and distance to next petrol pump value pairs as {4, 6}, {6, 5}, {7, 3} and {4, 5}. The first point from where truck can make a circular tour is 2nd petrol pump. Output should be “start = 1″ (index of 2nd petrol pump).
