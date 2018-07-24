**Constructor Function** - is simply a function that creates an object class and allows you to create multiple instance of that class \(allows to create multiple objects that all have the same properties and same functionality, because they are part of the same class\).

```
Function User(firstName, lastName, age, gender) {
    this.firstName = firstName;
    this.lastName = lastName;
    this.age = age; 
    this.gender = gender;
};

var user1 = new User('John', 'Doe', 25, 'male');
```

**Prototype Object** - is a simply an object that multiple other objects can refer to get any information or functionality that they need for our needs.

```
User.prototype.emailDomain = '@facebook.com';
```

**Linked List**

```
function LinkedList() {
    this.head = null;
    this.tail = null;
}

function Node(value, next, prev) {
    this.value = value;
    this.next = next;
    this.prev = prev;
}


//var node1 = new Node(100, 'node2', null);

// adding a method to the linked list
LinkedList.prototype.addToHead = function(value) {
    var newNode = new Node(value, this.head, null);
    //If LinkedList is not empty
    if (this.head) this.head.prev = newNode;
    // If LinkedList is empty
    else this.tail = newNode;
    this.head = newNode;
}

LinkedList.prototype.addToTail = function(value) {
    var newNode = new Node(value, null, this.tail);
    if (this.tail) this.tail.next = newNode;
    else this.head = newNode;
    this.tail = newNode;
}

LinkedList.prototype.removeHead = function() {
    if (!this.head) return null,
    var val = this.head.value;
    this.head = this.head.next;
    if (this.head) this.head.prev = null;
    else this.tail = null;
    return val;
}

var myLL = new LinkedList()

myLL.addToTail(10);
myLL.addToTail(20);
myLL.addToTail(30);


console.log(myLL.tail.prev.prev);
```



