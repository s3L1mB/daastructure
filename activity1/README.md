# Activities

## Task 1

- Refer to the following link. Discuss how bubble sort works:
  https://opendsa-server.cs.vt.edu/embed/bubblesortAV

  Bubble sort is a sorting algorithm that compares two adjacent elements and swaps them until they are in the intended order.

Just like the movement of air bubbles in the water that rise up to the surface, each element of the array move to the end in each iteration. Therefore, it is called a bubble sort.


## Task 2

- Refer to the following link. Your task is to show the behavior for one iteration of the outer for loop of Bubble Sort (Try at least 3 cases).
  https://opendsa-server.cs.vt.edu/ODSA/Exercises/Sorting/BubsortPRO.html

## Task 3

- The following snippet is from `./src/bubble.cpp` lines 16-28. Discuss in groups how the code works:

```cpp

    for (i = 0; i < 10; i++)
    {
        for (j = i + 1; j < 10; j++)
        {
            if (a[j] < a[i])
            {
                temp = a[i];
                a[i] = a[j];
                a[j] = temp;
            }
        }
        pass++;
    }
```

- The following snippet is from `./src/selection.cpp` lines 34-41. Discuss in groups how the code works:

```cpp
    for (j = i + 1; j < 10; j++)
    {
        if (myarray[j] < ele_small)
        {
            ele_small = myarray[j];
            position = j;
        }
    }
```

## Task 4: Individual, at home

- Discuss the complexity analysis of selection sort. Refer to the link below:
  https://www.softwaretestinghelp.com/selection-sort/

## Links

- https://cpp.sh/







Bubble Sort Complexity
Time Complexity
					 
			
Best
					O(n)
			
Worst
					O(n2)
			
Average
					O(n2)
			
Space Complexity
					O(1)
			
Stability
					Yes
			
Complexity in Detail

Bubble Sort compares the adjacent elements.
Cycle
					Number of Comparisons
			
1st
					(n-1)
			
2nd
					(n-2)
			
3rd
					(n-3)
			
.......
					......
			
last
					1
			

Hence, the number of comparisons is

(n-1) + (n-2) + (n-3) +.....+ 1 = n(n-1)/2

nearly equals to n2

Hence, Complexity: O(n2)

Also, if we observe the code, bubble sort requires two loops. Hence, the complexity is n*n = n2
1. Time Complexities

    Worst Case Complexity: O(n2)
    If we want to sort in ascending order and the array is in descending order then the worst case occurs.
    Best Case Complexity: O(n)
    If the array is already sorted, then there is no need for sorting.
    Average Case Complexity: O(n2)
    It occurs when the elements of the array are in jumbled order (neither ascending nor descending).

2. Space Complexity

    Space complexity is O(1) because an extra variable is used for swapping.
    In the optimized bubble sort algorithm, two extra variables are used. Hence, the space complexity will be O(2).
