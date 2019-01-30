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

#### Collections.max
```
public static <T extends Object & Comparable<? super T>> T max(Collection<? extends T> coll)
Returns the maximum element of the given collection, according to the natural ordering of its elements. All elements in the collection must implement the Comparable interface. Furthermore, all elements in the collection must be mutually comparable (that is, e1.compareTo(e2) must not throw a ClassCastException for any elements e1 and e2 in the collection).
This method iterates over the entire collection, hence it requires time proportional to the size of the collection.

Parameters:
coll - the collection whose maximum element is to be determined.
Returns:
the maximum element of the given collection, according to the natural ordering of its elements.
```
#### Iterate through a HashMap?
[Iterate through a HashMap](https://stackoverflow.com/questions/1066589/iterate-through-a-hashmap)
 keySet(), values(), entrySet()
 
 
#### iterate through Hashtable?
[](http://www.java2novice.com/java-collections-and-util/hashtable/iterate/)



### 105. Construct Binary Tree from Preorder and Inorder Traversal  
#### [If you are given two traversal sequences, can you construct the binary tree?](https://www.geeksforgeeks.org/?p=657/)  


#### [Construct Tree from given Inorder and Preorder traversals](https://www.geeksforgeeks.org/construct-tree-from-given-inorder-and-preorder-traversal/)   
```
Algorithm: buildTree()
1) Pick an element from Preorder. Increment a Preorder Index Variable (preIndex in below code) to pick next element in next recursive call.
2) Create a new tree node tNode with the data as picked element.
3) Find the picked element’s index in Inorder. Let the index be inIndex.
4) Call buildTree for elements before inIndex and make the built tree as left subtree of tNode.
5) Call buildTree for elements after inIndex and make the built tree as right subtree of tNode.
6) return tNode.

```   

#### [Construct a Binary Tree from Postorder and Inorder](https://www.geeksforgeeks.org/construct-a-binary-tree-from-postorder-and-inorder/)   
```
Let us see the process of constructing tree from in[] = {4, 8, 2, 5, 1, 6, 3, 7} and post[] = {8, 4, 5, 2, 6, 7, 3, 1}
1) We first find the last node in post[]. The last node is “1”, we know this value is root as root always appear in the end of postorder traversal.

2) We search “1” in in[] to find left and right subtrees of root. Everything on left of “1” in in[] is in left subtree and everything on right is in right subtree.

         1
       /    \
[4, 8, 2, 5]   [6, 3, 7] 
3) We recur the above process for following two.
….b) Recur for in[] = {6, 3, 7} and post[] = {6, 7, 3}
…….Make the created tree as right child of root.
….a) Recur for in[] = {4, 8, 2, 5} and post[] = {8, 4, 5, 2}.
…….Make the created tree as left child of root.

```

#### [Construct Full Binary Tree from given preorder and postorder traversals](https://www.geeksforgeeks.org/full-and-complete-binary-tree-from-given-preorder-and-postorder-traversals/)  
It is not possible to construct a general Binary Tree from preorder and postorder traversals.  

But if know that the Binary Tree is Full, we can construct the tree without ambiguity.
```
Let us consider the two given arrays as pre[] = {1, 2, 4, 8, 9, 5, 3, 6, 7} and post[] = {8, 9, 4, 5, 2, 6, 7, 3, 1};
In pre[], the leftmost element is root of tree. Since the tree is full and array size is more than 1. The value next to 1 in pre[], must be left child of root. So we know 1 is root and 2 is left child. How to find the all nodes in left subtree? We know 2 is root of all nodes in left subtree. All nodes before 2 in post[] must be in left subtree. Now we know 1 is root, elements {8, 9, 4, 5, 2} are in left subtree, and the elements {6, 7, 3} are in right subtree.

```

### 280. Wiggle Sort  
#### [Sorting algorithm](https://en.wikipedia.org/wiki/Sorting_algorithm)    

[Sorting Algorithms Details](https://www.geeksforgeeks.org/sorting-algorithms/)

##### [Selection Sort](https://www.geeksforgeeks.org/selection-sort/)  
It has O(n^2) time complexity  

##### [Insertion sort](https://www.geeksforgeeks.org/insertion-sort/)  
It has O(n^2) time complexity    


##### [Quicksort](https://www.geeksforgeeks.org/quick-sort/)
on average, the algorithm takes O(nlogn) comparisons to sort n items.   

in the worst case, it makes O(n^2) comparisons  


##### [Merge sort](https://www.geeksforgeeks.org/merge-sort/) 
Best: nlogn  

Average: nlogn  

##### [Heapsort](https://www.geeksforgeeks.org/heap-sort/)
nlogn  

#### [Bubble Sort](https://www.geeksforgeeks.org/bubble-sort/) 
on average, the algorithm takes O(n^2) comparisons to sort n items.   

in the best case, it makes O(n) comparisons    


### 621. Task Scheduler
#### PriorityQueue
[PriorityQueue (Java Platform SE 7 ) - Oracle Docs](https://docs.oracle.com/javase/7/docs/api/java/util/PriorityQueue.html)     
[PriorityQueue in Java](https://www.geeksforgeeks.org/priority-queue-class-in-java-2/)   

PriorityQueue<Integer> pq = new PriorityQueue<>(26, Collections.reverseOrder());  
  
  
[Collections (Java Platform SE 7 ) - Oracle Docs](https://docs.oracle.com/javase/7/docs/api/java/util/Collections.html)     


### Heaps and Priority Queues
[Heaps and Priority Queues](https://www.hackerearth.com/practice/notes/heaps-and-priority-queues/)    


### 380. Insert Delete GetRandom O(1)
#### get random int
[How do I generate random integers within a specific range in Java?](https://stackoverflow.com/questions/363681/how-do-i-generate-random-integers-within-a-specific-range-in-java)     

```
Random ran = new Random();
int x = ran.nextInt(6) + 5;

5 ~ 10
```


### 215. Kth Largest Element in an Array
#### int[] and Integer[]
```
Arrays.sort(arr, Collections.reverseOrder());
Arrays.sort(arr, new Comparator<Integer>(){
  ...});
Can't use for int[]
```   

### 480. Sliding Window Median
#### PriorityQueue
[PriorityQueue](https://docs.oracle.com/javase/8/docs/api/java/util/PriorityQueue.html)    
Implementation note: this implementation provides:   

O(log(n)) time for the enqueuing and dequeuing methods (offer, poll, remove() and add);    

linear time for the remove(Object) and contains(Object) methods;    

constant time for the retrieval methods (peek, element, and size).   


#### Heap vs Binary Search Tree (BST)
[Heap vs Binary Search Tree (BST)](https://stackoverflow.com/questions/6147242/heap-vs-binary-search-tree-bst)   

Heap just guarantees that elements on higher levels are greater (for max-heap) or smaller (for min-heap) than elements on lower levels, whereas BST guarantees order (from "left" to "right"). If you want sorted elements, go with BST.  


Heap is better at findMin/findMax (O(1)), while BST is good at all finds (O(logN)). Insert is O(logN) for both structures. If you only care about findMin/findMax (e.g. priority-related), go with heap. If you want everything sorted, go with BST.   



