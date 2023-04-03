# Activities

## Task 1

- What are the advantages of the C++ Standard Template Library (STL):
- What are the disadvantages of STL?
- What are the main components of STL?
 
 

The Standard Template Library (STL) is a set of C++ template classes to provide common programming data structures and functions such as lists, stacks, arrays, etc. It is a library of container classes, algorithms, and iterators. It is a generalized library and so, its components are parameterized. Working knowledge of template classes is a prerequisite for working with STL.

The C++ Standard Template Library (STL) is a collection of algorithms, data structures, and other components that can be used to simplify the development of C++ programs. The STL provides a range of containers, such as vectors, lists, and maps, as well as algorithms for searching, sorting and manipulating data.

One of the key benefits of the STL is that it provides a way to write generic, reusable code that can be applied to different data types. This means that you can write an algorithm once, and then use it with different types of data without having to write separate code for each type.

The STL also provides a way to write efficient code. Many of the algorithms and data structures in the STL are implemented using optimized algorithms, which can result in faster execution times compared to custom code.
Some of the key components of the STL include:

    Containers: The STL provides a range of containers, such as vector, list, map, set, and stack, which can be used to store and manipulate data.
    Algorithms: The STL provides a range of algorithms, such as sort, find, and binary_search, which can be used to manipulate data stored in containers.
    Iterators: Iterators are objects that provide a way to traverse the elements of a container. The STL provides a range of iterators, such as forward_iterator, bidirectional_iterator, and random_access_iterator, that can be used with different types of containers.
    Function Objects: Function objects, also known as functors, are objects that can be used as function arguments to algorithms. They provide a way to pass a function to an algorithm, allowing you to customize its behavior.
    Adapters: Adapters are components that modify the behavior of other components in the STL. For example, the reverse_iterator adapter can be used to reverse the order of elements in a container.



> You can refer to the following link: https://www.geeksforgeeks.org/the-c-standard-template-library-stl/

## Task 2

- Refer to `./src/non-manipulative.cpp`
  - Discuss how the program works
  - What are the Non-Manipulating Algorithms used in the program?
- Refer to `./src/manipulative.cpp`
  - Discuss how the program works
  - What are the Manipulating Algorithms used in the program?

> You can refer to the following link: https://www.geeksforgeeks.org/c-magicians-stl-algorithms/

## Task 3

- Refer to the following article. Reflect on the difference between Big Oh and little oh
  https://www.baeldung.com/cs/big-o-vs-little-o-notation

Overview

In this brief tutorial, we’ll learn about how big-O and little-o notations differ. In short, they are both asymptotic notations that specify upper-bounds for functions and running times of algorithms.

However, the difference is that big-O may be asymptotically tight while little-o makes sure that the upper bound isn’t asymptotically tight.

Let’s read on to understand what exactly it means to be asymptotically tight.
2. Mathematical Definition

Big-O and little-o notations have very similar definitions, and their difference lies in how strict they are regarding the upper bound they represent.
2.1. Big-O

For a given function g(n), O(g(n)) is defined as:

O(g(n)) = \{f(n): there exist positive constants c and n_0 such that 0 \le f(n) \le cg(n) for all n \ge n_0\}.

So \pmb{O(g(n))} is a set of functions that are, after \pmb{n_0}, smaller than or equal to \pmb{g(n)}. The function’s behavior before n_0 is unimportant since big-O notation (also little-o notation) analyzes the function for huge numbers. As an example, let’s have a look at the following figure:
ogn

Here, f(n) is only one of the possible functions that belong to O(g(n)). Before n_0, f(n) is not always smaller than or equal to g(n), but after n_0, it never goes above g(n).

The equal sign in the definition represents the concept of asymptotical tightness, meaning that when \pmb{n} gets very large, \pmb{f(n)} and \pmb{g(n)} grow at the same rate. For instance, 3n^3 = O(n^3) satisfies the equal sign, hence it is asymptotically tight, while 3n = O(n^3) is not.

For more explanation on this notation, look at an introduction to the theory of big-O notation.
2.2. Little-o

Little-o notation is used to denote an upper-bound that is not asymptotically tight. It is formally defined as:

o(g(n)) = \{f(n): for any positive constant c, there exists positive constant n_0 such that 0 \le f(n) < cg(n) for all n \ge n_0\}.

