```py
def _insert(self, data, node):
        # Checking to see if numbers in data are equal to node.
        if data == node.data:
            # If same numebr in, then return none
            return None
        if data < node.data:
            # The data belongs on the left side.
            if node.left is None:
                # We found an empty spot
                node.left = BST.Node(data)
            else:
                # Need to keep looking.  Call _insert
                # recursively on the left sub-tree.
                self._insert(data, node.left)
        else:
            # The data belongs on the right side.
            if node.right is None:
                # We found an empty spot
                node.right = BST.Node(data)
            else:
                # Need to keep looking.  Call _insert
                # recursively on the right sub-tree.
                self._insert(data, node.right)
tree = BST()
tree.insert(5)
tree.insert(3)
tree.insert(7)
# Shouldn't print these duplicates
tree.insert(3) # Doesn't get inserted
tree.insert(7) # Doesn't get inserted
# These should be inserted since they aren't duplicates.
tree.insert(10)
tree.insert(8)
for x in tree:
    print(x)
#output: 3, 5, 7, 8, 10
```
Go back to [Tree Page](3-tree.md)!