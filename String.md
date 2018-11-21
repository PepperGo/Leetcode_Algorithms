## String

### 12. Integer to Roman
#### [How to initialize an array in Java?](https://stackoverflow.com/questions/1938101/how-to-initialize-an-array-in-java)   
```
int[] data = {10,20,30,40,50,60,71,80,90,91};

// or

int[] data;
data = new int[] {10,20,30,40,50,60,71,80,90,91};

Datatype[] variable = new Datatype[] { value1,value2.... }

Datatype variable[]  = new Datatype[] { value1,value2.... }
 
```   

### 3. Longest Substring Without Repeating Characters
#### [How to check StringBuilder charcters to see if it contains same characters as new string request from array?](https://stackoverflow.com/questions/3202861/java-how-to-check-stringbuilder-charcters-to-see-if-it-contains-same-characters) 
```
public int indexOf(String str)
Returns the index within this string of the first occurrence of the specified substring. The integer returned is the smallest value k such that: this.toString().startsWith(str, k) is true.
Parameters:
str - any string.
Returns:
if the string argument occurs as a substring within this object, then the index of the first character of the first such substring is returned; if it does not occur as a substring, -1 is returned.
```   
#### length()
```
public int length()
Returns the length (character count).
Specified by:
length in interface CharSequence
Returns:
the length of the sequence of characters currently represented by this object
```   

### 17. Letter Combinations of a Phone Number
#### Java Convert char to int
```
Character.getNumericValue()

Get ASCII value

Integer.parseInt(String.valueOf(c)); 

```   

### 151. Reverse Words in a String
#### StringBuilder vs String
[StringBuilder vs String concatenation in toString() in Java](https://stackoverflow.com/questions/1532461/stringbuilder-vs-string-concatenation-in-tostring-in-java)    

#### String.split()
contain leading or trailing spaces, each word with more than one space
```
 String[] words = s.trim().split("\\s+");
```  


### 49. Group Anagrams
#### Iterate through a HashMap
[Iterate through a HashMap](https://stackoverflow.com/questions/1066589/iterate-through-a-hashmap)   
```
Map<String, String> map = ...
for (Map.Entry<String, String> entry : map.entrySet())
{
    System.out.println(entry.getKey() + "/" + entry.getValue());
}
```

[Map.Entry : How to use it?](https://stackoverflow.com/questions/8689725/map-entry-how-to-use-it)     
    
    

[Interface Map.Entry<K,V>](https://docs.oracle.com/javase/7/docs/api/java/util/Map.Entry.html)   


#### How to convert a Map to List in Java?
[How to convert a Map to List in Java?](https://stackoverflow.com/questions/1026723/how-to-convert-a-map-to-list-in-java)   


