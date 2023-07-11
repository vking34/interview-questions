# Middle Java


## Differences between Heap Mem vs Stack Mem?

- Stack Memory:

Stack memory is used for storing local variables and method call information.
Each thread in a Java program has its own stack memory.
Memory allocation and deallocation in stack memory are fast and deterministic.
The size of stack memory is typically fixed and limited.
Stack memory follows the Last-In-First-Out (LIFO) principle.
When a method is invoked, a new stack frame is created and pushed onto the stack, containing method arguments, local variables, and return addresses.
When the method execution completes, the corresponding stack frame is popped off the stack, and the memory is reclaimed.
Heap Memory:

Heap memory is used for dynamic memory allocation and is shared among all threads.
Objects created using the "new" keyword are allocated memory in the heap.
Memory allocation and deallocation in the heap are managed by the garbage collector.
Heap memory is larger than stack memory and not limited to a fixed size.
Objects in the heap can be accessed from multiple methods or threads.
Heap memory follows a more complex allocation and deallocation process compared to stack memory.
The garbage collector periodically identifies and frees up memory occupied by objects that are no longer referenced, ensuring efficient memory usage.


The key differences between stack and heap memory in Java are:
Purpose: Stack memory is used for storing local variables and method call information, while heap memory is used for dynamic memory allocation for objects.
Access: Stack memory is thread-specific and accessed only by the thread that owns it, whereas heap memory is shared among all threads.
Allocation and Deallocation: Stack memory allocation and deallocation are fast and deterministic, whereas heap memory allocation and deallocation are managed by the garbage collector and are relatively slower.
Size: Stack memory is typically limited in size and has a fixed allocation, whereas heap memory is larger and not limited to a fixed size.
Lifetime: Stack memory variables have a short lifetime and are deallocated automatically when they go out of scope, whereas heap memory objects have a longer lifetime and are deallocated by the garbage collector when they are no longer referenced.


