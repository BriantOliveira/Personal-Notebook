# LINK LIST

---

**Linked Lists** are a way to store data in which appending and prepending data is very fast. While looping through the data can be quite slow. A linked list is basically a chain of Nodes attached to each other.

The first concept we need to understand is the concept of **Reference vs Value**. In most computer science languages, there are two things a variable can be. It can either be a value like 1, 2, 3, 4... Or a reference to an object. What I mean by a reference is the value of the variable will be the location in which your object resides.

**Value Types**:  \(Int, Strings\)

If you pass variables by value, assigning a new variable to a value variable will give you a new variable with that constant value.

**Reference Types**:

If you pass a variable by reference, assigning a new variable to your current then changing your first will also change it for the second.

```
a = 7 #Value type
b = a #Reference type
print(a) 

>>> 7 
print(b) 

>>> 7

b = 3

print(a) 

>>> 7
print(b)

>>> 3
```

### Node

**DATA \| NEXT**

The first element of our Link list is the **Head** Reference and the **Tail** Reference is the last element &lt;&gt; \| both are Node.

The first thing we have to understand when creating a Linked List is something called a node. A node is used in multiple data structures in many different ways, but the concept of a node is the same. Nodes are used to store data and link to one or more other nodes.

Our node is going to have to elements. The first element of our node is going to be a data variable. This variable will be the element we want our Linked List to store. Then we will have a next variable which will point to the next node in our Linked List \(or None if we don't have a next\).

The Node does't know the **LAST**

#### Prepend

Prepend is quite a simple function. We start everything by creating a new node with its data variable defined. If our Linked List is empty then we set the head and tail to the reference of our node. If our Linked List is not empty, we set the next variable to the reference of the current head, and then set the head of our Linked List to our node that we just created. This function should run at O\(1\).

#### Append

Append is just like prepend, but we do add our node to the end of the Linked List. Like before we start by creating a Node. If our Linked List is empty then we assign the head and tail to our new node. If the list is not empty, we set the next variable in our current tail to the reference of our new node. Then we set the tail of our Linked List to the node we created. This function should run at O\(1\)

#### Find

We first get the head, and we get the next node using the next reference and we keep doing this until we have a node in which either our find function is true, or until we hit a next variable that is None. This function should run at best O\(1\) at worst O\(n\).

#### Delete

The most complicated of all the Linked List functions, but still quite simple. Like the find function, we get the head and keep getting the next node until we find the node we are looking for. Once we find the node we are looking for we set the last nodes next variable to the next variable in the node you want to delete. If the node was the list's head, assign the next variable to the next head. If the node was the tail, assign the tail to the reference to the last node.

##### Ex of link list:

\[\(5, "hi"\) --&gt; \(6, "w"\) --&gt; \(12, "h"\)...\]

Link list is different from an array, link list is just a reference to the **next** value.

Array:  \[1, 2, 3\]

##### Find:

* Check if we have a head
* Current = **Head**
* Current is not None \(conditional\)
* If item\(that you trying to find\) == current data \(whiled loop\)
* Current = current.next 

Let supposed that the item that you want to find is \(12, "h"\)

is \(5,"hi"\) = to \(12, "h"\)  **no**, so you go to the **next value** -&gt;-&gt;-&gt; \(6, "w"\) is = to \(12, "h"\) **no** -&gt;-&gt;-&gt; \(12, "h"\) is = \(12, "h"\) **yes** so we **return.**

##### **Delete:**

ex: \[1, 2, **3**, 4\]

* **Current** = **Head** & last = None
* Check if current is **not** None 
* If item is **==** to data  **\(IF YES  \| IF NO\)**
* If the current is = to the Tail \(current is a reference type\) \| Tail is = to last **\(YES\)**
* Last is none \| Head = current.next \| Else  last.next = current next **\(YES\)**
* **Last** = current **\(NO\)**
* **Current** = current.next **\(NO\)**

##### 

##### Double Link List:

**LAST\| DATA\| NEXT**

In the Double Link Link the **Node** does know the **LAST**

##### Reverse Link List:

\[1,2,3,4\]

**\|1\|**2,3,4

1**\|2\|**,3,4

2,1,**\|3\|**,4

3,2,1,**\|4\|**

4,3,2,1

1. Check if **NEXT** = **HEAD** . **NEXT**
2. **HEAD**.**NEXT** = **NONE**
3. **HEAD** = **NEXT**
4. While next is not none:
5. **Current** = **NEXT**
6. **NEXT** = **Current.NEXT**
7. Seek.**HEAD** = **Current**

```
def reverse(self):
        # Next node in the list
        next_node = self.head.next
        
        # Previous node in our list
        previous_node = self.head
        
		# Our head will be the tail after this is done
        self.tail = previous_node

        # Will be new last node so we don't want it's next to have anything
        self.head.next = None

        while next_node is not None:
            # Set our current node to the current next_node
            current_node = next_node
```



