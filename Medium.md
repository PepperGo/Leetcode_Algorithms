### 17. Letter Combinations of a Phone Number
#### 1. HashMap -> String[]
```
private HashMap<Character, String> hashMap = new HashMap<Character, String>();
String digitletter[] = {"","","abc","def","ghi","jkl","mno","pqrs","tuv","wxyz"};
```
Index of string array can be the key.

#### 2. char to String
- String.valueOf()
- Character.toString()  

Character, not Charactor

#### 3. char to Integer
- Get ASCII value
- Character.getNumericValue() 

#### 4. String.substring(...)   //not subString() X
- indexOf  
indexOf(String str): Returns the index within this string of the first occurrence of the specified substring.  
int	indexOf(String str, int fromIndex): Returns the index within this string of the first occurrence of the specified substring, starting at the specified index.
```

```

- substring  
substring(int beginIndex): Returns a new string that is a substring of this string.  
String	substring(int beginIndex, int endIndex): Returns a new string that is a substring of this string.
```
 "hamburger".substring(4, 8) returns "urge"
 "smiles".substring(1, 5) returns "mile"
```
#### 5. How do I apply the for-each loop to every character in a String?
[How do I apply the for-each loop to every character in a String?](https://stackoverflow.com/questions/2451650/how-do-i-apply-the-for-each-loop-to-every-character-in-a-string)  
```
for (char ch: "xyz".toCharArray()) {
}
```
