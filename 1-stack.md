# Stacks

## Introduction
A stack is a linear data structure for which operations are carried out in a specific order. The sequence could be LIFO (Last In First Out) or FILO (First In Last Out) (First In Last Out). You will learn how to Push and Pop!

![Pushing and Popping](images/stack-structure.png)

## Push

In order to push or add elements into a stack, you can use the append() method to push an element to the top of the stack. Here goes an example on how to use append().

```py
stack = []

stack.append(1)
stack.append(100)
stack.append(200)
stack.append(300)
stack.append(1000)

print(stack)
# [ 1, 100, 200, 300, 1000 ]
```
## Pop

In order to pop or remove elements from a stack, you can use the pop() method, which removes the top item from the stack. Here goes an example on how to use pop().

```py
print(stack.pop())  # removes number 1000
print(stack.pop())  # removes number 300

print(stack)
# What remains from the stack.
# [ 1, 100, 200]
```

## Efficiency
Operations | Complexity
 --- | ---
 Pop | O(1)
Push | O(1)
Since we do not run into any loops in the push or pop methods, the effiency is O(1).


## Example / Practice 
Go through each line of this practice problem and try to keep track of what's being pushed or popped. Remember, push is when an element is added to the end of the stack, while pop removes the last one added.


```py
stack = []

stack.append(1)
stack.append(100)
stack.append(200)
stack.pop()
stack.append(300)
stack.append(1000)
stack.pop()
stack.pop()
stack.pop()

# Figure out what remains in the stack.
print(stack)
```
<details>
<summary markdown="span">See the solution!</summary>

```py
stack = [] # Empty stack

stack.append(1) # [1]
stack.append(100) # [1, 100]
stack.append(200) # [1, 100, 200]
stack.pop() # [1, 100]
stack.append(300) # [1, 100, 300]
stack.append(1000) # [1, 100, 300, 1000]
stack.pop() # [1, 100, 300]
stack.pop() # [1, 100]
stack.pop() # [1]

print(stack) # [1] This is the answer
```
</details>

## Problem To Solve

Let's see if you're ready to take on stacks!

Here we have a class called Stack. We have some functions that are not completed. Finish the push and pop functions in order to print out the results.

```py
class Stack:

    def __init__(self):
        self.stack = []

    def push(self, value):
        # Add code here

    def pop(self):
        # Add code here

    x = Stack()
    x.push('monkey')
    x.push('lion')
    x.pop()
    x.push('bird')
    print(self.stack)

```
Solution to [Problem To Solve](stack-solution.md)


Go back to [Welcome Page](0-welcome.md)!
