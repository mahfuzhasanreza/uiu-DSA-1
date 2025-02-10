1. **Time complexity of `heapify()`:**  
   \( O(\log n) \)

2. **Index of the parent of node \( i \) in a heap:**  
   \[
   \text{Parent}(i) = \left\lfloor \frac{i-1}{2} \right\rfloor
   \]

3. **Number of internal nodes in a heap:**  
   \[
   \left\lfloor \frac{n}{2} \right\rfloor
   \]

4. **Index of the minimum-valued node in a min-heap:**  
   \( 0 \) (for 0-based indexing)