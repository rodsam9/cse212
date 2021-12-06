# Sets

## Introduction
A set is one of 4 built-in data types in Python used to store collections of data, the other 3 are List, Tuple, and Dictionary, all with different qualities and usage. Sets are used to store multiple items in a single variable.
Sets are unordered, unindexed, and also the values stored in sets are unchangeable.

![Sets](images/set-operations.png)
## How To Create A Set
We can create a set by using curly brackets {} and entering strings, numbers, or booleans. Look at the samples below.
```py
set1 = {200, 1, 0, 45, -6} # All numbers/integers
set2 = {'cat', 'pizza', 'piano', 'dog', 'house'} # All string values
set3 = {True, False, False, True, False} # All boolean values
set4 = {1, True, 'tree', 'cow', 5, False} # Mixing them is valid as well.
```
## Add
When wanting to add items into a set, you can use add().
```py
set1 = {10, 20, 30}
set1.add(40) # Add 40 to set1
set1.add(50) # Add 50 to set1

```
You can also add one set to another by using update().
```py
set1 = {10, 20, 30}
set2 = {10, 40, 50}

set1.update(set2) # {10, 20, 30, 40, 50} 
# Since sets can't have duplicates , the 10 from set2 didn't get updated again on set1

```
## Remove
If you want to remove an item from a set, you can use remove(), or discard().
```py
set1 = {'cat', 5, 'cow', 3}

set1.remove('cat') # Removes cat from set1
set1.discard('cow') # Discards cow from set1
# set1 = {5, 3}

```
## Efficiency
Operations | Complexity
 --- | ---
 Add | O(1)
Remove | O(1)
There is a constant runtime complexity, so on average the effiency is O(1).
## Example / Practice
Go through each line of this practice problem and try to keep track of what's being added or removed from the set. Don't get fooled by duplicates, remember that when sets are combined, duplicates will be removed.

```py
animals = {'dog', 'cat', 'hamster', 'lion', 'shark', 'monkey'}
animals.add('gorilla')
animals.remove('gorilla')
animals.add('penguin')
animals.remove('dog')
animals.remove('cat')
animals.add('shark')
animals.add('horse')
animals.add('gorilla')
# What remains in the set animals?
```
<details>
<summary markdown="span">See the solution!</summary>

```py
animals = {'dog', 'cat', 'hamster', 'lion', 'shark', 'monkey'}
animals.add('gorilla') # {'dog', 'cat', 'hamster', 'lion', 'shark', 'monkey', 'gorilla'}
animals.remove('gorilla') # {'dog', 'cat', 'hamster', 'lion', 'shark', 'monkey'}
animals.add('penguin') # {'dog', 'cat', 'hamster', 'lion', 'shark', 'monkey', 'penguin'}
animals.remove('dog') # {'cat', 'hamster', 'lion', 'shark', 'monkey', 'penguin'}
animals.remove('cat') # {'hamster', 'lion', 'shark', 'monkey', 'penguin'}
animals.add('shark') # shark is already in the set so you can't add a duplicate
animals.add('horse') # {'hamster', 'lion', 'shark', 'monkey', 'penguin', 'horse'}
animals.add('gorilla') # {'hamster', 'lion', 'shark', 'monkey', 'penguin', 'horse', 'gorilla'} <- Solution!
```
</details>

## Problem To Solve
Okay it seems like you're getting the hang of sets. Let's test out what you've learned so far! Try solving this practice problem!
```py

def add_sets(set1, set2):
    # Write code here that will update or add one set to the other.

def remove_odd(set1):
    # Write code here that will remove odd numbers in a set.

def remove_even(set1):
    # Write code here that will remove even numbers in a set.

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
Solution to [Problem To Solve](set-solution.md)

Go back to [Welcome Page](0-welcome.md)!