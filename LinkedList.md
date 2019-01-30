## LinkedList

### 23. Merge k Sorted Lists
#### PriorityQueue
[Confused over compareTo implementation with PriorityQueue](https://stackoverflow.com/questions/39352302/confused-over-compareto-implementation-with-priorityqueue)   
  
[Implement PriorityQueue through Comparator in Java](https://www.geeksforgeeks.org/implement-priorityqueue-comparator-java/)  

```
// Overriding compare()method of Comparator  
// for descending order of cgpa 
public int compare(Student s1, Student s2) { 
    if (s1.cgpa < s2.cgpa) 
      return 1; 
    else if (s1.cgpa > s2.cgpa) 
      return -1; 
    return 0; 
} 

public int compare(Student s1, Student s2) { 
    return s2.cgpa - s1.cgpa;
} 

```  

#### Use Way 2 may case overflow
[Example](https://github.com/PepperGo/Leetcode_Algorithms/blob/master/480.%20Sliding%20Window%20Median)
```
[-2147483648,2147483647,2147483647]

        PriorityQueue<Integer> minQ = new PriorityQueue<Integer>(new Comparator<Integer>(){
            public int compare(Integer i1, Integer i2){
                if(i1 < i2){
                    return 1;
                }else if(i1 > i2){
                    return -1;
                }else
                    return 0;
            }
        }); //max-heap
        
        But this can't work
        PriorityQueue<Integer> minQ = new PriorityQueue<Integer>(new Comparator<Integer>(){
            public int compare(Integer i1, Integer i2){
                return i2 - i1;
            }
        }); //max-heap
```
