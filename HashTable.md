## HashTable

### 36. Valid Sudoku
#### [java.util Class HashSet\<E\>](https://docs.oracle.com/javase/7/docs/api/java/util/HashSet.html)  
##### boolean add(E e)
```
public boolean add(E e)
Adds the specified element to this set if it is not already present. 
More formally, adds the specified element e to this set if this set contains no element e2 such that (e==null ? e2==null : e.equals(e2)). 
If this set already contains the element, the call leaves the set unchanged and returns false.
```

### 349. Intersection of Two Arrays
#### List\<Integer\> to int[]
[How to convert List<Integer> to int[] in Java?](https://stackoverflow.com/questions/960431/how-to-convert-listinteger-to-int-in-java)   

No
  
#### List\<String\> to String[]
[Converting 'ArrayList<String> to 'String[]' in Java](https://stackoverflow.com/questions/4042434/converting-arrayliststring-to-string-in-java)   
 
 String[] array = list.toArray(new String[list.size()]);


### 204. Count Primes
#### [Sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes)   


### 535. Encode and Decode TinyURL
#### [HashCode and hashCode()]
[Equals() and hashCode() methods in Java](https://www.geeksforgeeks.org/equals-hashcode-methods-java/)    

[Why do I need to override the equals and hashCode methods in Java?](https://stackoverflow.com/questions/2265503/why-do-i-need-to-override-the-equals-and-hashcode-methods-in-java)  

#### Random Number
[How to generate random integers within a specific range in Java?](https://stackoverflow.com/questions/363681/how-to-generate-random-integers-within-a-specific-range-in-java)    

[Getting random numbers in Java](https://stackoverflow.com/questions/5887709/getting-random-numbers-in-java)    


### 957. Prison Cells After N Days
#### Array Equals, Copy
[java.util Class Arrays](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html) 
```
Arrays.copyOfRange(T[] original, int from, int to)
Arrays.copyOf(T[] original, int newLength)

Arrays.equals(Object[] a, Object[] a2)

```  



#### Array Clone
clone(): Methods inherited from class java.lang.Object


### 353. Design Snake Game
#### HashSet<int[]> !!!! Wrong!
[HashSet usage with int arrays](https://stackoverflow.com/questions/28344312/hashset-usage-with-int-arrays)   

That's because HashSet uses .equals() to see if a new object is duplicated (and .hashCode() to determine the "bucket").

When you work with arrays, please be aware that new int[]{1,2,3} is NOT "equal to" new int[]{1,2,3}.

The proper way to "deep compare" arrays is via Arrays.equals(a, b) method


#### Override hashCode()
[Why to Override equals(Object) and hashCode() method ?](https://www.geeksforgeeks.org/override-equalsobject-hashcode-method/)   
You must override hashCode() in every class that overrides equals(). 

 
