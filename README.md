# algorithm-visualizer
This repository contains various functions that allow for the visualization of common algorithms taught in computer science courses, such as 
bubble sort, selection sort, binary search, tree traversals, and tree operations. Animations are made possible through the [AlgViz visualization tool](https://algviz.com/index_en.html).

## Examples
### Example 1: Bubble Sort
![bubble_sort_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/03714fcf-2043-4252-aa54-0c8e4ee615ac)
Bubble sort is a `O(n^2)` sorting algorithm that works by swapping the largest element with adjacent element until it
reaches the end of the array. For an array of length
`n`, once the largest element is swapped to index `n-1`, the algorithm continues by swapping the next largest element to index `n-2`. 
#### Colouring Scheme
- 🟦 *Blue*: Current largest element detected.
- 🟥 *Red*: Element being compared to current largest element. This element will change to blue if it's larger than the current blue element.
- 🟩 *Green*: Once an element is swapped to its final position, it's coloured in green and will no longer be swapped.


### Example 2: Selection Sort
![selection_sort_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/7a343493-4052-4e4d-9e4f-0a249511b96a)
Selection sort is a `O(n^2)` sorting algorithm that works by swapping the minimum element to the start of the array. For an array of length
`n`, once the minimum element is swapped to index `0`, the algorithm continues by searching for the next minimum element in indices `[1:n]`.
#### Colouring Scheme
- 🟦 *Blue*: Current minimum element detected.
- 🟥 *Red*: Element being compared to current minimum element. This element will change to blue if it's smaller than the current blue element.
- 🟩 *Green*: Once an element is swapped to its final position, it's coloured in green and will no longer be swapped.

### Example 3: Binary Search
![binary_search_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/8fc2760b-a529-4c4b-92bb-c46ebc587e81)
Binary search is a `O(log(n))` search algorithm that operates under the assumption that the array is already sorted in ascending order. 
An `array` and a `target` element in the array are passed as input. The algorithm works by using pointers to the `left`, `right`, and `mid` indices of the search space. It then checks whether the element `mid` index contains the `target` element; if it does, the algorithm terminates and returns the index, otherwise the search continues, but the search spaces is reduced by checking whether the `target` or greater than or less than the `mid` element. Depending
on the result, the algorithm will only search for element to the right or left the `mid` element and adjusts the pointers accordingly. Once the `left` and `right` pointers have crossed over each other, the algorithm terminates and returns a value indicating failure.
