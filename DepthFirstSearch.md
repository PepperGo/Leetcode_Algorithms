## Depth First Search
[DirectedEdge.java](https://algs4.cs.princeton.edu/44sp/DirectedEdge.java.html)    

[EdgeWeightedDigraph.java](https://algs4.cs.princeton.edu/44sp/EdgeWeightedDigraph.java.html)    

[EdgeWeightedDirectedCycle.java](https://algs4.cs.princeton.edu/44sp/EdgeWeightedDirectedCycle.java.html)   


### 394. Decode String
#### Convert String to int
[Java – Convert String to int](https://www.mkyong.com/java/java-convert-string-to-int/)  
```
	String number = "10";
	int result = Integer.parseInt(number);	
```  

```
  String number = "10";
	Integer result = Integer.valueOf(number);	
```  

```
  If the string does not contain a parsable integer, a NumberFormatException will be thrown.

	String number = "10A";
	int result = Integer.parseInt(number);
	
  Exception in thread "main" java.lang.NumberFormatException: For input string: "10A"
```    

#### character is a letter or number
[What is the best way to tell if a character is a letter or number in Java without using regexes?](https://stackoverflow.com/questions/4047808/what-is-the-best-way-to-tell-if-a-character-is-a-letter-or-number-in-java-withou)   

### 109. Convert Sorted List to Binary Search Tree
#### Setting LinkedList nodes to null
[Setting LinkedList nodes to null](https://stackoverflow.com/questions/33878718/setting-linkedlist-nodes-to-null)   

```
               n
               |
               v
A -> B -> C -> D 

If you set n to null, the end result is this:

               n---> null


A -> B -> C -> D
```    


### 207. Course Schedule
#### Topological sort
[Topological Sorting](https://www.geeksforgeeks.org/topological-sorting/)  

[Topological sorting From Wikipedia](https://en.wikipedia.org/wiki/Topological_sorting)  

#### Topological sort DFS
[Topological Sorting](https://en.wikipedia.org/wiki/Topological_sorting#Algorithms)   


#### Topological sort  BFS
[Kahn's algorithm](https://en.wikipedia.org/wiki/Topological_sorting#Algorithms)   

[Topo-Sort](https://courses.cs.washington.edu/courses/cse326/03wi/lectures/RaoLect20.pdf)

#### Array of ArrayList in Java
[Array of ArrayList in Java](https://www.geeksforgeeks.org/array-of-arraylist-in-java/)     

[Create an Array of Arraylists](https://stackoverflow.com/questions/8559092/create-an-array-of-arraylists)    


### 743. Network Delay Time 
#### Shortest Paths(from textbook)
##### Bellman-Ford algorithm
```
   Bellman-Ford (G, w, s)
1   Initialization (G, s) 
2   for i = 1 to n - 1
3     for each edge (u, v) belongs to E 
4       Relax (u, v)
5   for every edge (u, v)
6     if v.dist > u.dist + w(u, v)
7       return false 
8   return true
```   
[4.4 Shortest Paths - codes](https://algs4.cs.princeton.edu/44sp/BellmanFordSP.java.html)

##### Dijkstra algorithm
```
Dijkstra (G, w, s)
1   Initialization (G, s) 
2   S= {};
3   for i = 1 to n
4      find v {- V - S with minimum v.dist
5      S = S U {v}
6      for each vertex u {- v.Adj // u is a neighbor of v
7          Relax (v, u)
```  


##### Floyd-Warshall algorithm(All-Pairs Shortest Paths)
```
Floyd-Warshall (W, n)
// Input: n ⇥ n matrix W
// Output: matrix D of shortest-path weights
1  D=W
2  for k = 1 to n
3    for i = 1 to n 
4      for j = 1 to n
5         if D[i][j] > D[i][k] + D[k][j] 
6            D[i][j] = D[i][k] + D[k][j]
7  return D

```

### 332. Reconstruct Itinerary
#### PriorityQueue in Java
[PriorityQueue in Java](https://www.geeksforgeeks.org/priority-queue-class-in-java-2/)   
[Class PriorityQueue\<E\>](https://docs.oracle.com/javase/7/docs/api/java/util/PriorityQueue.html)  
[Priority queue ordering of elements](https://stackoverflow.com/questions/30072077/priority-queue-ordering-of-elements)   
```
Actually internal data structure of PriorityQueue is not ordered, it is a heap.  

An unbounded priority queue based on a priority heap. The elements of the priority queue are ordered according to their natural ordering, or by a Comparator provided at queue construction time, depending on which constructor is used. A priority queue does not permit null elements.  

A priority queue relying on natural ordering also does not permit insertion of non-comparable objects (doing so may result in ClassCastException).
```  
#### putIfAbsent
public V putIfAbsent(K key, V value)   
Description copied from interface: Map  

If the specified key is not already associated with a value (or is mapped to null) associates it with the given value and returns null, else returns the current value.

Specified by:
putIfAbsent in interface Map<K,V>

#### PriorityQueue offer(), add()
[What is the difference between the add and offer methods in a Queue in Java?](https://stackoverflow.com/questions/2703984/what-is-the-difference-between-the-add-and-offer-methods-in-a-queue-in-java)  









