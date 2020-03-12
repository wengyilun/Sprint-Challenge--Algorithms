y# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```



```
b)  sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

Answer:
# Question: how to know which floor egg starts breaking when

set a eggBroken flag to be false
set f (floor number) to be 1
while there are still floor to go AND eggBroken flag is false:
        throw out an egg
        if it's broken, set eggBroken flag to true and exit out the while loop
        else, continue to the next floor (f += 1) 

return floor number - 1 (the floor before the one that broke the egg)

# Run time complexity is 
Worst case will be O(f) if the floor that finally break the egg is at the topmost floor 
