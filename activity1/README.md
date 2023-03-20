# Activities

## Task 1
Discussed in group activity 
- Refer to the following link. Discuss how the
  Recursive Factorial works:
  https://www.cs.usfca.edu/~galles/visualization/RecFact.html
- Refer to the following link. Discuss how the Recursive Fibonacci works:
  https://www.cs.usfca.edu/~galles/visualization/DPFib.html

## Task 2
Discussed in group activity 
There are `n` stairs, a person standing at the bottom wants to reach the top. The person can climb either 1 stair or 2 stairs at a time. There is a simple implementations in `./src/` folder. Discuss how the code works.

## Task 3
Discussed in group activity 
- There are `n` stairs, a person standing at the bottom wants to reach the top. The person can climb either 1 stair or 2 stairs or **3 stairs** at a time. Write a program that counts the number of ways, the person can reach the top. You can use the following program as a starter `./src/staircase1.cpp`. Also the link below might useful:
  https://www.includehelp.com/cpp-programs/stair-case-program-to-solve-the-staircase-problem.aspx

## Task 4: Individual (at home)

- What are the pros/cons of recursive over iterative Programming?
- Difference between recursion and induction.


Recursion and induction belong to the branch of Mathematics, these terms are used interchangeably. But there are some differences between these terms. 

Recursion is a process in which a function gets repeated again and again until some base function is satisfied. It repeats and uses its previous values to form a sequence. The procedure applies a certain relation to the given function again and again until some base condition is met.

Induction is the branch of mathematics that is used to prove a result, or a formula, or a statement, or a theorem. It is used to establish the validity of a theorem or result. It has two working rules:

1 Base Step: It helps us to prove that the given statement is true for some initial value. 

2 Inductive Step: It states that if the theorem is true for the nth term, then the statement is true for (n+1)th term. 

Pros/Cons Of Recursion Over Iterative Programming

Recursive programs provide compact and clean code. A recursive program is a simple way of writing programs. There are some inherent problems like factorial, Fibonacci sequence, towers of Hanoi, tree traversals, etc. which require recursion for solving.

In other words, they are solved efficiently with recursion. They can also be solved with iterative programming using stacks or other data structures but there are chances to become more complex to implement.

Problem-solving powers of recursive as well as iterative programming are the same. However, recursive programs take more memory space as all the function calls need to be stored on the stack until the base case is matched.

Recursive functions also have a time overhead because of too many function calls and return values.


> Refer to the [links](#links) section below.

## Links

- https://cpp.sh/
- [Difference Between Recursion and Induction](https://www.geeksforgeeks.org/difference-between-recursion-and-induction/)
- [Recursion vs Iterative Programming](https://www.softwaretestinghelp.com/recursion-in-cpp/)
