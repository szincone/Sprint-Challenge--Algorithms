Add your answers to the Algorithms exercises here.
## I
1.
```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```
Pretty sure this would be O(n). Because you're adding 2n to a on each pass, that should negate the 2n in the param. This would means it's effectively equal too, `while (a < n)`. So it would be O(n) since it's only scaling w/ the 1 changing input.

2.
```
b)  sum = 0
    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1
```
Pretty sure this would be, O(n^4). I think each loop would make it grow exponentially for eveery loop.

3.
```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```
Pretty sure this would be depending, like best case, bunnies == 0, O(1). Worst case, I think this would be very bad. I'd say O(2^n) because I think the recursion could start to add up really quickly.


## II
I would try to take a binary approach.
1. Go to middle floor
2. Throw egg
3. If break, pick new floor below, if no break, new floor above.
4. New floor would be half of the remaining stairs for either direction.
5. Repeats until I find what _f_ equals.