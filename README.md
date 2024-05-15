# push_swap

## Table of Contents
1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Usage](#usage)
    - [push_swap](#push_swap)
    - [checker](#checker)
6. [Operations](#operations)
7. [Algorithm](#algorithm)
8. [Testing](#testing)
9. [Resources](#resources)
10. [Authors](#authors)

## Introduction
**push_swap** is a project from 42 School that involves sorting a stack of integers using a set of predefined operations. The goal is to sort the stack with the minimum number of moves using two stacks and a limited set of operations.

## Project Structure
```
push_swap/
├── Makefile
├── README.md
├── checker.c
├── includes/
│   └── push_swap.h
├── resources/
│   ├── ...
├── utils/
│   ├── ...
├── src/
│   ├── ...
└── libft/
    └── ...
```

## Requirements
- GCC (GNU Compiler Collection)
- Standard C library functions

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/abdurahim-H/Push-Swap.git
    cd push_swap
    ```

2. Compile the project using the provided Makefile:
    ```sh
    make
    ```

## Usage

### push_swap
The `push_swap` program calculates and outputs a series of operations to sort a stack of integers.
```sh
./push_swap [integers...]
```
Example:
```sh
./push_swap 4 67 3 87 23
```

### checker
The `checker` program reads a sequence of operations and checks if they correctly sort the stack.
```sh
./checker [integers...]
```
Example:
```sh
./checker 4 67 3 87 23
```
After running the checker, type the operations (e.g., `sa`, `pb`, etc.) followed by Enter. End with Ctrl-D.

## Operations
The following operations are supported:

- `sa` : Swap the first two elements at the top of stack `a`.
- `sb` : Swap the first two elements at the top of stack `b`.
- `ss` : Perform `sa` and `sb` simultaneously.
- `pa` : Push the top element from stack `b` to stack `a`.
- `pb` : Push the top element from stack `a` to stack `b`.
- `ra` : Rotate all elements in stack `a` upwards.
- `rb` : Rotate all elements in stack `b` upwards.
- `rr` : Perform `ra` and `rb` simultaneously.
- `rra`: Reverse rotate all elements in stack `a` downwards.
- `rrb`: Reverse rotate all elements in stack `b` downwards.
- `rrr`: Perform `rra` and `rrb` simultaneously.

## Algorithm
The sorting algorithm implemented in `push_swap` is designed to minimize the number of operations. Common strategies include:

- **Divide and Conquer**: Using variations of quicksort or mergesort.
- **Greedy Algorithms**: Making the most optimal move at each step.
- **Hybrid Approaches**: Combining multiple strategies for efficiency.

## Testing
To test the project, you can use provided test cases or create your own. For example:
```sh
ARG="4 67 3 87 23"; ./push_swap $ARG | ./checker $ARG
```
This command checks if the output of `push_swap` sorts the given list correctly using `checker`.

## Resources
- [42 School Documentation](https://github.com/JCluzet/42-doc)
- [Sorting Algorithms](https://en.wikipedia.org/wiki/Sorting_algorithm)
- [Stack Data Structure](https://en.wikipedia.org/wiki/Stack_(abstract_data_type))

## Authors
- [Abdurahim](https://github.com/abdurahim-H)
