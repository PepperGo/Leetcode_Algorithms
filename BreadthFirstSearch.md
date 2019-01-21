## Breadth First Search

### 127. Word Ladder
#### BFS && DFS
BFS - Use Queue
DFS - Stack, Recursive   

[Breadth First Search or BFS for a Graph](https://www.geeksforgeeks.org/breadth-first-search-or-bfs-for-a-graph/)   

[Breadth First Search Algorithm Tutorial with Java](https://tutorialedge.net/artificial-intelligence/breadth-first-search-java/)    

#### java concurrentmodificationexception
[java.util Class ConcurrentModificationException](https://docs.oracle.com/javase/7/docs/api/java/util/ConcurrentModificationException.html)   

[Stack Overflow](https://stackoverflow.com/questions/49971932/java-util-concurrentmodificationexception-thrown-when-adding-to-list/49971962)   

#### List to Set
[Easiest way to convert a List to a Set in Java](https://stackoverflow.com/questions/1429860/easiest-way-to-convert-a-list-to-a-set-in-java)    

#### Set to List
[Convert Set to List without creating new List](https://stackoverflow.com/questions/8892360/convert-set-to-list-without-creating-new-list)    



### 210. Course Schedule II
#### Topological sort
Using DFS

Topological-Sort (G)
1   make an empty list L
2   call DFS with the modification:
       when v is finished, add it as the head of list L
3   return L

