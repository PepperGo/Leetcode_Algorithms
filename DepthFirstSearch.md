## Depth First Search

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



