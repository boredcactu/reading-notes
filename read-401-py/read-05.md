# Classes and Objects

# Linked Lists
  Linked lists are linear data structures that hold data in individual objects called nodes. These nodes hold both the data and a reference to the next node in the list.

#### Linked types:

  * Singly : Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

  * Doubly : Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

  * `Node` : is the individual items/links that live in a linked list. Each node contains the data for each link.

  * `Singly` : refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the `Next` node in a linked list.

  * `Doubly` : refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the `Next` and `Previous` node.

  * `Next` : This property contains the reference to the next node.

  * `Head` : This property contains the reference to the first node in a linked list.

  * `Current - The Current`:S
  reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

  >The `Next` property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.

  >The best way to approach a traversal is through the use of a `while()` loop. This allows us to continually check that the Next node in the list is not null.

## SUMMARY

  - A linked list is made up of a series of nodes, which are the elements of the list.
  - The starting point of the list is a reference to the first node, which is referred to as the head. 
  - The end of the list isnâ€™t a node, but rather a node that points to null, or an empty value.
  - A single node is also pretty simple. It has just two parts: data, or the information that the node contains, and a reference to the next node.


  Use WHY, WHAT, HOW structure

  now i know that sounds like a lot of work to do, so why linked lists ? 
  * Linked lists are often used because of their efficient insertion and deletion. They can be used to implement stacks, queues, and other abstract data types.

  * Linked lists offer some important advantages over other linear data structures. Unlike arrays, they are a dynamic data structure, resizable at run-time. Also, the insertion and deletion operations are efficient and easily implemented.


  These are nodes each node points the node next to it and the last node points to null indecating the end of a linked list 

  >When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.

### how `linked list` it look like in code ? 

  The first thing that you need to do is to create a class for the nodes

  ``` 
   class Node:
      def __init__(self, data):
        self.item = data
        self.ref = None

  ```

  >The objects of this class will be the actual nodes that we will insert in our linked list. We know that a node for a single linked list contains the item and the reference to the next node. Therefore, our node class will contain two member variables item and ref. The value of the item will be set by the value passed through the constructor, while the reference will be initially set to null.

  Next, we need to create a class for the Linked List. This class will contain the methods to insert, remove, traverse and sort the list

  ``` 
   class LinkedList:
      def __init__(self):
          self.start_node = None
  ```
  >Initially, the class will only contain one member start_node that will point to the starting or first node of the list. The value of start_node will be set to null using the constructor since the linked list will be empty at the time of creation. 


  The Python code for the traverse function is as follows. Add the function below to the LinkedList class that we created in the last section.

  ```
   def traverse_list(self):
      if self.start_node is None:
          print("List has no element")
          return
      else:
          n = self.start_node
          while n is not None:
              print(n.item , " ")
              n = n.ref
  ``` 
  >If the linked list is empty, that means there is no item to iterate. In such cases, the traverse_list() function simply prints the statement that the list has no item.


  The simplest way to insert an item in a single linked list is to add an item at the start of the list.

  ``` 
    def insert_at_start(self, data):
          new_node = Node(data)
          new_node.ref = self.start_node
          self.start_node= new_node
  ```

Done
---
 
[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)