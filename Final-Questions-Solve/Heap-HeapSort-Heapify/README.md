# Final Q. Solve (Heap, Heap Sort, Heapify)

## Spring - 2024


![Image](https://github.com/user-attachments/assets/61e10700-a9fd-40cf-b81b-d58fe120b2f2)  

### Answer to 3(a) [Spring-24]
I) O(log n)

II)  
![Image](https://github.com/user-attachments/assets/fdb61d51-440f-4a65-9ae8-b146b032f8fd)

III) (n-1)/2

IV) In a min-heap, the minimum-valued node is always the root of the heap. Therefore, its index is:\
0 (for 0-based indexing) or 1 (for 1-based indexing)


### Answer to 3(b) [Spring-24]


## Summer - 2024

![Image](https://github.com/user-attachments/assets/61ec8cd1-6672-42e3-9558-2d302b77c2b2)

### Answer to 4(a) [Summer-24]
To sort an array in descending order using the heapsort algorithm with a max-heap, I **do not need to call the `Build-Heap` function before starting the sorting process**. Here's why:\
In a max-heap, the largest element is already at the root (index 0). The heapsort algorithm works by repeatedly extracting the maximum element from the heap (which is the root in a max-heap) and placing it at the end of the array. After each extraction, the heap property is restored by calling `heapify` on the reduced heap. However, if the array is not a max-heap, I would need to call `Build-Heap` to transform it into a max-heap before starting the sorting process.\
So, if the array is already a max-heap, I can proceed with the sorting without calling `Build-Heap`.\

**Answer to 4(b):**

## Summer - 2023

![Image](https://github.com/user-attachments/assets/9b81ac03-fea4-42ae-b629-c17e3903f241)

### Answer to 2(a) [Summer-23]
No, running `Max-Heapify` on the first node (index 1) does not necessarily convert the given heap into a max-heap.  

**Reason:**  
The `Max-Heapify` function assumes that the subtrees rooted at the left and right children of the current node are already max-heaps. It only ensures that the subtree rooted at the current node becomes a max-heap. However, in the provided heap, some subtrees are not max-heaps initially. Therefore, simply running `Max-Heapify` on the root will not fix violations further down the tree.  

**Proposed Algorithm:**  
To convert the entire heap into a max-heap, use the **Build-Max-Heap** algorithm, which calls `Max-Heapify` starting from the last non-leaf node up to the root.  

**Pseudocode for `Build-Max-Heap`:**
```
Build-Max-Heap(A)
1. for i = floor(A.heap-size/2) downto 1
2.     Max-Heapify(A, i)
```
