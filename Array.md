# Array

### 1. Two Sum
#### Arrays.binarySearch
```
public static int binarySearch(Object[] a, Object key)
Searches the specified array for the specified object using the binary search algorithm. The array must be sorted into ascending order according to the natural ordering of its elements (as by the sort(Object[]) method) prior to making this call. If it is not sorted, the results are undefined. (If the array contains elements that are not mutually comparable (for example, strings and integers), it cannot be sorted according to the natural ordering of its elements, hence results are undefined.) If the array contains multiple elements equal to the specified object, there is no guarantee which one will be found.  

Returns:
index of the search key, if it is contained in the array;   
otherwise, (-(insertion point) - 1). The insertion point is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or a.length if all elements in the array are less than the specified key. Note that this guarantees that the return value will be >= 0 if and only if the key is found.  

```

#### HashMap
##### get()
```
public V get(Object key)  
Returns the value to which the specified key is mapped, or null if this map contains no mapping for the key.
```

##### getOrDefault()
```
public V getOrDefault(Object key, V defaultValue)   
Returns the value to which the specified key is mapped, or defaultValue if this map contains no mapping for the key.
```

### 167. Two Sum II - Input array is sorted  
#### How to Throw an Exception in Java  

```
throw new IllegalArgumentException("No two sum solution");
```

### 169. Majority Element  
#### HashMap Iterate
[How to efficiently iterate over each entry in a Java Map?](https://stackoverflow.com/questions/46898/how-to-efficiently-iterate-over-each-entry-in-a-java-map)  


### 15. 3Sum
#### Arrays.asList
```
public static <T> List<T> asList(T... a)
Returns a fixed-size list backed by the specified array. (Changes to the returned list "write through" to the array.) This method acts as bridge between array-based and collection-based APIs, in combination with Collection.toArray(). The returned list is serializable and implements RandomAccess.
```
List<String> stooges = Arrays.asList("Larry", "Moe", "Curly");
  
#### ArrayList<ArrayList<String>> listOLists = new ArrayList<ArrayList<String>>();
ArrayList<ArrayList<String>> listOLists = new ArrayList<ArrayList<String>>();  
    
### 56. Merge Intervals  
####  Comparator<T> Interface
[Comparator Interface in Java with Examples](https://www.geeksforgeeks.org/comparator-interface-java/)     
  
```
    Collections.sort(intervals, new IntervalComparator());  
  
    private class IntervalComparator implements Comparator<Interval> {
        @Override
        public int compare(Interval a, Interval b) {
            return a.start < b.start ? -1 : a.start == b.start ? 0 : 1;
        }
    }

```  
To compare two elements, it asks “Which is greater?” Compare method returns -1, 0 or 1 to say if it is less than, equal, or greater to the other.  


### 118. Pascal's Triangle
#### ArrayList<ArrayList<>> and List<List<>>
[Incompatible types List of List and ArrayList of ArrayList](https://stackoverflow.com/questions/24796273/incompatible-types-list-of-list-and-arraylist-of-arraylist)   


### 152. Maximum Product Subarray  
#### kadane's algorithm  
[Largest Sum Contiguous Subarray](https://www.geeksforgeeks.org/largest-sum-contiguous-subarray/)  


### 153/154. Find Minimum in Rotated Sorted Array I, II
#### mid = start + (end - start)/2; 
mid = (start + end)/2: binary search bug: if the size of array are too large, equal or larger than the upper bound of int type, hi + lo may cause an overflow and become a negative number. mid = start + (end - start)/2;   


### 142. Linked List Cycle II  
#### Floyd's Tortoise and Hare
Proof: [Solution](https://leetcode.com/problems/linked-list-cycle-ii/solution/)  

### 229. Majority Element II 
#### Majority Voting Algorithm  
[Majority Voting Algorithm](https://gregable.com/2013/10/majority-vote-algorithm-find-majority.html)    

#### Array to List
public static <T> List<T> asList(T... a)
Returns a fixed-size list backed by the specified array. (Changes to the returned list "write through" to the array.) This method acts as bridge between array-based and collection-based APIs, in combination with Collection.toArray(). The returned list is serializable and implements RandomAccess.  
  
This method also provides a convenient way to create a fixed-size list initialized to contain several elements:   
List<String> stooges = Arrays.asList("Larry", "Moe", "Curly");
  
### 79. Word Search  
#### boolean
boolean (correct)
Boolean (incorrect)  


### 39. Combination Sum
#### Subsets, Permutations, Combination Sum, Palindrome Partitioning
[Subsets, Permutations, Combination Sum, Palindrome Partitioning](https://leetcode.com/problems/combination-sum/discuss/16502/A-general-approach-to-backtracking-questions-in-Java-(Subsets-Permutations-Combination-Sum-Palindrome-Partitioning))   

#### list.add(new ArrayList<>(tempList));

### 189. Rotate Array
#### Reverse array
```
    
    public void reverse(int[] nums, int start, int end){
        while(start < end){
            int temp = nums[start];
            nums[start] = nums[end];
            nums[end] = temp;
            start++;
            end--;
        }
    }
```   

### 120. Triangle
#### List to Array  
```  
    List<Integer> sourceList = Arrays.asList(0, 1, 2, 3, 4, 5);
    Integer[] targetArray = sourceList.toArray(new Integer[sourceList.size()]);

```
toArray <T> T[] toArray(T[] a)
  
Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. If the list fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this list.
If the list fits in the specified array with room to spare (i.e., the array has more elements than the list), the element in the array immediately following the end of the list is set to null. (This is useful in determining the length of the list only if the caller knows that the list does not contain any null elements.)

Like the toArray() method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose x is a list known to contain only strings. The following code can be used to dump the list into a newly allocated array of String:


     String[] y = x.toArray(new String[0]);
 
Note that toArray(new Object[0]) is identical in function to toArray().   

[java.util Interface List\<E\>](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)  
  
  
### 697. Degree of an Array
#### HashMap, HashTable
[彻底搞懂HashMap,HashTable,ConcurrentHashMap之关联](https://blog.csdn.net/cn_yaojin/article/details/78790221)  
