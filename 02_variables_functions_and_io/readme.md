# 02 Variables, Functions, and Input/Output

In this lesson, you will learn how to work with variables, functions and Input/Output(IO). At the end of this lesson, you should be able to do the following.

1. Introduction to Memory
2. Assigning Variables
3. Reassigning and Using Variables.

## 1. Introduction to Memory

Variables are ways to temporarily store information. You can save data into variables, then reuse that data later in your code.

To fully understand variables, we need to understand how data is used in a computer.

<a href="https://en.wikipedia.org/wiki/Von_Neumann_architecture">![Von Neuman Architecture](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e5/Von_Neumann_Architecture.svg/1024px-Von_Neumann_Architecture.svg.png)</a>

- CPU
    - Also known as processor
    - In charge of doing computations
    - Receives commands from code, and computes results
- Memeory(RAM)
    - Temporary Data Storage
    - Used when a program is running.
- HardDrive(ROM)
    - Permenant storage
    - Used when a program is not running

When a program is run, the following happens:

1. The program binary code is loaded into memory
2. The CPU fetches the commands one by one from memory and executes them

This is important to understand because variables are essentially aliases to addresses in memory. Memory is divided by addresses usually denoted by hexidecimal values that look like this: `0x12DF`. Rather than trying to remember the correct memory address, coding languages use variables that let you name a memory address whatever you want.

## 2 Assigning Variables

To create variables we use what is called the assignment operator which is the `=` symbol. Operators are special symbols that the interpreter recognizes and performs special functions when it sees them.

```
my_boolean_variable = True
my_string_variable = "Some Text"
my_number_variable = 1
```

To understand what is happening above, lets look at what the computer is doing.

1. The interpreter comes across this line and sees the `=` operator
2. The computer receives the instruction to assign a memory address for use. Example `0x12DF`
3. The progrem creates an alias for `my_boolean_variable` and links it to the memory address `0x12DF`
4. The program then adds the value `True` to the memory address `0x12DF`

## 3 Reassigning and Using Variables

To use variables, you simply just type the name of the variable when that data is needed.

```
a = 1
b = 2
c = a + b
```