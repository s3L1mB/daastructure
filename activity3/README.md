# Activities

## Task 1/3: Divide-and-conquer

The code in `./src/pow1.cpp` and `./src/pow2.cpp` compute the power `pow(x, n)` using iterative and recursive approaches respectively.

> Refer to the following [link](https://www.techiedelight.com/power-function-implementation-recursive-iterative/).

- What is the time complexity for both approaches?






Running time measures the number of operations it takes to complete a code or program. the keyword here is "operations" and "complete", the time taken for every single operation to complete can be affected by the processor, memory, etc.

With running time, If we have 2 different algorithms solving the same problem, the optimized algorithm might take a longer time to complete than the non-optimized one because of varying factors like ram, the current state of the PC (serving other programs) etc. or even the function for calculating the runtime itself.

For this reason, it is not enough to measure the efficiency of an algorithm based on operations it takes to complete but rather time against input, that way all the external factors are eliminated and that's exactly what time complexity does.

Time complexity is the measurement of an algorithm's time behavior as input size increases.

Time complexity can also be calculated from the logic behind the algorithm/code. On the other hand, running time can be calculated when the code is completed.






## Task 2/3: Divide-and-conquer vs Decrease and conquer

- In many literature, Binary search is referred to use divide-and-conquer technique. Discuss in groups whether you agree or disagree and justify your answers. Refer to the the following thread: [Why Binary Search is not a divide and conquer algorithm?](https://stackoverflow.com/questions/8850447/why-is-binary-search-a-divide-and-conquer-algorithm)





Divide and Conquer algorithm is based on 3 step as follows:

    Divide
    Conquer
    Combine

Binary Search problem can be defined as finding x in the sorted array A[n]. According to this information:

    Divide: compare x with middle
    Conquer: Recurse in one sub array. (Finding x in this array)
    Combine: it is not necessary.



## Task 3/3: Individual, at home

- Refactor the code in `./src/pow2.cpp` to optimize the time complexity of the recursive approach. Use `./src/pow3.cpp` as a starter.
- Refactor the code in `pow1.cpp` and `pow2.cpp`, as follows:
  - Replace `printf()` with` std::cout()`
  - Include the right headers e.g. `iostream`

## Links

- https://www.techiedelight.com/power-function-implementation-recursive-iterative/
- https://cpp.sh/
