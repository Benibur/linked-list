# Linked-lists

Two vanila js, heavy tested, libraries to manage :
* (doubly) linked lists
* circular linked-lists (head is linked to the tail and vice-versa)


## Usage :

* add one of the following files to your code (no dependencies) :
  * `./lib/linked-list.js`
  * `./lib/linked-circurlar-list.js`

* Exemple :
``` javascript
const LinkedList = require('../src/linked-list')
const list = new LinkedList()
list.append('c')
list.prepend('a')
list.insert(1,'b')
console.log( list.printDataChain() )
// a-b-c
```

See in ./test/ for more exemples

## API :

* `DoublyLinkedList.append(data)`
  * Appends a node to the end of the list, after its tail.
  * `data` can be a pointer to anything (object, string, integer...)
  * returns the created node

* `DoublyLinkedList.prepend(data)`
  * Prepends a node to the start of the list, before its head.
  * returns the created node

* `DoublyLinkedList.insert(rank, data)`
  * Inserts one node at rank.
  * Returns the created node, undefined if rank out of range.

* `DoublyLinkedList.insertAfterNode(nextNode, data)`
  * Inserts a new node after one
  * Returns the new node

* `DoublyLinkedList.at(index)`
  * Returns the node at the specified index. The index starts at 0.
  * Undefined if index out of range.
  * a node is an object like : { data, next, prev, id }

* `DoublyLinkedList.id(id)`
  * Returns the node with the specified id, undefined if wrong id.

* `DoublyLinkedList.rank(node)`
  * Returns the rank of a node, undefined if node not found

* `DoublyLinkedList.head()`
  * Returns the node at the head of the list.

* `DoublyLinkedList.tail()`
  * Returns the node at the tail of the list.

* `DoublyLinkedList.size()`
  * Returns the size of the list.

* `DoublyLinkedList.remove(index)`
  * Removes the item at the index.
  * returns undefined if index out of range

* `DoublyLinkedList.removeID(id)`
  * Removes the item with this id
  * Returns undefined if id not in the chain

* `DoublyLinkedList.removeNode(node)`
  * Removes the given node
  * Returns undefined if the node is not in the chain

* `DoublyLinkedList.printIdChain()`
  * return a string representing the list of ordered ids in the chain

* `DoublyLinkedList.printAllChain()`
  * return a string representing the list of ordered nodes (rank, id, data) in the chain

* `DoublyLinkedList.printDataChain()`
  * return a string representing the list of ordered nodes (rank, id, data) in the chain

* `DoublyLinkedList.(data)`
  * return a string representing the list of ordered data in the chain


## Tests :
Run tests :
```
npm install
npm run test
```

## Build :

Push source files in ./lib

```
npm run build
````
