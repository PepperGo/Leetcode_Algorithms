## Binary Search

### 50. Pow(x, n)
#### n is a 32-bit signed integer, within the range [−2^31, 2^31 − 1]
n is a 32-bit signed integer as stated in the note. If n = INT_MIN, -n will overflow.


### 278. First Bad Version
#### Binary Search [a, b)
[Solution](https://github.com/PepperGo/Leetcode_Algorithms/blob/master/278.%20First%20Bad%20Version)    

[左开右闭写法](https://www.zhihu.com/question/36132386/answer/530313852)   

2147483647 + 1 = -2147483648


### 34. Find First and Last Position of Element in Sorted Array
#### Binary Search
注意binary search函数的返回值判断！[Solution](https://github.com/PepperGo/Leetcode_Algorithms/blob/master/034.%20Find%20First%20and%20Last%20Position%20of%20Element%20in%20Sorted%20Array)    



### 528. Random Pick with Weight
#### Generate Random Number
[How do I generate random integers within a specific range in Java?](https://stackoverflow.com/questions/5887709/getting-random-numbers-in-java)   
```
 Random rand;
 // nextInt is normally exclusive of the top value,
 // so add 1 to make it inclusive
 int randomNum = rand.nextInt((max - min) + 1) + min;
 
 //The Sun documentation explicitly says that you should better use Random() if you need an int instead of Math.random() which produces a double.   
 
```   

### 367. Valid Perfect Square
#### Integer square root
[Integer square root](https://en.wikipedia.org/wiki/Integer_square_root#Using_only_integer_division)   




