## Heap

### 295. Find Median from Data Stream
#### Heap
[Priority Queue | Set 1 (Introduction)](https://www.geeksforgeeks.org/priority-queue-set-1-introduction/)   

[Heaps and Priority Queues](https://www.hackerearth.com/practice/notes/heaps-and-priority-queues/)    


#### PriorityQueue\<Integer\>

```
    PriorityQueue<Integer> smallHalf = new PriorityQueue<>(new Comparator<Integer>(){
        public int compare(Integer a, Integer b){
            return b - a;
        }
    });

```   

##### add(), offer()  

[What is the difference between the add and offer methods in a Queue in Java?](https://stackoverflow.com/questions/2703984/what-is-the-difference-between-the-add-and-offer-methods-in-a-queue-in-java)   

```
add() comes from Collection, throw Exception
offer() comes from Queue, return false  
```   


  
