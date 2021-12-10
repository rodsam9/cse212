# Tree

## Introduction
Trees are made up of parent and child nodes, and are extremely valuable data structures. Because the nodes do not appear next to one another within memory, these appear similar to linked lists. They begin with a root node and then branch out as they go.

## Recursion
Before dealing with Trees, you must first grasp what recursion is and how it is used. Recursion is when your calling the same function in within itself and it won't stop till it reaches a set of conditions. The first condition is a base case. It's a condition that will stop the function from calling itself. It is important to have this base case or it will loop many times.
Here's an example of recursion being used.
```py
# Can you figure out what's the base case in this function?
def sum_squares_recursive(n):
    if n <= 0: 
        return 0
    else:
        return n * n + sum_squares_recursive(n - 1) 

print(sum_squares_recursive(10)) # And what number should be printed here?
```
<details>
<summary markdown="span">See the solution!</summary>

```py
def sum_squares_recursive(n):
    # Check if value is less than or equal to 0
    if n <= 0:  # Here we have our base case.
        # Then return 0
        return 0
    else:
        return n * n + sum_squares_recursive(n - 1) # Notice how we call the same function inside it's function, that's RECURSION.

print(sum_squares_recursive(10))  # Should print 385
```
</details>

## Binary and Binary Search Trees
### Binary Tree
In a binary tree, every node has 0 to 2 children.

<img src="images/binary-tree.png" width="400">

### Binary Search Tree
In a binary search tree, every node has 0 to 2 children, and the large nodes are sorted on the right and smaller nodes sorted on the left. When a node splits into other nodes, this is a parent node, and the ones under are children nodes. Any node that doesn't branch off anymore is a leaf.

<img src="images/binary-search-tree.png" width="400">

## Efficiency
Operations | Complexity
 --- | ---
 Insert | O(log n)
Remove | O(log n)
Contains | O(log n)
A binary search tree is extremely efficient! It doesn't take as long as a linked list to find a specific node. The reason why it doesn't take long is because of the ability to cut everything in half to find a specific node.

## Problem To Solve

Let's see if you're ready to take on trees!

```py
class BST:

    class Node:
            self.data = data
            self.left = None
            self.right = None

    def __init__(self):
        self.root = None

    def insert(self, data):
        if self.root is None:
            self.root = BST.Node(data)
        else:
            self._insert(data, self.root)
# Fix _insert() so that you can insert a node with data into the tree. Also, implement no duplicates being added to BST.
    def _insert(self, data, node):
        if data < node.data:
            if node.left is None:
                node.left = BST.Node(data)
            else:
                self._insert(data, node.left)
        else:
            if node.right is None:
                node.right = BST.Node(data)
            else:
                self._insert(data, node.right)
    tree = BST()
    tree.insert(5)
    tree.insert(3)
    tree.insert(7)
    # Shouldn't print these duplicates
    tree.insert(3)
    tree.insert(7)
    # These should be inserted since they aren't duplicates.
    tree.insert(10)
    tree.insert(8)
    for x in tree:
        print(x)
    # What's the output?

```

Solution to [Problem To Solve](tree-solution.md)


Go back to [Welcome Page](0-welcome.md)!