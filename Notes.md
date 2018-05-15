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


