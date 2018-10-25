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
