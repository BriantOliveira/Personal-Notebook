## Recursion & Search Algorithms

**Iteration** - is the act of repeating a process, either to generate an unbounded sequence of outcomes, or with the aim of approaching a desired goal, target of result. Each repetition of the process is also called an "iteration", and the result of one iteration are used as the starting point for the next iteration.

**Recursion** - is a method where the solution to a problem depends on solution to a problem depends on a solution to smaller instances of the same problem \(as opposed to iteration\).

**Logarithm** - Is the inverse operation to exponentiation, just as division is the inverse of multiplication and vice versa. That means the algorithm of a number is the exponent to which another fixed number, the base, must be raised to produce that number.

The main thing we use logarithms for is solving for** x** when **x** is an **exponent**.

**Logarithm in binary search** - This comes up in time cost of binary search, which is an algorithm for finding a target number in a sorted list.

1. **Start with the middle number: is it bigger or smaller than our target number?** Since the list is sorted, this tells us the if the target would be in the left half or the right half of the list. 
2. **We've effectively divided the problem in half**. We can "rule out"  the whole half of the list that we know doesn't contain the target number. 
3. **Repeat the same approach \(of starting in the middle\) on the new half-size problem**. Then do it again and again, until we either find the number or "rule out" the whole set. 

#### **Selection Sort**

* In selection sort, the idea of the algorithm is to find the smallest unsorted element and add it to the end of the sorted list. 

**In Pseudocode:**

Repeat until no unsorted elements remain:

* Search the unsorted part of the data to find the smallest value.
* Swap the smallest found value with the first element of the unsorted part.

* **Worse-case scenario:** We have to iterate over each of the n elements of the array \(to find the smallest unsorted element\) and we must  repeat this process n times, since only one element gets sorted on each pass.  O\(n^2\)

* **Best-case scenario: **Exactly the same! There's no way to guarantee the array is sorted until we go through this process for all elements. Ω\(n^\)

#### Bubble Sort

* In bubble sort, the idea of the algorithm is to move the hight valued elements generally towards the right and the lower value element generally towards the left. 

**In Pseudocode:**

* Set swap counter to a non-zero value
* Repeat until the swap counter is 0: 
  * Reset swap counter is 0
  * Look at each adjacent pair
    * If two adjacent elements are not in order, swap them and add one to the swap counter.
* To know if the list is in order you set the counter back to 0 and check each adjacent pair - if the counter remains 0 means that the list is completely sorted.

* Worse-case scenario: The array is in reverse order; we have to "bubble" each of the_ n elements_ all the way across the array, and since we can only fully bubble one element into position per pass, we must do this _n times_. O\(n^2\)

* Best-case scenario: The array is already perfectly sorted, and we make no swap on the first pass. Ω\(n\)

#### Insertion Sort

* In insertion sort, the idea of algorithm is to build your sorted array in place, shifting element out of the way if necessary to make room as you go. 

**In Pseudocode:**

* Call the first element of the array "sorted".
* Repeat until all elements are sorted: 
  * Look at the next unsorted element. Insert into the "sorted" portion by shifting the requisite number of elements.

* **Worse-case scenario**: The array is in reverse order; we have to shift each of the _n elements n positions_ each time we make an insertion. O\(n\)
* **Best-case scenario**: The array is already perfectly sorted, and we simply keep moving the line between "unsorted" and "sorted" as we examine each element. Ω\(n\)



