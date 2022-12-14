# DSA Theory and Notes

## Heaps And Priority Queue
### Heaps
* Min heap - Every child is larger or equal to its parent
  * Naturally, root is the smallest element
* Max heap - Every child is smaller or equal to its parent
  * Naturally, root is the largest element
* It is a complete tree - all elements are leftmost
  
#### Time Complexity of Basic Operations
![heap operations complexity](heap-operations-complexity.png)

#### Heap Sort
* Heapify the array to be sorted - O(n)
* Remote the root while sifting what is left - O(nlog(n))
* Overall time complexity - O(nlog(n))

### Prioirity Queue
* A practical application of heap, basically it is just a heap, the highest priority element is at the root

#### Time Complexity of Basic Operations
![priority queue operations complexity](priority-queue-operations-complexity.png)

You can use Java Priority Queue as a Heap.

Min Heap: --> to keep the min element always on top, so you can access it in O(1).
```java
PriorityQueue<Integer> minHeap = new PrioirtyQueue<>();
```
Max Heap: --> to keep the max element always on top, the same order as above.
```java
PriorityQueue<Integer> maxHeap = new PriorityQueue<>(Comparator.reverseOrder());
```
Which is the same as ```java(Integer o1, Integer o2) -> Integer.compare(o2, o1) or - Integer.compare(o1, o2)```.

And you can use:
* add --> to add element to the queue. O(log n)
* remove --> to get and remove the min/max. O(log n)
* peek --> to get, but not remove the min/max. O(1)

## Stacks
* Like playing cards stacked on top of each other
* First In Last Out (FILO)
* Methods
  * Peek
  * Push
  * Pop

```java
Stack<Integer> stack = new Stack<>();
```

## Brute Force Approach
* When you try out all possible solutions and pick the ones that are suitable.
* Used to solve problems with multiple possible solutions and you want to make a list or collection of those solutions

### Backtracking
* The solution tree is created using DFS (Depth First Search)

### Branch and Bound
* The solution tree is generated using BFS (Breadth First Search) or level order traversal

## Greedy Approach
* Used to solve min/max or optimization problems subject to some constraints
* There is ofcourse only 1 optimal solution but there could be many feasible solutions
* The problem is solved in stages by eliminating feasible candidates based on some filtering criteria

Imagine a hiring process:
Talent pool - 1000
1. Stage 1 - HR call - 600 candidates passed
2. Stage 2 - Technical assessment 1 - 300 candidates passed
3. Stage 3 - Technical assessment 2 - 50 candidates passed
4. Stage 4 - Domain knowledge and resume round - 10 candidates passed
5. Stage 5 - Product sense round - 1 candidate passed
1 optimal candidate hired!

This is a greedy process.
