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
