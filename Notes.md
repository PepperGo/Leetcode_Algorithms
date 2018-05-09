### 830. Positions of Large Groups
#### 1. List<List<Integer>> result = new ArrayList<ArrayList<Integer>>();  
The correct way is: List<List<Integer>> list = new ArrayList<List<Integer>>()  
**Reason**:   
Generic type is List<Integer> and we are trying to pass object of subtype i.e. ArrayList<Integer>, so it will not work.
Some useful link:   
[Why can't I initialise List<List<Integer>> as List<List<Integer>> list = new ArrayList<ArrayList<Integer>>();?](https://www.quora.com/Why-cant-I-initialise-List-List-Integer-as-List-List-Integer-list-new-ArrayList-ArrayList-Integer)  
[Is List<Dog> a subclass of List<Animal>? Why are Java generics not implicitly polymorphic?](https://stackoverflow.com/questions/2745265/is-listdog-a-subclass-of-listanimal-why-are-java-generics-not-implicitly-po)  
[Why List<List<Integer>> list = new ArrayList<ArrayList<Integer>>() is wrong?](https://stackoverflow.com/questions/29266304/why-listlistinteger-list-new-arraylistarraylistinteger-is-wrong)  

#### 2. Java: String.length  
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

Some useful link:  
[Difference between size and length methods?](https://stackoverflow.com/questions/20192843/difference-between-size-and-length-methods)

