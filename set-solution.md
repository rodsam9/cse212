```py
def add_sets(set1, set2):
    # Write code here
    set1.update(set2)
def remove_odd(set1):
    # Write code here that will remove odd numbers in a set.
    for i in set1:
        if i % 2 != 0:
            set1.remove(i)
def remove_even(set1):
    # Write code here that will remove even numbers in a set.
    for i in set1:
        if i % 2 == 0:
            set1.remove(i)
            
s1 = {5, 10, 15, 20}
s2 = {20, 25, 30, 35}
s3 = {1, 10, 20, 40}

print(add_sets(s1, s2)) # Should display {5, 10, 15, 20, 25, 30 ,35}
print(add_sets(s1, s3)) # Should display {1, 5, 15, 20, 40}
print(add_sets(s2, s3)) # Should display {1, 10, 20, 25, 30, 35, 40}
print(remove_odd(s1)) # Should display {10, 20}
print(remove_odd(s2)) # Should display {20, 30}
print(remove_even(s3)) # Should display {10, 20, 40}
```

Go back to [Sets Page](2-set.md)!