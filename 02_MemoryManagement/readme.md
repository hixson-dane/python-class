# 02 Memory Management

## What is Memory
- RAM = Random Access Memory
- Temporary storage of computer data
  - i.e, once program is shut down, the data is gone
- You can think of memory as a mailroom at a big office building. Every section of memory has an address, and can hold a certain amount of data.

| Address | Data |
| ------- | ---- |
|    1    | 0001 |
|    2    | 0010 |
|    3    | 0011 |
|    4    | 0100 |


## What is Memory used for
- Used for temporarily storing data that the program can use. 
- Used to use data that needs to be accessed multiple times.

## Why use Memory instead of HardDrive Storage
- Memory is faster
- Memory can be thrown away(garbage collected) easier


## Types of Memory
- Heap
  - Manually allocated memory (although python does most the work for us)
  - Slower due to the allocation and de-allocation
- Stack 
  - Automatically added memory
  - Used to keep track of memory for a funtion
  - Automatically cleaned up when a function ends
  - Faster than heap memory as it is controlled by the CPU
- Static
  - Used to define global scope memory
  - Can be used by anything, anywhere in the program

## How to allocate Memory
 
### The `=` operator
In order to allocate memory in python, you need to use the `=` operator. The `=` operator tells python to do 2 things

1. Allocate a new block(address) of memory
2. And take data from the other part of the statement, and save it there.

*Example*
```
name = "Dane"
```
In this example, we have a few things happening.

1. We are using a variable `name`
   1. Variables allow programmers to assign names to the memory address that is alocated so they are easier to remember than the binary value given to them.
   2. In this case, because name was not used before, python is "defining" the new variable for us. Other languages make you tell the compiler that you are defining it. Python just does it for you.
2. A "string" (or collection of charecters) is being stored into the address assigned to the variable `name`

In this example, we are using what is called "literal" data, which means it is raw data being saved directly in memory. However it is also possible to take data from another memory address

```
name = "Dane"
firstname = name
```

In this example, we are defining two variables, `name` and `firstname`. The `name` variable processes the same as the first example. However the `firstname` variable processes a little different.

1. The variable name `firstname` is still allocated and assigned a memory address, just like the first example.
2. However because `name` does not begin with a `"`, python knows that this is a variable, so rather than putting the string "name" in, it looks up the data in the address associated with `name`, then copies that data over to the memory address for `firstname`.