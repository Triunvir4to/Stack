# Stack Implementation in C

This repository contains a simple yet comprehensive implementation of a stack data structure in C, using a linked list as its underlying storage mechanism.

## Overview

The stack is a fundamental data structure in computer science, characterized by its Last In, First Out (LIFO) property. This implementation provides a straightforward example of how a stack can be implemented and manipulated through various operations such as push, pop, and peek, among others.

## Features

- **Dynamic Memory Allocation:** The stack grows and shrinks as elements are pushed and popped, thanks to dynamic memory management.
- **Linked List Underlying Structure:** Utilizes a custom linked list implementation to store stack elements, ensuring efficient use of memory and runtime.
- **Stack Operations:** Includes essential stack operations such as push, pop, top (peek), and checking if the stack is empty.
- **Additional Utilities:** Features utilities for stack concatenation, copying, and destruction to manage and manipulate multiple stacks effectively.

## Usage

### Structure Definition

The `Stack` structure is defined as follows:

```c
typedef struct stack {
    int n;              // Size of the stack
    LinkedList *list;   // Pointer to the underlying linked list
} Stack;
```

### Core Functions

- `Stack *newStack()`: Creates and returns a new, empty stack.
- `void stackPush(Stack *stack, int v)`: Pushes a new element onto the stack.
- `int stackPop(Stack *stack)`: Pops the top element from the stack and returns its value.
- `bool stackEmpty(Stack *stack)`: Checks if the stack is empty.
- `Stack *stackConcat(Stack *stack1, Stack *stack2)`: Concatenates two stacks into one.
- `Stack *stackCopy(Stack *stack)`: Creates a copy of the given stack.
- `int stackTop(Stack *stack)`: Retrieves the top element of the stack without removing it.
- `void stackDestroy(Stack *stack)`: Destroys the stack and releases all allocated memory.

### Exception Handling

- The `stackPop` and `stackTop` functions throw an exception if called on an empty stack. Ensure to handle or avoid such situations by checking `stackEmpty` before calling these functions.

## Compilation and Running with CMake

This project uses CMake for easy compilation and building. Follow these steps to compile and run the stack implementation:

1. **Create a Build Directory:** From the root of your project directory, create a new directory to hold the build output. This keeps the build files separate from your source files.
   ```bash
   mkdir build && cd build
   ```
2. **Generate Build System:** Use the cmake to compile the project
  ```bash
  cmake ..
  ```
3. **Build the Project:** Use the generated build system to compile the project.
    ```bash
    make
    ```
4. **Run the Project:** Run the executable
   ```bash
    ./Stack
    ```

## License

This stack implementation is open-source and freely available for personal and educational use. For more details, see the LICENSE file in the repository.

## Contributions

Contributions to improve this implementation or fix issues are welcome. Please feel free to submit pull requests or open issues for discussion.
