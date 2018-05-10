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

##### (2) Operations

##### (3) Traversal


#### 4. 
