What is time complexity

As we get more experience with coding, we will want to know how we can make our code runs more efficiently. We can do this by finding the time complexity. Time complexity is the number of time a statement is being executed as element size grows (eventually to Infinity). 


![time complexity](/img/time_complexity.jpg)

image credit
https://www.freecodecamp.org/news/content/images/2021/06/1_KfZYFUT2OKfjekJlCeYvuQ.jpeg

The basic time complexity are O(1), O(log n), and O(n). 

O(n*log n), O(n^2) and O(mn) are calculated based on the above 3 time complexity.

There are also  O(2^n) and O(n!) which could be lead to Infinity, so we are not discussing it here. 

<b>O(1)</b>
    
```
let x=0
let temp=x
let y=x+1
return temp
for(let x=0, i=0;i<3;i++){
    x++
}
```
Time complexity does not change. ie, constant amount of time is used to execute each line of code.

<b>O(n)</b>

```
for(let i=0;i<n;i++)
    x++
```
Time complexity chnages according to n. ie, linear amount of time is used to execute the code in the for loop.
Time complexity for searching an item in an array from position 0 is O(n). We only consider the worst case, which means we check every item in teh array from begining to end.

<b>O(log n)</b>
```
example:
let i=1
while(i<n)
    i*=2
```
In the example, i is doubled and getting closer to n in every loop. The number of loops to reach n is x=log2(n)
Time complexity of binary search is O(log n). we repeatedly divided the sorted array in half and look for which gorup the target will be. Its more efficient than checking every item in the array.

It seems straighe forward to calculate time complexity in the above examples when the code is short. In reality our code is way longer and complex. We are not displaying all the time complexity with a long strand of every operation. We only count the dormant ones and ignore constants and lower order ones. 
Thus O(1) operations within for or while loop are often ignored. When we calculated time, we only considered worst case scenario in the loop. 


<b>O(n log n)</b>

```
for(let i=0;i<n;i++){
    let i=1
    while(i<n)
        i*=2
}
```
Here we have a while loop (O(log n)) being run n time, thus we have O(n * O(log n * O(1))) = O(n log n)

<b>O(n^2)</b> 
```
for(let r=0;r<n;r++){
    for(let c=0;c<n;c++){
        matrix[r][c]=1
    }
}
```
In this 2D array we have a for loop within a for loop with same number of cycel, ie O(n * O(n * O(1))) = O(n^2)

<b>O(mn)</b>
In the case the 2d array with diffenet sizes
```
for(let r=0;r<m;r++){
    for(let c=0;c<n;c++){
        matrix[r][c]=1
    }
}
```
We still have a for loop within a for loop, but this time the number of cycles in worst case are different. ie O(m * O(n * O(1))) = O(mn)

Here is a more complicated example:
```
for(let j=0;j<3;j++){  //O(1)
    for(let i=0;i<n;i++){ //O(n)
        let i=1
        while(i<n)   //O(logn)
            i*=2
    }
}
```
O(3*O(n * O(log n *(O(1))))) is shorten to O(nlogn)
this process of ignoring thh lower term is known as Big O notation.






