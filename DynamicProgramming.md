## Dynamic Programming

### 5. Longest Palindromic Substring  
#### String.substring()  
```
public String substring(int startIndex)  
and  
public String substring(int startIndex, int endIndex)  

startIndex : starting index is inclusive
endIndex : ending index is exclusive

```   

### 139. Word Break  
#### ArrayList -> HashSet
Contains for a HashSet is O(1) compared to O(n) for a list, therefore you should never use a list if you often need to run contains . 
The ArrayList uses an array for storing the data. The ArrayList.contains will be of O(n) complexity.  


Collection object has a constructor that accept a Collection object to initial the value.  
Since both Set and List are extend the Collection, the conversion is quite straightforward. It’s just pass a List into Set constructor or vice verse.
```
Convert List to Set
Set set = new HashSet(list);

Convert Set to List
List list = new ArrayList(set);
```  

#### [Interface Queue](https://docs.oracle.com/javase/7/docs/api/java/util/Queue.html)
Throws exception, Returns special value
add(e), offer(e)
remove(), poll()


#### Boolean, boolean
[Boolean vs boolean in Java](https://stackoverflow.com/questions/3728616/boolean-vs-boolean-in-java)  

The default value for the elements in a boolean[] is false. You don't need to do anything.
The reason it's necessary for Boolean[] is because the default value is null.


### 140. Word Break II  
#### Array
```
ArrayList<String>[] dp = new ArrayList[n];
LinkedList<String>[] dp = new LinkedList[n];

ArrayList<String>[] dp = new ArrayList<String>[n] (X, wrong)
```  


#### ArrayList with values
[How to declare ArrayList with values in Java?](http://www.java67.com/2015/10/how-to-declare-arraylist-with-values-in-java.html)  

