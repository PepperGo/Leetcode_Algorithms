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

```
Convert List to Set
Set set = new HashSet(list);

Convert Set to List
List list = new ArrayList(set);
```  
