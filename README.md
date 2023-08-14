# algorithm-visualizer
This repository contains various functions that allow for the visualization of common algorithms taught in computer science courses, such as 
bubble sort, selection sort, binary search, tree traversals, and tree operations. Animations are made possible through the [AlgViz visualization tool](https://algviz.com/index_en.html).

## Examples

### Sorting Algorithms
#### Bubble Sort
![bubble_sort_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/03714fcf-2043-4252-aa54-0c8e4ee615ac)
Bubble sort is a `O(n^2)` sorting algorithm that works by swapping the largest element with adjacent element until it
reaches the end of the array. For an array of length
`n`, once the largest element is swapped to index `n-1`, the algorithm continues by swapping the next largest element to index `n-2`. 
##### Colouring Scheme
- 🟦 *Blue*: Current largest element detected.
- 🟥 *Red*: Element being compared to current largest element. This element will change to blue if it's larger than the current blue element.
- 🟩 *Green*: Once an element is swapped to its final position, it's coloured in green and will no longer be swapped.


#### Selection Sort
![selection_sort_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/7a343493-4052-4e4d-9e4f-0a249511b96a)
Selection sort is a `O(n^2)` sorting algorithm that works by swapping the minimum element to the start of the array. For an array of length
`n`, once the minimum element is swapped to index `0`, the algorithm continues by searching for the next minimum element in indices `[1:n]`.
##### Colouring Scheme
- 🟦 *Blue*: Current minimum element detected.
- 🟥 *Red*: Element being compared to current minimum element. This element will change to blue if it's smaller than the current blue element.
- 🟩 *Green*: Once an element is swapped to its final position, it's coloured in green and will no longer be swapped.

### Search Algorithms

#### Binary Search
![binary_search_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/8fc2760b-a529-4c4b-92bb-c46ebc587e81)
Binary search is a `O(log(n))` search algorithm that operates under the assumption that the array is already sorted in ascending order. 
An `array` and a `target` element in the array are passed as input. The algorithm works by using pointers to the `left`, `right`, and `mid` indices of the search space. It then checks whether the element `mid` index contains the `target` element; if it does, the algorithm terminates and returns the index, otherwise the search continues, but the search spaces is reduced by checking whether the `target` or greater than or less than the `mid` element. Depending
on the result, the algorithm will only search for element to the right or left the `mid` element and adjusts the pointers accordingly. Once the `left` and `right` pointers have crossed over each other, the algorithm terminates and returns a value indicating failure.

### Depth-First Binary Tree Traversals
The following binary tree traversals are all example of depth first searches, which run in `O(n+m)`, where `n` is the number of nodes and `m` is the number
of edges in the tree. The order of the traversals is indicated by the order in which nodes are coloured in green.

#### Creating a Tree
Trees can be created by creating a list of the nodes of the tree in **left to right, top to bottom** order. This means the root of the tree is at
index `0` and the bottom rightmost node is at the end of the list. If a node does not have a child, fill thart index with `None`.
The following is an example of some Python code to generate a tree.

`Python Code`
``` python
tree_info = [3,2,5,1,None,4,6]
tree = binaryTree(tree_info=tree_info)
```

`Resulting Tree`

<img width="180" alt="image" src="https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/b37b20cd-bd5b-4308-92d2-ed238777091e">

##### Colouring Scheme
- 🟦 *Blue*: Visited node.
- 🟩 *Green*: Completed node.

#### Pre-Order Traversal
`Pseudocode`
1. Visit the root.
2. Visit left subtree
3. Visit the right subtree.

![binary_tree_preorder_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/9f0c9afc-80c3-48bd-ab0b-48860f067149)

#### Post-Order Traversal
`Pseudocode`
1. Visit left subtree
2. Visit the right subtree.
3. Visit the root.


![binary_tree_postorder_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/dde00f41-85e3-4b41-9452-774b6adcd731)

#### In Order Traversal
`Pseudocode`
1. Visit left subtree
2. Visit the root.
3. Visit the right subtree.

Once the traversal is complete on a binary search tree, the nodes will have been traversed in non-decreasing order, since smaller children (ie. elements in left subtrees) are always marked before the root, and the root is always marked before the larger children (ie. the elements in the right subtree).
![binary_tree_inorder_gif](https://github.com/jikaelgagnon/algorithm-visualizer/assets/82888595/7e8f9074-88b2-489e-853a-2e6b8399bc43)

### Other Functions
Other functions include:
- Searching a binary tree
- Insertion into a binary tree
- Finding the max/min in a binary tree



