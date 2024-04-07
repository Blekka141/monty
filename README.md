# 0x19. C - Stacks, Queues - LIFO, FIFO

## Overview
This project involves the implementation of stack and queue data structures in C, utilizing operations typical to both structures such as push and pop. The project emphasizes understanding and applying the Last In, First Out (LIFO) and First In, First Out (FIFO) principles.

## Learning Objectives
- Understanding and defining what LIFO (Stack) and FIFO (Queue) are.
- Practical applications and operations of stacks and queues.
- Proper usage of global variables within constraints.
- Development and troubleshooting with custom data structures.

## Requirements
- **Environment:** Compiled on Ubuntu 20.04 LTS using gcc with `-Wall -Werror -Wextra -pedantic -std=c89`.
- **Submission:** Each team must maintain a single repository for the project.
- **Compilation:** `gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty`

## Data Structures
For this project, the following data structures are used:
```c
/**
 * struct stack_s - doubly linked list representation of a stack (or queue)
 * @n: integer
 * @prev: points to the previous element of the stack (or queue)
 * @next: points to the next element of the stack (or queue)
 *
 * Description: doubly linked list node structure for stack, queues, LIFO, FIFO
 */
typedef struct stack_s
{
    int n;
    struct stack_s *prev;
    struct stack_s *next;
} stack_t;

/**
 * struct instruction_s - opcode and its function
 * @opcode: the opcode
 * @f: function to handle the opcode
 *
 * Description: opcode and its function for stack, queues, LIFO, FIFO
 */
typedef struct instruction_s
{
    char *opcode;
    void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;
