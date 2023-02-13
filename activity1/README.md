# Activities

## Task 1/5

> Refer to the instruction in [GitHub Workflow](../github.md)

- Clone today's repo
- Create a new branch e.g answers
- Create a repository in GitHub
- Change remote to point to your repo

## Task 2/5: Brute force

- What is the maximum number of steps it would take to perform a linear search on an ordered array of size 100,000?
  > Refer to `./src/search-linear.cpp`

  The input array is
5 8 10 13 21 23 25 43 54 75 
Enter the key that is to be searched:
[Done] exited with code=null in 52.799 seconds

## Task 3/5: Decrease-and-Conquer

- What is the maximum number of steps it would take to perform a binary search on an ordered array of size 100,000?

  > Refer to `./src/search-binary.cpp`

  The input array is
21 43 23 54 75 13 5 8 25 10 
Enter the key to be searched : 
[Done] exited with code=null in 104.124 seconds

## Task 4/5: Quiz

32 teams qualified for the 2014 World Cup. If the names of the teams were arranged in sorted order (an array), how many items in the array would binary search have to examine to find the location of a particular team in the array, in the worst case?

- [] At most, 32.
- [] At most, 1.
- [] At most, 6.
- [] At most, 16.

## Task 5/5: Individual, at home

Refactor the code in `./src/task4.cpp` to use recursion

- Refer to the following [link](https://www.techiedelight.com/binary-search/)
- Make sure that you:
  - Replace `printf()` with` std::cout()`
  - Include the right headers e.g. `iostream`

## Links

- https://cpp.sh/
- https://www.techiedelight.com/binary-search/
- https://www.softwaretestinghelp.com/searching-algorithms-in-cpp/
- https://www.khanacademy.org/computing/computer-science/algorithms/binary-search/e/running-time-of-binary-search
