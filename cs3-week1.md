## Recursion & Search Algorithms

**Iteration** - is the act of repeating a process, either to generate an unbounded sequence of outcomes, or with the aim of approaching a desired goal, target of result. Each repetition of the process is also called an "iteration", and the result of one iteration are used as the starting point for the next iteration.

**Recursion** - is a method where the solution to a problem depends on solution to a problem depends on a solution to smaller instances of the same problem \(as opposed to iteration\).

**Logarithm** - Is the inverse operation to exponentiation, just as division is the inverse of multiplication and vice versa. That means the algorithm of a number is the exponent to which another fixed number, the base, must be raised to produce that number.

The main thing we use logarithms for is solving for** x** when **x** is an **exponent**.

**Logarithm in binary search** - This comes up in time cost of binary search, which is an algorithm for finding a target number in a sorted list. 

1. **Start with the middle number: is it bigger or smaller than our target number?** Since the list is sorted, this tells us the if the target would be in the left half or the right half of the list. 
2. **We've effectively divided the problem in half**. We can "rule out"  the whole half of the list that we know doesn't contain the target number. 
3. **Repeat the same approach \(of starting in the middle\) on the new half-size problem**. Then do it again and again, until we either find the number or "rule out" the whole set. 



**Selection Sort**

* In selection sort, the idea of the algorithm is to find the smallest unsorted element and add it to the end of the sorted list. 

**In Pseudocode:** 

* Repeat until no unsorted elements remain:
  * Search the unsorted part of the data to find the smallest value.
  * Swap the smallest found value with the first element of the unsorted part.



Worse-case scenario: We have to iterate over each of the n elements of the array \(to find the smallest unsorted element\) and we must  repeat this process n times, since only one element gets sorted on each pass.  O\(n^2\)

* Best-case scenario: Exactly the same! There's no way to guarantee the array is sorted until we go through this process for all elements. Ω\(n^\)





