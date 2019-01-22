## Greedy

### 406. Queue Reconstruction by Height
#### Override compare method
[Java - How to Use Comparator?](https://www.tutorialspoint.com/java/java_using_comparator.htm)   

```
int compare(Object obj1, Object obj2)
obj1 and obj2 are the objects to be compared. 
This method returns zero if the objects are equal. 
It returns a positive value if obj1 is greater than obj2.
Otherwise, a negative value if obj1 is smaller than obj2.
```  

[Interface Comparator\<T\>](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html#compare-T-T-)   

[Comparator Interface in Java with Examples](https://www.geeksforgeeks.org/comparator-interface-java/)   

```
To compare two elements, it asks “Which is greater?” 
Compare method returns -1, 0 or 1 to say if it is less than, equal, or greater to the other. 
It uses this result to then determine if they should be swapped for its sort.
```   


[What determines ascending or descending order in Comparator / Comparable collection class?](https://stackoverflow.com/questions/26107921/what-determines-ascending-or-descending-order-in-comparator-comparable-collect)   
```
if( data[i].compareTo(data[j]) > 0 ){
   // swap data[i] and  data[j]
}

```  




