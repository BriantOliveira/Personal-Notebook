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

var LL = new LinkedList();
```



