# Dynamic-Memory-Allocator


This problem is based on the implementation of Doubly Linked Lists, Binary Search Trees and Balanced Binary Search Trees (AVL Trees) in order to create a system to perform Memory Allocation. Memory Allocation in simple terms means the reservation of portions of the Computer memory for execution of processes. Thus, this system will be running on our machines and it will give out memories to the programs as requested by them.
We design a dynamic memory allocation system. In this the system does not exactly know the amount of memory required. And so in this case, it would get requested for memory dynamically.

There are two algorithms that have leveraged to perform the task of fragmentation and defragmentation of memory blocks. They are:

- First Bit: Here the Allocation system will go through all the Free Memory blocks, stored using any Data structure, and first block that is big enough to fulfill the needs of the program will be returned. The process of finding the first such block will finish quickly in general, but there will be an issue regarding the loss of memory.
- Best Bit: Rather than finding the first adequate memory block, the system will go through all the free blocks and will return the smallest block which will be big enough to fulfill the needs of the program. Here as it will need to go through the entire data structure of free blocks so it will be slower. But there will be a minimum loss of memory here, as it is finding the best block possible to be assigned.

Our system will be allocating memory using a variant of First Fit and Best Fit algorithm. These variants will be called First Split Fit and Best Split Fit algorithm. Here during the allocation, these algorithms will split the found free block into two segments; one block of size k (that is requested by the program) and the other block of the remaining size.

## Usage

### Using makefile

`make all`

To compile your .java files

`make clean`

To remove the generated .class files

### Using run.sh

`run.sh {input_file} {output_file}`

Example:
`run.sh test.in res.out`

Both arguments are optional, inputfile is the file containing the test cases and output file is where you want the result to be written into.
In the case any argument is missing, console is used for input or output.

A res_gold.out has been added which can be used to compare your results against the standard results.

### Format of test file

number of test cases

size

number of commands

command1

command2

...

size (next test case)

number of commands

command1

command2

...

One sample test file test.in is attached alongside

`Allocate Size`

`Free Address`

This is the format for commands required