Note that in this definition, the set of functions \pmb{f(n)} are strictly smaller than \pmb{cg(n)}, meaning that little-o notation is a stronger upper bound than big-O notation. In other words, the little-o notation does not allow the function f(n) to have the same growth rate as g(n).

Intuitively, this means that as the n approaches infinity, f(n) becomes insignificant compared to g(n). In mathematical terms:

    \[ \lim_{n\to\infty} \frac{f(n)}{g(n)} = 0\]

In addition, the inequality in the definition of little-o should hold for any constant c, whereas for big-O, it is enough to find some c that satisfies the inequality.

If we drew an analogy between asymptotic comparison of f(n) and g(n) and the comparison of real numbers a and b, we would have f(n) = O(g(n)) \approx a \le b while f(n) = o(g(n)) \approx a < b.



## Task 4

Refer to one of the following articles. Reflect on the differences between Big Oh, Big Omega and Theta.

- https://jarednielsen.com/big-o-omega-theta/
- https://www.codeandgadgets.com/big-oh-big-omega-and-theta-definitions/
- https://www.geeksforgeeks.org/difference-between-big-oh-big-omega-and-big-theta/


1. Big oh notation (O): 

It is define as upper bound and upper bound on an algorithm is the most amount of time required ( the worst case performance).
Big oh notation is used to describe asymptotic upper bound. 

Mathematically, if f(n) describes the running time of an algorithm; f(n) is O(g(n)) if there exist positive constant C and n0 such that,

    0 <= f(n) <= Cg(n) for all n >= n0

n = used to give upper bound an a function. 
If a function is O(n), it is automatically O(n-square) as well. 

 

 2. Big Omega notation (Ω) : 

It is define as lower bound and lower bound on an algorithm is the least amount of time required ( the most efficient way possible, in other words best case).
Just like O notation provide an asymptotic upper bound, Ω notation provides asymptotic lower bound. 
 

Let f(n) define running time of an algorithm;
f(n) is said to be Ω(g (n)) if there exists positive constant C and (n0) such that 

    0 <= Cg(n) <= f(n) for all n >= n0

n = used to given lower bound on a function 
If a function is Ω(n-square) it is automatically Ω(n) as well. 

Graphical example for Big Omega (Ω): 


3. Big Theta notation (Θ) : 

It is define as tightest bound and tightest bound is the best of all the worst case times that the algorithm can take.

Let f(n) define running time of an algorithm. 
f(n) is said to be Θ(g(n)) if f(n) is O(g(n)) and f(n) is Ω(g(n)).

    Mathematically, 

    0 <= f(n) <= C1g(n) for n >= n0
    0 <= C2g(n) <= f(n) for n >= n0

    Merging both the equation, we get :  

    0 <= C2g(n) <= f(n) <= C1g(n) for n >= n0

The equation simply means there exist positive constants C1 and C2 such that f(n) is sandwich between C2 g(n) and C1g(n). 



Difference Between Big oh, Big Omega and Big Theta : 
 

Big Oh (O)
It is like (<=) 
rate of growth of an algorithm is less than or equal to a specific value. 
The upper bound of algorithm is represented by Big O notation. Only the above function is bounded by Big O. Asymptotic upper bound is  given by Big O notation.
Big oh (O) – Upper Bound
It is define as upper bound and upper bound on an algorithm is the most amount of time required ( the worst case performance).
Mathematically: Big Oh is 0 <= f(n) <= Cg(n) for all n >= n0



Big Omega (Ω)
It is like (>=) 
rate of growth is greater than or equal to a specified value.
The algorithm’s lower bound is represented by Omega notation. The asymptotic lower bound is given by Omega notation.
Big Omega (Ω) – Lower Bound
It is define as lower bound and lower bound on an algorithm is the least amount of time required ( the most efficient way possible, in other words best case).
Mathematically: Big Omega is 0 <= Cg(n) <= f(n) for all n >= n0


Big Theta (Θ)
It is like (==) 
meaning the rate of growth is equal to a specified value.
The bounding of function from above and below is represented by theta notation. The exact asymptotic behavior is done by this theta notation.
Big Theta (Θ) – Tight Bound
It is define as tightest bound and tightest bound is the best of all the worst case times that the algorithm can take.
Mathematically – Big Theta is 0 <= C2g(n) <= f(n) <= C1g(n) for n >= n0


