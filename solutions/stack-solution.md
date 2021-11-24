```py
class Stack:

    def __init__(self):
        self.stack = []

    def push(self, item):
        # Add code here
        return self.stack.append(item)

    def pop(self):
        # Add code here
        return self.stack.pop()

    x = Stack()
    x.push('monkey')
    x.push('lion')
    x.pop()
    x.push('bird')
    print(self.stack) # Results ['monkey', 'bird']

```