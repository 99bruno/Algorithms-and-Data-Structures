# Linked List

**A linked list** is a linear data structure that consists of a series of nodes connected by pointers (in C or C++) or 
references (in Java, Python and JavaScript). 
Each node contains data and a pointer/reference to the next node in the list.
Unlike arrays, linked lists allow for efficient insertion or removal of elements from any position in the list, 
as the nodes are not stored contiguously in memory.

## How it works:

A linked list is a dynamic data structure where each element (node) contains a reference (or pointer) to the next element in the sequence. This allows for efficient insertion and deletion of elements.

### Key Points:
- **Node Structure**: Each node contains data and a reference to the next node.
- **Head**: The first node in the list.
- **Tail**: The last node in the list, which points to `None`.
- **Traversal**: To access elements, you start from the head and follow the references to the next nodes.
- **Insertion/Deletion**: Can be done efficiently at any position by updating the references.

## Complexity

The time complexity for the linked list operations is:

- **Access**: O(n)
- **Search**: O(n)
- **Insertion**: O(1)
- **Deletion**: O(1)
- **Append**: O(1)
- **Prepend**: O(1)
- **Length**: O(n)
- **Traversal**: O(n)
- **Space Complexity**: O(n)

## Implementation

- [LinkedList.ipynb](LinkedList.ipynb) - The main implementation of a linked list in Python.
- [LinkedListBankSystem.ipynb](LinkedListBankSystem.ipynb) - A simple bank system implemented using a linked list.

