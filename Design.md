## Design

### 146. LRU Cache
#### Why Double Linked List instead of LinkedList?
```  
In order to remove the node, you have to let the next pointer of its previous node point to its next node, but in single linked list, you can not easily get the reference(O(n)) to its previous node when you only have the reference to itself. 
Thus double-linked list solves this problem.
```

#### HashMap detele element
```
Hash_Map.remove(Object key)
```  

### 642. Design Search Autocomplete System
#### String compare
[Comparing two string and sorting them in alphabetical order](https://stackoverflow.com/questions/20445900/comparing-two-string-and-sorting-them-in-alphabetical-order)    

```
String a="LetterA";
String b="ALetterB";
int compare = a.compareTo(b);
if (compare < 0){
    System.out.println(a+" is before "+b);
}
else if (compare > 0) {
    System.out.println(b+" is before "+a);
}
else {
    System.out.println(b+" is same as "+a);
}
```   

