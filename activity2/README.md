# Activities

## Task 1

- Refer to the following link. Discuss how bubble Insertion works:
  https://opendsa-server.cs.vt.edu/ODSA/AV/Sorting/insertionsortAV.html

Thus, in the insertion sort technique, we start from the second element as we assume that the first element is always sorted. Then from the second element to the last element, we compare each element to all of its previous elements and the put that element in the proper position.

## Task 2

- The following snippet is from `./src/insertion.cpp` lines 12-22. Discuss in groups how the code works:

```cpp
    for (int k = 1; k < 10; k++)
    {
        int temp = myarray[k];
        int j = k - 1;
        while (j >= 0 && temp <= myarray[j])
        {
            myarray[j + 1] = myarray[j];
            j = j - 1;
        }
        myarray[j + 1] = temp;
    }
```
 it has been discussed in the group activity

## Task 3

- Discuss the complexity analysis of insertion sort. Refer to the link below:
  https://www.softwaretestinghelp.com/insertion-sort/


  Insertion sort is a sorting technique which can be viewed in a way which we play cards at hand. The way we insert any card in a deck or remove it, insertion sorts works in a similar way.

Insertion sort algorithm technique is more efficient than the Bubble sort and Selection sort techniques but is less efficient than the other techniques like Quicksort and Merge sort.
## Links

- https://cpp.sh/
