# Activities

## Task 1

Refer to the first [link](#links).

- Why is Algorithm Analysis Important?
- Explain the Big $O$ notation
Big-O notation is a way of converting the overall steps of an algorithm into algebraic terms, then excluding lower order constants and coefficients that don’t have that big an impact on the overall complexity of the problem.
- Compare `Linear`, `Logarithmic`, `Quadratic` and `Constant` complexities.

    O(1) — Constant Time: Given an input of size n, it only takes a single step for the algorithm to accomplish the task.
    O(log n) — Logarithmic time: given an input of size n, the number of steps it takes to accomplish the task are decreased by some factor with each step.
    O(n) — Linear Time: Given an input of size n, the number of of steps required is directly related (1 to 1)
    O(n²) — Quadratic Time: Given an input of size n, the number of steps it takes to accomplish a task is square of n.
    O(C^n) — Exponential Time: Given an input of size n, the number of steps it takes to accomplish a task is a constant to the n power (pretty large number).

## Task2

Refer to the first [link](#links).

- Write a simple algorithm in C++ that finds the square of the first item in a list and then prints it on the screen.
- What is the complexity of the algorithm?

## Task 3

Refer to the first [link](#links).

- Write a simple program that displays all items in a list to the console.
- What is the complexity of the algorithm?

## Task 4: : Individual, at home

Refer to this [pdf](./big_o.pdf):

- What is the difference between complexity and performance:
- Does complexity affects performance bor is it the other way around?
- Restate the formal definition of big $O$ in plain English



"performance guarantee" is not a term typically used in analyzing algorithms.

Time complexity is measured in terms of whatever you want. You're stumbled on a dirty secret of CS - Big-O notation is often used rather sloppily without specifying what exactly increases with the input size in that manner. It's generally the number of some primitive operation that's assumed to dominate others in the implementation, and assumed to take constant time itself. Both of these assumptions are often not universally true. For example, for sorting algorithms time complexity is usually based on the number of comparisons. But comparing numbers is actually not a constant time operation itself if the numbers get realy big


## Links

- [Big O Notation and Algorithm Analysis ](https://stackabuse.com/big-o-notation-and-algorithm-analysis-with-python-examples/)
- [Visualization](https://www.cs.usfca.edu/~galles/visualization/Search.html)
- [Big-O notation explained by a self-taught programmer](https://justin.abrah.ms/computer-science/big-o-notation-explained.html)
- [Big-O is easy to calculate, if you know how](https://justin.abrah.ms/computer-science/how-to-calculate-big-o.html)
- https://cpp.sh/
