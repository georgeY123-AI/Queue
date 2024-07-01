### Queue

A queue is a linear data structure that follows the First-In-First-Out (FIFO) principle. Elements are added to the rear (enqueue) and removed from the front (dequeue).

#### Operations and Time Complexity

1. **Enqueue (Insert at the end)**:
   - **Array-based implementation**: O(1)
   - **Linked-list implementation**: O(1)

2. **Dequeue (Remove from the front)**:
   - **Array-based implementation**: O(n) (due to shifting elements)
   - **Linked-list implementation**: O(1)

3. **Access (Peek at the front)**:
   - **Array-based implementation**: O(1)
   - **Linked-list implementation**: O(1)

#### Use Cases
- **Real-World Example**: Printer spooling, where print jobs are processed in the order they arrive.
- **Real-World Example**: Task scheduling, where tasks are executed in the order they are added.

### Priority Queue

A priority queue is a special type of queue where each element is associated with a priority, and elements are dequeued based on their priority. There are several ways to implement a priority queue, such as using a heap, an unordered list, or an ordered list.

#### Operations and Time Complexity

1. **Insert (Enqueue)**:
   - **Unordered list**: O(1)
   - **Ordered list**: O(n)
   - **Binary heap**: O(log n)

2. **Remove (Dequeue) the highest priority element**:
   - **Unordered list**: O(n) (finding the highest priority element)
   - **Ordered list**: O(1)
   - **Binary heap**: O(log n)

3. **Access (Peek) the highest priority element**:
   - **Unordered list**: O(n)
   - **Ordered list**: O(1)
   - **Binary heap**: O(1)

#### Use Cases
- **Real-World Example**: Task scheduling in operating systems, where high-priority tasks are executed before lower-priority tasks.
- **Real-World Example**: Dijkstra's algorithm for finding the shortest path, where the priority queue is used to process nodes based on their distance from the source.

### Summary Table

| Operation                      | Queue (Array) | Queue (Linked List) | Priority Queue (Unordered List) | Priority Queue (Ordered List) | Priority Queue (Binary Heap)  |
|--------------------------------|---------------|----------------------|---------------------------------|-------------------------------|------------------------------|
| Enqueue (Insert)               | O(1)          | O(1)                 | O(1)                            | O(n)                          | O(log n)                     |
| Dequeue (Remove)               | O(n)          | O(1)                 | O(n)                            | O(1)                          | O(log n)                     |
| Access (Peek)                  | O(1)          | O(1)                 | O(n)                            | O(1)                          | O(1)                         |

### When to Use Each Type

- **Queue (Array-based)**: Use when you need a simple FIFO structure and can afford the cost of dequeuing with element shifting. Example: simple buffering where dequeuing frequency is low.
- **Queue (Linked-list-based)**: Use when frequent enqueue and dequeue operations are needed without the overhead of shifting elements. Example: task scheduling in systems with frequent task arrivals and completions.
- **Priority Queue (Unordered List)**: Use when the priority of elements is dynamic, and you can afford linear time complexity for dequeue operations. Example: scheduling tasks with dynamically changing priorities.
- **Priority Queue (Ordered List)**: Use when you need fast access to the highest priority element and can afford linear time complexity for insertion. Example: maintaining a sorted list of tasks where insertion order matters.
- **Priority Queue (Binary Heap)**: Use when you need a balanced trade-off between insertion and removal operations. Example: implementing algorithms like Dijkstra’s shortest path or A* search.

Each data structure has its advantages and is suited to different scenarios based on the specific requirements of the application.
