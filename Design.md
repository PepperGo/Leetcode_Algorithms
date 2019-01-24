## Design

### 146. LRU Cache
#### Why Double Linked List instead of LinkedList?
```  
In order to remove the node, you have to let the next pointer of its previous node point to its next node, but in single linked list, you can not easily get the reference(O(n)) to its previous node when you only have the reference to itself. 
Thus double-linked list solves this problem.
```

