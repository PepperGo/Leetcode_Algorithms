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






