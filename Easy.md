### 830. Positions of Large Groups
#### 1. List<List<Integer>> result = new ArrayList<ArrayList<Integer>>();   X
The correct way is: List<List<Integer>> list = new ArrayList<List<Integer>>()  
**Reason**:   
Generic type is List<Integer> and we are trying to pass object of subtype i.e. ArrayList<Integer>, so it will not work.
Some useful links:   
[Why can't I initialise List<List<Integer>> as List<List<Integer>> list = new ArrayList<ArrayList<Integer>>();?](https://www.quora.com/Why-cant-I-initialise-List-List-Integer-as-List-List-Integer-list-new-ArrayList-ArrayList-Integer)  
[Is List<Dog> a subclass of List<Animal>? Why are Java generics not implicitly polymorphic?](https://stackoverflow.com/questions/2745265/is-listdog-a-subclass-of-listanimal-why-are-java-generics-not-implicitly-po)  
[Why List<List<Integer>> list = new ArrayList<ArrayList<Integer>>() is wrong?](https://stackoverflow.com/questions/29266304/why-listlistinteger-list-new-arraylistarraylistinteger-is-wrong)  

#### 2. Java: String.length  X
**Reason**:   
For Java, Here is the syntax of this method −
```
public int length()
```
For JavaScript, 
```
str.length
```  

size() is a method specified in java.util.Collection, which is then inherited by every data structure in the standard library.  length is a field on any array (arrays are objects, you just don't see the class normally), and length() is a method on java.lang.String, which is just a thin wrapper on a char[] anyway.

Some useful links:  
[Difference between size and length methods?](https://stackoverflow.com/questions/20192843/difference-between-size-and-length-methods)

#### 3. Arrays.asList(i, j - 1) V
Link: [Arrays (Java Platform SE 7 )](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html#asList(T...))



### 824. Goat Latin
#### 1. String Methods
```
String concat(String str), 	boolean	contains(CharSequence s),  static String copyValueOf(char[] data), boolean	endsWith(String suffix), boolean	equals(Object anObject), int	indexOf(int ch), int	indexOf(int ch, int fromIndex), int indexOf(String str), int lastIndexOf(String str), int	length(), String	replaceAll(String regex, String replacement), String[] split(String regex), 

String	substring(int beginIndex), String	substring(int beginIndex, int endIndex)
char[]	toCharArray(), 

```
#### 2. String array to array
```
If you just want a "debug-style" dump of an array:

String str = Arrays.toString(arr);
or, for more control (before Java 8):

StringBuilder builder = new StringBuilder();
for(String s : arr) {
    builder.append(s);
}
String str = builder.toString();
(Java 8 and above):

String str = String.join(",", arr);
```
#### 3. if-condition to for-loop

```
 if(ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' || ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U')
            return true;
        else 
            return false;
```

```
for (char c : "aeiouAEIOU".toCharArray()) 
    vowel.add(c);

```
Some links:   
[String (Java Platform SE 7 )](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html)  
[Java String Array to String](https://www.journaldev.com/773/java-string-array-to-string)  
[Convert array of strings into a string in Java](https://stackoverflow.com/questions/5283444/convert-array-of-strings-into-a-string-in-java)  


### 819. Most Common Word
#### 1. "\\s" or "\\s+" is better than " "

#### 2. Remove punctuation
```
String[] words = instring.replaceAll("[^a-zA-Z ]", "").toLowerCase().split("\\s+");
```
For this question,
```
String[] words = paragraph.replaceAll("[!?',;.]","").toLowerCase().split("\\s+");
```
Link:
1. [How can I remove punctuation from input text in Java?](https://stackoverflow.com/questions/18830813/how-can-i-remove-punctuation-from-input-text-in-java)

#### 3. Hashtable, HashSet, HashMap

##### (1) Comparsion
[What is the difference between HashSet, HashMap and hash table?](https://www.quora.com/What-is-the-difference-between-HashSet-HashMap-and-hash-table-How-do-they-behave-in-a-multi-threaded-environment)   
[Hashtable, HashMap, HashSet , hash table concept in Java collection framework](https://stackoverflow.com/questions/47838841/hashtable-hashmap-hashset-hash-table-concept-in-java-collection-framework)   
##### (2) Operations

##### (3) Traversal
- HashSet  
```
(1)
     Iterator<String> it = hset.iterator();
     while(it.hasNext()){
        System.out.println(it.next());
     }
     
(2)   Set<String> set = new HashSet<String>();

    for (String s : set) {
        System.out.println(s);
    }
    
(3) set.forEach(System.out::println);


```  

- HashMap

If you're only interested in the keys, you can iterate through the keySet() of the map:  
```
Map<String, Object> map = ...;

for (String key : map.keySet()) {
    // ...
}
```
If you only need the values, use values():
```
for (Object value : map.values()) {
    // ...
}
```  
Finally, if you want both the key and value, use entrySet():

```
for (Map.Entry<String, Object> entry : map.entrySet()) {
    String key = entry.getKey();
    Object value = entry.getValue();
    // ...
}

```  


[How to Iterate over a Set/HashSet](https://beginnersbook.com/2014/08/how-to-iterate-over-a-sethashset/)    
[Iterate through a HashMap](https://stackoverflow.com/questions/1066589/iterate-through-a-hashmap)   



- Hash
```
        Set<String> keys = hm.keySet();
        for(String key: keys){
            System.out.println("Value of "+key+" is: "+hm.get(key));
        }
```

[Program: How to iterate through Hashtable?](http://www.java2novice.com/java-collections-and-util/hashtable/iterate/)    


### 812. Largest Triangle Area

#### 1. Two dimensional array

##### (1) Basic
```
int[][] multi = new int[5][10];
```
which is a short hand for something like this:
```
int[][] multi = new int[5][];
multi[0] = new int[10];
multi[1] = new int[10];
multi[2] = new int[10];
multi[3] = new int[10];
multi[4] = new int[10];
```
Note that every element will be initialized to the default value for int, 0, so the above are also equivalent to:
```
int[][] multi = new int[][]{
  { 0, 0, 0, 0, 0, 0, 0, 0, 0, 0 },
  { 0, 0, 0, 0, 0, 0, 0, 0, 0, 0 },
  { 0, 0, 0, 0, 0, 0, 0, 0, 0, 0 },
  { 0, 0, 0, 0, 0, 0, 0, 0, 0, 0 },
  { 0, 0, 0, 0, 0, 0, 0, 0, 0, 0 }
};
```
[Syntax for creating a two-dimensional array](https://stackoverflow.com/questions/12231453/syntax-for-creating-a-two-dimensional-array)  

[Two-Dimensional Arrays](https://www.cs.cmu.edu/~mrmiller/15-110/Handouts/arrays2D.pdf)    

##### (2) Size
int[][] rating = new int[3][4];

What is the value of rating.length?  Answer: 3, the number of rows (first dimension)   

What is the value of rating[0].length? Answer: 4, the number of columns (second dimension)   


### 811. Subdomain Visit Count
#### 1. Type conversion in Java
String to int:   
```
(1)
String number = "10";
int result = Integer.parseInt(number);			
(2)
String number = "10";
Integer result = Integer.valueOf(number);
```   
int to String:
```
(1)
Integer.toString(int)
(2)
String.valueOf(int)
```
[Type conversion in Java with Examples](https://www.geeksforgeeks.org/type-conversion-java-examples/)   

#### 2. hashMap.containsKey(Key key)

#### 3. boolean	contains(CharSequence s)
Returns true if and only if this string contains the specified sequence of char values.

#### 4. int	indexOf(int ch), int indexOf(String str), int indexOf(int ch, int fromIndex), int indexOf(String str, int fromIndex)



### 804. Unique Morse Code Words
#### 1. HashSet Operationbs
```
boolean	add(E e)  
void	clear()  
Object	clone()  
boolean	contains(Object o)  
boolean	isEmpty()  
Iterator<E>	iterator()     
boolean	remove(Object o)     
int	size()
```

#### Adding a duplicate value to a HashSet/HashMap
In the case of HashMap, it replaces the old value with the new one.

In the case of HashSet, the item isn't inserted.

[Does adding a duplicate value to a HashSet/HashMap replace the previous value](https://stackoverflow.com/questions/12940663/does-adding-a-duplicate-value-to-a-hashset-hashmap-replace-the-previous-value)   


### 784. Letter Case Permutation
#### 1. valueOf()
static String	valueOf(boolean b)  
static String	valueOf(char c)  
static String	valueOf(char[] data)  
static String	valueOf(char[] data, int offset, int count)  
static String	valueOf(double d)  
static String	valueOf(float f)  
static String	valueOf(int i)  
static String	valueOf(long l)  
static String	valueOf(Object obj)  

#### 2. Character Class
static boolean	isDigit(char ch)    
static boolean	isAlphabetic(int codePoint)   
static boolean	isLowerCase(char ch)  
static boolean	isUpperCase(char ch)  



Links:   
[Class Character](https://docs.oracle.com/javase/7/docs/api/java/lang/Character.html)     


### 783. Minimum Distance Between BST Nodes
#### 1. Tree Traversals (Inorder, Preorder and Postorder)
```
 void printPostorder(Node node)
    {
        if (node == null)
            return;
 
        // first recur on left subtree
        printPostorder(node.left);
 
        // then recur on right subtree
        printPostorder(node.right);
 
        // now deal with the node
        System.out.print(node.key + " ");
    }
 
    /* Given a binary tree, print its nodes in inorder*/
    void printInorder(Node node)
    {
        if (node == null)
            return;
 
        /* first recur on left child */
        printInorder(node.left);
 
        /* then print the data of node */
        System.out.print(node.key + " ");
 
        /* now recur on right child */
        printInorder(node.right);
    }
 
    /* Given a binary tree, print its nodes in preorder*/
    void printPreorder(Node node)
    {
        if (node == null)
            return;
 
        /* first print data of node */
        System.out.print(node.key + " ");
 
        /* then recur on left sutree */
        printPreorder(node.left);
 
        /* now recur on right subtree */
        printPreorder(node.right);
    }

```  

Link:  
[Tree Traversals (Inorder, Preorder and Postorder)](https://www.geeksforgeeks.org/tree-traversals-inorder-preorder-and-postorder/)

#### 2. Recursive + public variable

### 771. Jewels and Stones

#### 1. Regex
S.replaceAll("[^" + J + "]", "").length();

### 747. Largest Number At Least Twice of Others
#### 1. Return the two largest values in an array of values
```
int largestA = Integer.MIN_VALUE, largestB = Integer.MIN_VALUE;

for(int value : values) {
    if(value > largestA) {
        largestB = largestA;
        largestA = value;
     } else if (value > largestB) {
            largestB = value;
     }
 }


```
[Return the two largest integers in an array of values](https://stackoverflow.com/questions/16384472/return-the-two-largest-integers-in-an-array-of-values)  

### 746. Min Cost Climbing Stairs

#### 1. DP & Recursive
[Solution](https://leetcode.com/problems/min-cost-climbing-stairs/discuss/110111/Easy-to-understand-C++-using-DP-with-detailed-explanation)  


### 744. Find Smallest Letter Greater Than Target
#### 1.   int mid = lo + (hi - lo) / 2; instead of   int mid = (start + end)/2;

#### 2. Binary Search(critical condition)
Take care: This is just solution to question, not binary search codes!
```
 while(start <= end){
            int mid = (start + end)/2;
            if(target < letters[mid])
                end = mid - 1; 
            else
                start = mid + 1;
        }
```   

```
 while(start < end){
            int mid = (start + end)/2;
            if(target < letters[mid])
                end = mid;
            else
                start = mid + 1;
        }

```

### 744. Find Smallest Letter Greater Than Target
#### 1. String.contains('a') X   => String.contains("a") V


#### 2. Char to Integer
```
char c='1';  
int a=Integer.parseInt(String.valueOf(c));  
```   
[Java Convert char to int](https://www.javatpoint.com/java-char-to-int)   


### 724. Find Pivot Index
#### 1. += and =+
a += b is short-hand for a = a + b (though note that the expression a will only be evaluated once.)   
a =+ b is a = (+b), i.e. assigning the unary + of b to a.   

[The difference between += and =+](https://stackoverflow.com/questions/6958401/the-difference-between-and)     

#### 2. Solution!


### 720. Longest Word in Dictionary
#### 1. Arrays Class
(1) copyof
java.util.Arrays.copyof() method is in java.util.Arrays class. It copies the specified array, truncating or padding with false (if necessary) so the copy has the specified length.

Syntax:

 copyOf(int[] original, int newLength) 
original – original array
newLength – copy of original array   

int[] copy = Arrays.copyOf(org, 5);

(2) copyOfRange
This method creates a copy of elements, within a specified range of the original array.

Syntax :

public static int[] copyOfRange(int[] original_array, int from_index, int to_index)
original_array : Array to be copied from
from_index : Starting index of range to be copied
to_end : Ending index of range to be copied

 int[] copy1 = Arrays.copyOfRange(arr, 4, arr.length + 3);

(3)	sort


(4) toString

The java.util.Arrays.toString(int[]) method returns a string representation of the contents of the specified int array. The string representation consists of a list of the array's elements, enclosed in square brackets ("[]"). Adjacent elements are separated by the characters ", " (a comma followed by a space).

Declaration
Following is the declaration for java.util.Arrays.toString() method

public static String toString(int[] a)
Parameters
a − This is the array whose string representation to return.

Return Value
This method returns a string representation of a.

Example:
 int[] i1 = new int[] { 33, 12, 98 };  
 System.out.println(Arrays.toString(i1));    //[33, 12, 98]
 

[Class Arrays](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html)   

#### 2. String.substring()
public String substring(int startIndex): This method returns new String object containing the substring of the given string from specified startIndex (inclusive).
public String substring(int startIndex, int endIndex): This method returns new String object containing the substring of the given string from specified startIndex to endIndex.

startIndex: inclusive
endIndex: exclusive

String s="hello";  
System.out.println(s.substring(0,2));//he  


### 697. Degree of an Array
#### 1. HashMap
(1) a duplicate key is put into a HashMap   
Associates the specified value with the specified key in this map. If the map previously contained a mapping for the key, the old value is replaced.   

[What happens when a duplicate key is put into a HashMap?](https://stackoverflow.com/questions/1669885/what-happens-when-a-duplicate-key-is-put-into-a-hashmap)  

(2) Find max value in HashMap   
```
    Map.Entry<Integer, Integer> maxEntry = null;

    for (Map.Entry<Integer, Integer> entry : mapValues.entrySet()) {

        if (maxEntry == null
                || entry.getValue().compareTo(maxEntry.getValue()) > 0) {
            maxEntry = entry;
        }
    }
    assertEquals(new Integer(7), maxEntry.getValue());
```
[Find max value in HashMap](https://www.leveluplunch.com/java/examples/find-max-value-in-map/)   
[Finding Key associated with max Value in a Java Map](https://stackoverflow.com/questions/5911174/finding-key-associated-with-max-value-in-a-java-map)    

#### 2. Interface Comparable<T>
Compares this object with the specified object for order. Returns a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object.   
    

### 693. Binary Number with Alternating Bits
#### 1. Integer.toBinaryString
public static String toBinaryString(int i)

#### 2. public boolean matches(String regex)
Integer.toBinaryString(n).matches("(10)*1?");


### 690. Employee Importance
#### 1. HashMap
public V put(K key,V value), public V get(Object key), public boolean isEmpty(), public int size()  

[HashMap](https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html)   

#### 2. Stack
A more complete and consistent set of LIFO stack operations is provided by the Deque interface and its implementations, which should be used in preference to this class. For example:

   Deque<Integer> stack = new ArrayDeque<Integer>();   
 
 [Deque](https://docs.oracle.com/javase/7/docs/api/java/util/Deque.html)   
 
Stack:  
boolean	empty()
Tests if this stack is empty.
E	peek()
Looks at the object at the top of this stack without removing it from the stack.
E	pop()
Removes the object at the top of this stack and returns that object as the value of this function.
E	push(E item)
Pushes an item onto the top of this stack.
int	search(Object o)

### 657. Judge Route Circle
#### multiple if-else  ==> switch
```
  switch (ch) {
                case 'U' : v++; break;
                case 'D' : v--; break;
                case 'R' : h++; break;
                case 'L' : h--; break;
            }
```   

### 682. Baseball Game
#### 1. Deque
![](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/java-collection.jpg)     
Deque deque = new LinkedList<>();  
Deque<String> deque = new ArrayDeque<String>();

Methods of deque:     
add(element): Adds an element to the tail.  
addFirst(element): Adds an element to the head.   
addLast(element): Adds an element to the tail.   
offer(element): Adds an element to the tail and returns a boolean to explain if the insertion was successful.   
offerFirst(element): Adds an element to the head and returns a boolean to explain if the insertion was successful.   
offerLast(element): Adds an element to the tail and returns a boolean to explain if the insertion was successful.   
iterator(): Returna an iterator for this deque.   
descendingIterator(): Returns an iterator that has the reverse order for this deque.    
push(element): Adds an element to the head.    
pop(element): Removes an element from the head and returns it.   
removeFirst(): Removes the element at the head.   
removeLast(): Removes the element at the tail.

### 643. Maximum Average Subarray I
[Why is Double.MIN_VALUE in not negative](https://stackoverflow.com/questions/3884793/why-is-double-min-value-in-not-negative)  
### 637. Average of Levels in Binary Tree
#### 1. Queue is abstract; cannot be instantiated
Cannot instantiate Queue like: Queue<E> queue = new Queue<E>();

[Cannot instantiate the type Queue. Why is this?](https://stackoverflow.com/questions/28641605/cannot-instantiate-the-type-queue-why-is-this)  

[The Queue Interface](https://docs.oracle.com/javase/tutorial/collections/interfaces/queue.html)    

[The Deque Interface](https://docs.oracle.com/javase/tutorial/collections/interfaces/deque.html)  

[Lesson: Interfaces](https://docs.oracle.com/javase/tutorial/collections/interfaces/index.htmlLesson: Interfaces)  

![](https://docs.oracle.com/javase/tutorial/figures/collections/colls-coreInterfaces.gif)  

##### Deque:
- Insert
The **addfirst** and **offerFirst** methods insert elements **at the beginning of** the Deque instance. The methods **addLast** and **offerLast** insert elements **at the end** of the Deque instance. When the capacity of the Deque instance is restricted, the **preferred methods** are **offerFirst** and offerLast because **addFirst** might fail to throw an **exception** if it is full.

- Remove
The **removeFirst** and **pollFirst** methods remove elements from **the beginning of** the Deque instance. The **removeLast** and **pollLast** methods remove elements from **the end**. The methods **pollFirst** and **pollLast** return **null** if the Deque is empty whereas the methods **removeFirst** and **removeLast** throw an **exception** if the Deque instance is empty.

- Retrieve
The methods **getFirst** and **peekFirst** retrieve the **first element** of the Deque instance. These methods dont remove the value from the Deque instance. Similarly, the methods **getLast** and **peekLast** retrieve the last element. The methods **getFirst and getLast** throw an exception if the deque instance is empty whereas the methods **peekFirst** and **peekLast** return NULL.


#### 2. Use queue.isEmpty() instead of queue.size() == 0
    

### 633. Sum of Square Numbers
#### 1. double int compare
[Is it valid to compare a double with an int in java?](https://stackoverflow.com/questions/13297207/is-it-valid-to-compare-a-double-with-an-int-in-java)
Then performing operations (including comparisons) with two different numerical types, Java will perform an implicit widening conversion. This means that when you compare a double with an int, the int is converted to a double so that Java can then compare the values as two doubles.

#### 2. Primitive Data Types
[Primitive Data Types](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)   

### 605. Can Place Flowers
#### 1. The else parts are the same, we can refine it

#### 2. change flowerbed[i] = 1 to flowerbed[i++] = 1 to skip the neighbor;


### 599. Minimum Index Sum of Two Lists
#### 1. Use HashMap instead of HashTable in Leetcode
[Differences between HashMap and Hashtable?](https://stackoverflow.com/questions/40471/differences-between-hashmap-and-hashtable)  

HashMap(containsKey, put, get)

#### 2. ArrayList to Array
String [] countries = list.toArray(new String[list.size()]);

#### 3. ArrayList: clear() && removeAll()
[What is the difference between ArrayList.clear() and ArrayList.removeAll()?](https://stackoverflow.com/questions/7032070/what-is-the-difference-between-arraylist-clear-and-arraylist-removeall)  
The time complexity of ArrayList.clear() is O(n) and of removeAll is O(n^2).  


