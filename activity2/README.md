# Activities

Many data structures are used in four basic ways, which we refer to as operations. These operations are:

- Read: Reading refers to looking something up at a particular spot within the data structure. With an array, this means looking up a value at a particular index.
- Search: Searching refers to looking for a particular value within a data structure. With an array, this means looking to see if a particular value exists within the array, and if so, at which index.
- Insert: Insertion refers to adding a new value to our data structure. With an array, this means adding a new value to an additional slot within the array.
- Delete: Deletion refers to removing a value from our data structure. With an array, this means removing one of the values from the array.

Measuring the speed of an operation is also known as measuring its time complexity, efficiency, performance interchangeably. They all refer to the number of steps a given operation takes.

> In the following tasks we will analyze the time complexity of arrays and an array-based set. This is a primitive first order analysis. We will use special tools later

> A set is a data structure that does not allow duplicate values to be contained within it e.g. an array-based set is an array with one additional constraint of barring duplicates.

## Task 1: Arrays

Discuss in group whether the following statements are True or false.

- [T ] Reading from an array takes one step.
- [F ] Searching an array of N elements takes up to N steps e.g. for an array of 5 elements, the maximum number of steps is 5. For an array of 500 elements, the maximum number would take is 500.
- [ T] Insertion of an element in an array of length N, takes (N + 1) steps in worst-case scenario.
- [T ] Deletion of an element from an array of length N, takes N steps in worst-case scenario.

## Task 2: Sets

Discuss in group whether the following statements are True or false.

- [ F] Reading from an an array-based set takes one step.
- [T ] Searching an array-based set of N elements takes up to N steps.
- [T ] Insertion of an element in an array-based set of length N, takes (2N + 1) steps steps in worst-case scenario.
- [ T] Deletion of an element from an array-based set of length N, takes N steps in worst-case scenario.

## Taks 3

- Array-based sets are arrays with one additional constraint of barring duplicates. How does this single Rule affect efficiency?

A good algorithm is correct, but a great algorithm is both correct and efficient. The most efficient algorithm is one that takes the least amount of execution time and memory usage possible while still yielding a correct answer.

ref: https://www.khanacademy.org/computing/ap-computer-science-principles/algorithms-101/evaluating-algorithms/a/measuring-an-algorithms-efficiency 

- Should we avoid sets because insertion is slower for sets than regular arrays?

There is no "duplicate elimination" such as comparing to all existing elements. If you insert into hash set, it's really a dictionary of items by hash code. There's no duplicate checking unless there already are items with the same hash code. Given a reasonable (well-distributed) hash function, it's not that bad.
 
 ref: https://stackoverflow.com/questions/6044228/java-collection-insertion-set-vs-list 

## Reference

- A Common-Sense Guide to Data Structures and Algorithms,Jay Wengrow
