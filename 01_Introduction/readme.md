# 01 Python Introduction

In this lesson, you will learn the very basic skills necessary to write python code. At a high level, we will be learning about the following.

1. Accessing the coding environment
2. Working with source control (Github)
3. Python Basic syntax
4. Printing to console

---

## 1. Accessing the coding environment
We will be using two websites during this course that will allow you to write and keep track of your code.
1. github.com
2. gitpod.com

---

<a href="github.com" rel="Github Website">![Github Logo](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTJflRVfd9wk80MKCV4kTq-OoHehNMG8HJNLA&usqp=CAU)</a>

Github is a website that allows you to manage different versions of code that you have written. It does this by creating `branches` of code. Think of it like a tree. Each leaf comes from a branch, and each branch comes from a limb, and each limb comes from the main trunk. Git allows you to "branch" off a specific version of code to do work without changing the trunk's code. Then when things are working as you want them to, you can merge those changes into the trunk so everyone else has access to it. This also makes it easier for people to work on the same code at the same time without breaking things for eachother.

---


<a href="https://gitpod.io" rel="some text">![Gitpod Logo](https://www.gitpod.io/images/media-kit/logo-dark-theme.png)</a>

Gitpod is a way to open your github repositories in a virtualized development environment in your web browser. This allows us to be working in similar environments, without having to install a bunch of things on everyone's computer first. Just Click the link in each readme or assignment, and it will open up the developer workspace and you can begin coding.

A few points to consider.
- While the account is free, you are limited to how many hours per month the environment is running. At the time of writing this, you will have 50 hours per month to use in this course and work on your assignments. This means when you are not using the environment, be sure to shut it down so you don't run out of time.
- The environments autosave your work, however they do not auto-commit or auto-push your work to github. This means that if you are not done with something and your workspace gets deleted, even though the work is saved, you will loose it. So get in the habbit of commiting and pushing your work anytime you have to leave it.

---

## Working with Git
Git manages the versions of your software to allow developers to make changes to their code without affecting other developers, and all the while providing a history of all the changes that have been made. At a basic level, there are a few concepts to understand when working with Git.

- Origins
- Repositories
- Branches
- Changes
- Commits

### Origins
An origin in Git refers to the server that holds the main code of the repository. In the case of this course, our remote origin is Github.

### Repositories
A repository refers to a collection of files that you will be changing. Each repository refers to a project you are working on.

### Branches
Branches refer to a specific version of the code. This is the fundemental principal of Git source control. 

![Branch Flow Diagram](https://wac-cdn.atlassian.com/dam/jcr:34c86360-8dea-4be4-92f7-6597d4d5bfae/02%20Feature%20branches.svg?cdnVersion=695)

When you first open a repository in github it will default to the `main` branch. This is usually reserved for production(or customer ready) code. When you create a branch, it will take all the code that is in main, and freeze it as it was, then allow you to make new changes to it. Once your new code is ready, you can then merge your new code into the `main` branch. It's like the multiverse but for your code!

### Changes
A `change` referes to anything that exists in the current branch, that is different from the last commit. These changes must be "staged" befor they can be commited.

This can either be done through the interface by clicking on the `+` icon next to the file in the Source control manager, or you can run `git add <filename>` in the command line.

You can also reverse the changes by clicking on the back button next to the file in the Source Control manager, or you can run `git checkout <filename>` in the command line.

### Commits
Commits are how versions of the code are tracked. Every time you commit code, a unique identification number is given to the commit called a "commit id". This commit id can be used at anytime to change the code back to what it was when it was commited. To commit code you can either click the "Commit" button on the Source Control manager, or run `git commit -m "your commit message"` in the command line. 

Every commit has a "commit message" that is useful in telling another developer what the changes were in the commit.

Once commits are made, they can be pushed to your origin by selecting the "push" command in the Source Control manager, or by calling `git push` in the command line.


## Python Basic Syntax


### Indentation
Python syntax starts first and formost with indentation. Rather than utilizeing brackets (`{`} and `}`) to organize nesting code, python utilizes tab spaces (or 4 spaces). Everything that is indented belengs inside the command that is not. For example:

```
def itemOne():
    itemTwo = 2
    itemThree = 3

itemFour = 4
```

In this example `itemTwo` and `itemThree` belong to the `itemOne` function. Where `itemFour` belongs to the global program. This is a principle that in software development is called `Scoping`. Where we would say that `itemTwo` and `itemThree` belong to scope of `itemOne`, and `itemFour` exists in the global scope. This means that you can only use `itemTwo` and `itemThree` if you are still inside the `itemOne` function. However because `itemFour` is in the global scope, it can be used anytime in the program after it is defined.

### Line Endings
In python, to end a statement, you simply start a new line. This is different from other programming languages where you would typically end a statment with a `;`
### Colon
A Colon tells python that you are about to indent, and it will throw an error if you do not. You can see in the example above that after I defined a function, I added a `:` to let python know I was about to indent.

### Comments
A comment is a useful tool in programming. It can be a way to give yourself a guidline to follow as you are writting your code, or a way to let yourself or other developers know what the code is doing without having to follow the code itself.

In python there are two ways of writting comments.
- A single line comment using a `#`
```
# this is a comment
```
- A multi-line comment using docstrings 

```
"""
This 
is 
a comment
"""
```
In the case of python, a single comment is ignored by python altogether. However a docstring is just an empty string that does nothing. This means that indentation rules apply to the docstring, but are ignored for a single line comment.

## Printing to Console
One of the first things to learn when writing in any language is how to get information out of your program into a console. In python, this is easily done using by using the `print()` function. This is what we call a built-in function of python and is included in what is refered to as the `standard library`. To print, you would simply call:

```
print('Your Message')
```

## Running Python Code
There are a few ways to run python code
- Command Line
  - Simply type `python <yourFileName>`
- Code Editor
  - Type `command + shift + p` to open the tools prompt
  - Type `Python: Run Python File in Terminal`
  - Click on the option and look at the terminal to see the output