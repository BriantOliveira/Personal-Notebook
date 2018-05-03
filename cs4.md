## Class 1: Bit Manipulation

Bitwise Operations

And **&**

Or **\|**

XOR **^ \(**Either one of the other**\)**

NOT** ~ \(**Flips the value**\)**

LEFT SHIFT **&lt;&lt;**

RIGHT SHIFT **&gt;&gt;**

**And** - Only true if both input bits are true

0 & 0 = 0

1 & 0 = 0

0 & 1 = 0

1 & 1 = 1

**XOr** - True if any input bit is true

0 \| 0 = 0

1 \| 0 = 1

0 \| 1 = 1

1 \| 1 = 0

**Left shift **-  Shift the binary digits by n, pad 0's on the right. Each shift is a multiply 2 \(unless there's overflow\)

```
00010110
<<
00000010
_________
01011000
```

**Right shift** - Shift the binary digits by n, pad 0's on the right. Each shift is a divide by 2 with round towards negative infinity.

**Set Bit**

```
int setBit(int x, unsigned char position) {
    int mask = 1 << position; 
    return x | mask;
}
```

**Clear Bit**

```
int clearBit(int x, unsigned char position) {
    int mask = 1 << position;
    return x & ~mask;
}
```

**Flip Bit**

```
int flipBit(int x, unsigned char position) {
    int mask = 1 << position;
    return x & ^mask;
}
```

**Is Bit Set**

```
bool isBitSet(int x, unsigned char position) {
    int shifted = x << position;
    return shifted x & 1;
}
```

**Modify a Bit**

```
int modifyBit(int x, unsigned char position, int state) {
    int mask = 1 << position;
    return (x & ~mask) | (-state & mask);
}
```

---

### Class 3

**Priority Queue Application **

* Prioritizing data packets in route. 
* Tracking unexplored routes in path-finding. 
* Bayesian span filtering 
* Data compression
* OS: load balancing, interrupt handling.

**Priority Queue**

You can build a priority queue with two queues. Where one queue with dequeue and goes to the queue that has it's priority.

_Array representation \(unordered\)._

* Perhaps the simplest priority queue implementation is based on our code for pushdown stacks. The code for _insert \_in the priority queue is the same as for \_push \_in the stack. To implement \_remove the maximum_, we can add code like the inner loop of selection sort to exchange the maximum item with the item at the end and the delete that one, as we did with pop\(\) for stacks. Program implements a priority queue using this approach.

* _Array representation \(ordered\)._  
  Another approach is to add code for  
  \_insert \_to move larger entries one position to the right, thus keeping the entries in the array in order \(as in insertion sort\). Thus the largest item is always at the end, and the code for \_remove the maximum \_in the priority queue is the same as for \_pop \_in the stack. Program implements a priority queue using this approach.

* _Linked-list representations \(unordered and reverse-ordered\)._  
  Similarly, we can start with our linked-list code for pushdown stacks, either modifying the code for pop\(\) to find and return the maximum or the code for push\(\) to keep items in reverse order and the code for pop\(\) to unlink and return the first \(maximum\) item on the list.  



