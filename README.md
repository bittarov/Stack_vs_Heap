Experimental Comparison of Stack vs Heap Memory Allocation in C : 

This report compares memory allocation on the stack versus the heap in C programs. Two programs were written to measure and compare the performance of stack and heap allocation. 

First Code : The main steps are 

allocate_on_stack function:

Declares a 1 million int array on the stack. This allocates memory on the stack.

allocate_on_heap function:

Uses malloc to allocate the same amount of memory (1 million ints) on the heap.

Uses free to deallocate this memory after use to avoid memory leaks.

It uses the gettimeofday function to measure the time taken for each allocation.

It prints the time in microseconds for stack and heap allocation.

In general, stack allocation is faster because it is a relatively simple operation.

Heap allocation requires more complex memory management operations.

But heap provides more flexibility in memory management.

Program 1 Results:

The first program allocated 1 million ints on the stack and heap separately and measured the time taken. The results were:

Stack allocation took 893 microseconds

Heap allocation took 5 microseconds

Based on one measurement, stack allocation appeared slower than heap.

Second program : It does the following

Defines the array size (1 million ints) and number of test iterations (10).

allocate_on_stack() function allocates an array of the given size on the stack.

allocate_on_heap() uses malloc() to allocate memory on heap, and frees it after use.

In main():

Uses a loop to call allocate_on_stack() NUM_ITERATIONS times.

Before and after each call, it uses gettimeofday() to measure time elapsed.

Calculates total time taken and stores it in time_taken_stack.

Repeats same steps to measure time for heap allocation in time_taken_heap.

Calculates the average time for stack and heap by dividing total time by number of iterations.

Compares the averages and prints which one was faster.

Program 2 Results:

The second program repeated the memory allocation multiple times and calculated the average time taken. This gives a more accurate comparison of the average performance.

The results of the second program were:

Heap allocation is faster with an avareg time of 1.200000 Microseconds.

Conclusion:

In summary, by repeating the allocation and measuring average times, the second program provided a better comparison of stack vs heap performance. The heap allocation was faster on average compared to the stack.

This demonstrates that for large allocations, the flexibility of heap management results in better performance than simply allocating on the stack.

