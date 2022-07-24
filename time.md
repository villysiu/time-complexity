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

Time complexity varies according to n. ie, linear amount of time is used to execute the code in the for loop.
Time complexity for searching an item in an array from position 0 is O(n). It depends on teh position of the item. WOrst case is the last item. 

O(log n)
example:
let i=1
while(i<n)
    i*=2

in the example, i is doubled and getting closer to n in every loop. The number of loops to reach n is x=log2(n)
Time complexity of binary search is O(log n). we repeatedly divided the sorted array in half and look for which gorup the target will be. Its more efficient than checking every item in the array.

in the above time complexity, we have simple O(1) operations inside the for and while loop. When we calculated time, we only considered worst case scenario in the process. Thats why O(1) is often ignored when there the loop involved. This process is knownn as Big O, aka Big Order function. we only count the dormant term and ignore constants and lower order terms. E.g. O(3*n^2 + 10n + 10) becomes O(n^2).

O(nlog n)
exmple: 

for(let i=0;i<n;i++){
    let i=1
    while(i<n)
        i*=2
}

This is the above while loop (O(log n))being run n time, so we have n(log n)







