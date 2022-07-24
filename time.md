What is time complexity

As we get more experience with coding, we will want to know how we can make our code runs more efficiently. We can do this by finding the time complexity. Time complexity is the number of time a statement is being executed as element size grows (eventually to Infinity). 

graph goes here

the time complexity we run into most often are O(1), O(log n), O(n).

O(n*log n), O(n^2) and O(mn) are calculated based on the above 3 time complexity.

there are also  O(2^n) and O(n!) which are rearly involved as the time could be Infinity, so we are not discussing it here. 

O(1)
example: 
let x=0
let temp=x
let y=x+1
return temp

Time complexity does not change. ie, constant amount of time is used to execute each line of code. No cycle involved. 

O(n)
example:
for(let i=0;i<n;i++)
    x++

Time complexity chnages according to n. ie, linear amount of time is used to execute the code in the for loop.
Time complexity for searching an item in an array from position 0 is O(n). It depends on the position of the item. Worst case is the last item. 

O(log n)
example:
let i=1
while(i<n)
    i*=2

in the example, i is doubled and getting closer to n in every loop. The number of loops to reach n is x=log2(n)
Time complexity of binary search is O(log n). we repeatedly divided the sorted array in half and look for which gorup the target will be. Its more efficient than checking every item in the array.

in the above time complexity, we have simple O(1) operations inside the for or while loop. When we calculated time, we only considered worst case scenario in the loop. Thats why O(1) within is often ignored in a loop. 


O(n log n)
exmple: 

for(let i=0;i<n;i++){
    let i=1
    while(i<n)
        i*=2
}

Here we have a while loop (O(log n)) being run n time, thus we have O(n * O(log n)) = O(n log n)

O(n^2) 
for(let r=0;r<n;r++){
    for(let c=0;c<n;c++){
        matrix[r][c]=1
    }
}
In this 2D array we have a for loop within a for loop, ie O(n * O(n)) = O(n^2)

In the case the 2d array is not same size
for(let r=0;r<m;r++){
    for(let c=0;c<n;c++){
        matrix[r][c]=1
    }
}
We still have a for loop within a for loop, ie O(m * O(n)) = O(mn)


It seems straighe forward to calculate time complexity in the above examples when the code is short. In reality our code is way longer and complex. We are not displaying all the time with a long strand of every operation. we only count the dormant ones and ignore constants and lower order terms. E.g. O(3*n^2 + 10n + 10) becomes O(n^2).





