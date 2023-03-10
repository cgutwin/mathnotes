## Running Times
- Possible to reverse in constant time: see [[#Doubly-Linked Lists#Reversal in Constant Time]]
	- Need to use a doubly-linked list.

|Operation|Linked List|Double Linked List|
|-|-|-|
|get/set| O(N)| O(N)|
|Find element|O(N)|O(N)|
|Insert at beginning|O(1)|O(1)|
|Insert at end|O(1)|O(1)|
|Insert in middle|O(1)|O(1)|
|Remove from middle|==O(N)==|==O(1)==|
| Remove from beginning|O(1)|O(1)|
|Remove from end|==O(N)==|==O(1)==|




## Common Methods
### Inserts at Head
Inserts at head need to make the new head point to the old head.
1. Create new node `newNode`
2. Make `newNode.next` point to `head`
3. Update the `head` to be `newNode`
- If the tail is null, the list was empty, so make `tail` point to the `head`.
#### Code
```java
public void addLeft(T item) {  
    Node leftNode = new Node();  
    leftNode.item = item;  
    // A left node will be the new head of the linked list,
    // point to the old one.  
    leftNode.next = head;  
  
    // If there was a head (list wasn't empty), make the old
    // head point back to the new node.  
    if (head != null) {  
        head.prev = leftNode;  
    }  
  
    // Update the head.  
    head = leftNode;  
  
    // If tail is null, the list was empty to begin with, so the
    // head is the tail.  
    if (tail == null) {  
        tail = head;  
    }  
  
    size++;  
}
```


### Inserts at Tail
Inserts at the tail need to make the old tail point to the new one.
- If the head null, the list is empty, so make `head` the new node and the `tail = head`, else
1. Make `tail.next` the `newNode`
2. Update the tail to `tail = newNode`
#### Code
```java
public void addRight(T item) {  
    Node rightNode = new Node();  
    rightNode.item = item;  
  
    // If the list is empty, the head and tail are the same.  
    if (head == null) {  
        head = rightNode;  
        tail = head;  
    } else {  
        // The tail needs to point to the new right node.  
        tail.next = rightNode;  
        // The new right node needs to point back to the old
        // tail.  
        rightNode.prev = tail;  
        // Update the tail.  
        tail = rightNode;  
    }  
  
    size++;  
}
```

### Removals at Head
Need to make the current head of the list be `head.next`.
1. Temp store `head` and update `head = head.next`.
2. Check if the new head is null. If it is, the list is now empty
	1. Update `tail` to be null.
3. `size--`
- Return `oldHead` if required.

#### Code
```java
public T removeLeft() {  
    if (isEmpty()) throw new NoSuchElementException("List is empty.");  
  
	// "Pop" the old head and make the new one the next element
    // in the list.  
    Node oldHead = head;  
    head = oldHead.next;  
    
    // If the new head exists (the list isn't now empty), make
    // the prev pointer null as nothing ahead.  
    if (head != null) {  
        head.prev = null;  
    }  
    // Else it's empty so make tail null too.  
    else {  
        tail = null;  
    }  
    
    size--;  
    
    return oldHead.item;  
}
```
### Removals at Tail
More difficult than removing from the head. To make easier, a [[#Doubly-Linked Lists|Double-Linked List]] would work in O(1) time, with the drawback of more space used for pointer to tail.
- Need to traverse the list until it hits a node with a null `next` value.
1. If `head.next == null` then the list has one element.
	1. Make the head null.
2. Traverse the list from the head
	1. While `node.next.next != null`, make the current node the next node.
		- Need to target `node.next.next`, so there's no `NullPointerException` when updating the current node.
	2. Store the last node's data, and disconnect it from the list by making `node.next == null`.
3. Reduce the size and return the data if required.

#### Code
```java
public T removeFromTail() {
        if (head == null)
            throw new NoSuchElementException("My linked list is empty");
            
        T ret;
        if (head.next == null) {
            ret = head.data;
            head = null;
        } else {
            LinkedListNode node = head;
            while (node.next.next != null)
				// node is the one before last
                node = node.next;
                // remember the last element
	            ret = node.next.data;
	            // disconnecting node.next from the list
	            node.next = null; 
        }
        length--;
        return ret;
    }
```
## Doubly-Linked Lists
- Add an extra pointer in the `Node` structure to the previous `Node`.

### Reversal in Constant Time

#### Method
Swap the the next and previous pointers of each node in the list, then swap the head and tail pointers.

#### Code
```java
public void reverse() {  
	// Start from the head of the list.
    Node current = head;
    
    // While the list is not at the end
    while (current != null) {  
        // Swap the pointers of the node.  
        Node temp = current.prev;  
        current.prev = current.next;  
        current.next = temp;  
        current = current.prev;  
    }  
  
    // Swap the head and tail.  
    Node temp = head;
    head = tail;
    tail = temp;
}
```

### Removing from Tail

```java
public T removeRight() {  
    if (isEmpty()) throw new NoSuchElementException("List is empty.");  
    // Store the old tail
    Node oldTail = tail; 
    // Make the tail point to the previous node of the oldTail 
    tail = oldTail.prev;  
    
    // If the tail is an element, make it's next element null.
    if (tail != null) {  
        tail.next = null;  
	// Else the list is now empty so make head null.
    } else {  
        head = null;  
    }  
    
    size--;  
    return oldTail.item;  
}
```
## Utils
### Find middle elements
- Run two cursors through the list. One is 2x ahead of the first. When the second cursor hits the end, the first one is in the middle.
#### Code
```java
public T getMiddle() {  
    if (isEmpty()) throw new NoSuchElementException("List is empty.");  
  
    // Two cursors: One will be 2x ahead of the other.  
    // When the second cursor hits the end of the list, the
    // first will be in the middle.    
    Node cursor = head;  
    Node next = head;  
  
    while (next.next != null) {  
        cursor = cursor.next;  
        if (next.next.next != null) {  
            next = next.next.next;  
        } else {  
            break;  
        }  
    }  
    return cursor.item;  
}
```