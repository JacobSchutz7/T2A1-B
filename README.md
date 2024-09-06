# T2A1-B: Workbook Part B

## Q1
Identify and explain the workings of TWO sorting algorithms and discuss and compare their performance/efficiency (i.e Big O)

#### Linear Search

##### Description
Linear Search is a very simple search algorithm that works be checking each element of a list sequentially until the target element is found or the list ends. 

Here is an example of how this algorithm could work step by step:
1. Starting with the first element of the list, compare the current element with the target element.
2. If they match, return the index of the element. 
3. If they do not match, move to the next element and repeat the above steps. 
4. If the target element is not found return a special value (e.g. -1) indicating that the element is not present in the given list. 

##### Performance
- Best case time complexity: the best case for this algorithm is if the target element is found in the first element of the list. In this case Linear Search completes in constant time and is noted as $O(1)$. This means that the time to complete is always the same no matter the size of the data being searched.
- Worst case time complexity: the worst case for this algorithm is if the target element is not present. In this case every element must be searched and compared before completing with a non-result. Searching every single element in this way is noted as $O(n)$. This is known as linear complexity meaning that the time complexity will always linearly increase or decrease with the size of the data being searched. 
- Average case time complexity: on average this algorithm will search and compare half of the elements in the given list. This means that the time complexity of the average case grows linearly as the average will increase as the size of the data being searched increases. This is noted as $O(n)$. 
- Space complexity: the space complexity of this algorithm is $O(1)$ because the algorithm is able to function in-place, meaning that it does not require creating or modifying new data structures in order to function. It takes the given list and applies the steps directly to it. 

##### Efficiency 
The Linear Search algorithm is simple but very inefficient for large datasets due to its linear time complexity. It can be useful for small unsorted datasets. Edge cases like the target element being the first element (best case) or the target element not being present (worst case) significantly effect the performance. 

#### Binary Serach 

##### Description
The Binary Search algorithm works by continually dividing the search interval in a sorted list in half. 

Here is an example of the steps for a Binary Search algorithm: 
- The target element is compared with the middle element of a sorted list. If the target element is less than the middle element the search continues in left (lower) side of the list. If the target element is higher than the target element then the search continues in right (higher) side of the list. 
- The remaining space in the list is what is referred to as the search interval. The middle value of the search interval is then compared in the same way as the previous step. 
- The algorithm continues dividing the list down further and further until it finds the target element or confirms that the target element is not present, in which case it will return a non-result (e.g. -1). 

##### Performance
- Best case time complexity: if the middle element of the sorted list matches the target element in the first comparison then the algorithm completes in constant time, $O(n)$ .
- Worst case time complexity: this algorithm cuts the list in half with each iteration which results in a logarithmic time complexity meaning that after log $n$ operations, only one element remains (and is either the target or not, in which case the algorithm returns a non-result). This is noted as $O($log $n)$ .
- Average case time complexity: the average case of this algorithm also has logarithmic complexity. Regardless of the structure, as long as the data is sorted, the algorithm will keep halving the search space or search interval. The number of times this halving process needs to happen scales logarithmically, meaning that the dataset has to increase significantly for this number to go up. This is noted as $O($log $n)$ . 
- Space complexity: this differs depending on whether the version of the algorithm being used. The iterative version has a space complexity of $O(1)$ because no additional memory is needed to compute. The recursive version has a space complexity of $O($log $n)$ because the number of recursions will increase with the number of times the search space is halved, as discussed above. 

##### Efficiency 
Binary Search is a very efficient algorithm for large sorted datasets. The main drawback is that it requires a sorted dataset so it is not applicable to dynamic or unsorted data. The edge cases, when the target element is exactly in the middle of the dataset (best case) or when not able to find it at all (worst case), still present a relatively stable performance because of the logarithmic nature of the algorithm. This means that even in the worst case Binary Search is still an efficient algorithm to use in large datasets. 

#### Comparison
Linear Search is clearly more suited to small and unsorted datasets. This is because its linear complexity increases too much for larger datasets but stays low for small datasets. The Binary Search is almost the opposite. It must be used on sorted data to work and it is efficient with large datasets because of its logorithmic complexity.