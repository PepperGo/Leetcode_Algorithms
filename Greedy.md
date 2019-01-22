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

#### <T> T[] toArray(T[] a)
[java.util Interface List\<E\>](https://docs.oracle.com/javase/8/docs/api/java/util/List.html#toArray-T:A-)   
   
[How to convert List<Integer> to int[] in Java?](https://stackoverflow.com/questions/960431/how-to-convert-listinteger-to-int-in-java)     
   
[Converting 'ArrayList<String> to 'String[]' in Java](https://stackoverflow.com/questions/4042434/converting-arrayliststring-to-string-in-java)    


### 253. Meeting Rooms II
#### java.util Class PriorityQueue<E>
offer(), add()   
peek(), poll()   
   
   
   
### 714. Best Time to Buy and Sell Stock with Transaction Fee
#### [Most consistent ways of dealing with the series of stock problems](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-transaction-fee/discuss/108870/Most-consistent-ways-of-dealing-with-the-series-of-stock-problems)   

### 767. Reorganize String
#### Traverse through a HashSet in Java
[Traverse through a HashSet in Java](https://www.geeksforgeeks.org/traverse-through-a-hashset-in-java/)   

```
1. Using an Iterator 
HashSet<String> h = new HashSet<String>();
// Iterating over hash set items 
Iterator<String> i = h.iterator(); 
while (i.hasNext()) 
  System.out.println(i.next()); 
   
2. Using for-each loop
for (String i : h)  
  System.out.println(i); 
  
3. Using forEach() method
h.forEach(i -> System.out.println(i));

```      


#### Traverse through a HashMap in Java
[Traverse through a HashMap in Java](https://www.geeksforgeeks.org/traverse-through-a-hashmap-in-java/)   
```   
1. Using an Iterator

HashMap<String, Integer> hm = new HashMap<String, Integer>(); 
Iterator hmIterator = hm.entrySet().iterator();   
while (hmIterator.hasNext()) { 
   Map.Entry mapElement = (Map.Entry)hmIterator.next(); 
   int marks = ((int)mapElement.getValue() + 10); 
   System.out.println(mapElement.getKey() + " : " + marks); 
} 

2. Using for-each loop
HashMap<String, Integer> hm = new HashMap<String, Integer>(); 
// Using for-each loop 
for (Map.Entry mapElement : hm.entrySet()) { 
   String key = (String)mapElement.getKey(); 
   int value = ((int)mapElement.getValue() + 10); 
   System.out.println(key + " : " + value); 
} 

3. Using forEach() method
hm.forEach((k, v) -> System.out.println(k + " : " + (v + 10)));
```     





