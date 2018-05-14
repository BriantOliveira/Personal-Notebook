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

* Almost always implemented with a heap
* Elements with smaller numbers are higher priority
* Elements are inserted in O\(log n\) time with a heap instead of O\(n\) time with a sorted array or linked list. 
* Ordering happens during each insertion and deletion, so the cost of ordering is distributed across insertion and deletion operations instead of in one big chunk.

You can build a priority queue with two queues. Where one queue with dequeue and goes to the queue that has it's priority.

_Array representation \(unordered\)._

* Perhaps the simplest priority queue implementation is based on our code for pushdown stacks. The code for _insert \_in the priority queue is the same as for \_push \_in the stack. To implement \_remove the maximum_, we can add code like the inner loop of selection sort to exchange the maximum item with the item at the end and the delete that one, as we did with pop\(\) for stacks. Program implements a priority queue using this approach.

* _Array representation \(ordered\)._  
  Another approach is to add code for  
  \_insert \_to move larger entries one position to the right, thus keeping the entries in the array in order \(as in insertion sort\). Thus the largest item is always at the end, and the code for \_remove the maximum \_in the priority queue is the same as for \_pop \_in the stack. Program implements a priority queue using this approach.

* _Linked-list representations \(unordered and reverse-ordered\)._  
  Similarly, we can start with our linked-list code for pushdown stacks, either modifying the code for pop\(\) to find and return the maximum or the code for push\(\) to keep items in reverse order and the code for pop\(\) to unlink and return the first \(maximum\) item on the list.

**Complete Binary Tree**

* Every level except possibly last is completely filled and nodes are as far left as possible. 
* Almost perfect Binary Tree.
* Height: O\(log2 n\).

**Binary Heap Definition**

* A complete binary tree.
* Satisfies heap ordering property.
* Min-heap - each node is greater than or equal to its parent \(min value is root\).
* Max-heap - each node is less than or equal to its parent \(max value is root\).

**Note about ordering**

* Heaps are not sorted, instead they are considered "partially ordered".
* Max element is at the root, but we don't know where min element is only it must be a leaf. 

**Array Representation**

Items stored in \(dynamic\) array following level-order traversal.

Calculate parent-child index relationships with arithmetic.

* Left child index 2\*i + 1
* Right child index 2\*i + 2
* Parent index: \(i - 1\) / 2

**Advantages**

Uses less memory than binary tree represented with nodes \(avoids node objects containing 3 pointers: data, left, right child\)

Allows sorting an array in-place \(heap sort\)

**Insert**

1. Add element to end
2. Sift up \(aka bubble up, percolate up, trickleup\)
3. Swap with parent up to the root until path fulfills heap ordering property. 

**Delete Min/Max**

1. Replace root with last element
2. Sift down 
3. Swap with smaller child \(min\) or larger child \(max\) until trio fulfills heap ordering property. 

**Other Methods **

Peek \(Aka find-min or find-max\) returns the root value.

Size \(Aka count or length\) return number of elements.

### **Heapify**

* Input is an array \(usually unsorted, unordered\). 
* Output is an array that satisfies the binary heap ordering property. 

```
# Start at last parent node
Index = (size - 2) / 2
while index >=0:
# Sift down element at index 
index -=1
```

**Heap Sort**

Heapify array

```
while (count > 0):
    find-min or find-max element (peek)
    delete-min or delete-max element
```

---

### **Class 4**

**Tree Rotation**

In discrete mathematics, **tree rotation **is an operation on a binary tree that changes the structure without interfering with the order of the elements. A tree rotation moves one node up in the tree and one node down. It is used to change the shape of the tree, and in particular to decrease its height by moving smaller subtrees down and larger subtrees up, resulting in improved performance of many tree operations.

There exists an inconsistency in different descriptions as to the definition of the **direction of rotations**. Some say that the direction of rotation reflects the direction that a node is moving upon rotation \(a left child rotating into its parent's location is a right rotation\) while others say that the direction of rotation reflects which subtree is rotating \(a left subtree rotating into its parent's location is a left rotation, the opposite of the former\). This article takes the approach of the directional movement of the rotating node.

**AVL Tree**

* Is a height balanced binary search tree.

* AVL trees implement the standard Dictionary data type methods, fetch, insert, delete, split and join -- each has O \(log n\) run time for trees containing n nodes.

* The difference between heights of left and right subtrees cannot be more than one for all nodes.

* The height of an AVL tree is always O\(Log n\) where n is the number of nodes in the tree.

**Insert**

* Attach the new node as a leaf according to symmetric order with respect data key k. Set balance of the new node to zero. Back-out of tree adjusting balance fields and restructuring as needed until tree is AVL again.

* For insertion in AVL tree, we first perform standard BST insertion of the node and then rebalance the BST by left or right rotation.

* After insertion if the tree is not balanced then following 4 cases might occur:

  * Left Left case
  * Left Right case
  * Right Right case
  * Right Left case

Case 1: Left Left Case y is the left child of z and x is the left child of y.

```
struct Node * insert(struct Node* node, int key)
{
    if(node == NULL)
        return (newNode(key));
    if (key < node ->key)
        node -> left = insert(node -> left,key);
    else if (key > node -> key)
        node -> right = insert (node -> right, key);
    else // Equals key are not allowed in BST
        return node;

    node -> height = 1 + max(height(node -> left),
                    height(node -> right));
    //Left Left Case
    if (balance > 1 && key < node -> left ->key)
        return rightRotate(node);

    // Right Right Case
    if (balanced < -1 && key > node -> right -> key)
        return leftRotate(node);
    // Left Right Case
    if (balance > 1 && key > node -> left -> key)
        {
            node -> left = leftRotate(node -> left);
            return rightRotate(node);
        }
    // Right Left Case
    if (balance > 1 && key > node -> right -> key)
    {
        node -> left = rightRotate(node -> right);
        return leftRotate(node);
    }
```

**Splay Tree **

Is a self-adjusting binary search tree with the additional property that recently accessed elements are quick to access again.  

