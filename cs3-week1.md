# Week 1

---

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

#### Linear Search

* In linear search, the idea of the algorithm is to iterate across the array from left to right, searching for a specified element.

**In Pseudocode:**

* Repeat, starting at the first element:

  * If the first element is what you're looking for \(the target\), stop. 
  * Otherwise, move to the next element.

* **Worse-case scenario**: We have to look through the entire array of n elements, either because the target element is the last element of the array or doesn't exist in the array at all. O\(n\)

* **Best case scenario**: The target element is the first element of the array, and so we can stop looking immediately after we start. Ω\(1\)

#### Binary Search

* In binary search, the idea of the algorithm is to divide and conquer, reducing the search area by half each time, trying to find a target number. 
  * In order to leverage this power however, our array must first be sorted, else we cannot make assumptions about the array's contents.

**In Pseudocode:**

* Repeat until the \(sub\)array is of size 0:

  * Calculate the middle point of the current \(sub\)array.
  * If the target is at the middle, stop. 
  * Otherwise, if the target is greater than what's at the middle, repeat, changing the end point to be just the left of the middle. 
  * Otherwise, if the target is greater than what's at the middle, repeat, changing the start point to be just to the right of that middle.

* Worse-case scenario: We have to divide a list of n elements in half repeatedly to find the target element, either because the target element will be found at the end of the last division or doesn't exist in the array at all. O\(log n\)

* Best-case scenario: The target element is at the midpoint of the full array, and so we can stop looking immediately after we start. Ω\(1\)

#### Recursion

* We might describe an implementation of an algorithm as being particularly "elegant" if it solves a problem in a way that is both interesting and easy to visualize. 
* The technique of recursion is a very common way to implement such an "elegant" solution. 
* The definition of a recursive function is on that, as part of it's execution, invokes itself.
  * The factorial function \(n!\) is defined over all positives integers. 
  * n! equals all the positive integers less than or equal to n, multiplied together. 
  * Thinking in terms of programming, we'll define the mathematical function n! as fact\(n\)

```
fact(1) = 1
fact(2) = 2 * 1 
fact(3) = 3 * 2 * 1
fact(4) = 4 * 3 * 2 * 1
fact(5) = 5 * 4 * 3 * 2 * 1
```

fact\(n\) = n \* fact\(n-1\)

* This forms the basis for a recursive definition of the factorial function
* Every recursive function has two cases that could apply, given any input. 
  * The base case, which when triggered will terminate the recursive process. 
  * The recursive case, which is where the recursion will actually occur. 

```
int fact(int n)
 {
   if (n == 1)
     return 1;
   else 
     return n * fact(n-1);
 }
```

* In general, but not always, recursive function replace loops in non-recursive functions. 

```
int fact2(int n)
{
    int product = 1;
    while (n > 0)
    {
        product *= n;
        n--;
    }
    return product;
}
```

* It's also possible to have more than one base or recursive case, if the program might recurse or terminate in different ways, depending on the input being passed in.

#### Merge Sort

Merge Sort does log n merge steps because each merge step double the list size.

It does n work for each merge step because it must look at every item.

So it runs in O\(n log n\).

#### Palindrome -

**Is a word, phrase, number, or other sequence of characters which reads the same backward as forward.**

In automata theory, as set of all palindromes in a given alphabet is a typical example of language that is context-free, but not regular. This means that it is impossible for a computer with a finite amount of memory to reliably test for palindromes on one pass. It is possible to find the longest palindromic substring of a given input string in a linear time.

#### String Searching algorithm -

Usually called as z matching algorithms, are an important class of string algorithms that **try to find a place where one or several strings \(also called patterns\) are found within a large string or text.**

In practice, how the string is encoded can affect the feasible string search algorithms. In particular if a variable width encoding is in use then it may be slower to find the Nth character \(perhaps requiring time proportional to N\). This may slow down some search algorithms.

#### Permutation -

In mathematics, the notion of permutation relates to **the act of arranging all the members of a set into some sequence or order, or if the set is already ordered, rearranging \(reordering\) its elements.**

#### Anagram -

Is the word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

#### Unit Testing -

Is a software testing method by which individual units of source code, set of one or more computer program modules together with associated control data, usage procedures, are tested to determine whether they are fit for use.

---

# Week 2

#### **Abstract Data Type \(ADT\)** -

Is a mathematical model for data types, where a data type is defined by its behavior \(semantics\) from the point of view of a user of the data, specifically in terms of possible values, possible operations on data of this type, and the behavior of these operations.

**Arrays** -

* Contiguous piece of memory. 
* Same size storage space at each index. 
* Static - Memory allocated once, size can't change. 
* Dynamic - New memory allocated, array copied to grow. 

**Linked List -**

Not contiguous piece of memory.

Differing size storage space at each index.

Dynamic - New \(small\) piece of memory allocated.

No need to copy the whole thing like an array.

**Linked List run time:**

Access Element via Index - **O\(n\)**

Find and Insert or Delete Element\(Beginning\) - **O\(1\)**

Find and Insert or Delete Element \(Middle\) - **O\(n\)**

Find and Insert or Delete Element \(End\) - **O\(n\)**

