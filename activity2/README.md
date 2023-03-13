# Activities

> The [modulo-calculator](#links) might be handy in these exercises.

## Task 1
Discussed in group activity 

- Refer to the following link. Discuss how open hashing works.
  https://www.cs.usfca.edu/~galles/visualization/OpenHash.html

- Open Hashing Practice. Refer to the following link. Move each record on the left to the appropriate bin on the right.

  https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Hashing/OpenHashPRO.html

- Given the following input (`4322, 1334, 1471, 9679, 1989, 6171, 6173, 4199`) and the hash function `x mod 10`, which of the following statements are true?
- [] `9679, 1989, 4199` hash to the same value
- [] `1471, 6171` hash to the same value
- [] All elements hash to the same value
- [] Each element hashes to a different value

## Task 2
Discussed in group activity 

- Bucket Hashing Practice. Refer to the following [link](https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Hashing/HashBucketPRO.html).
- The keys `12, 18, 13, 2, 3, 23, 5 and 15` are inserted into an initially empty hash table of length `10` using open addressing with hash function `h(k) = k mod 10` and **linear probing**. What is the resultant hash table?

## Task 3:
Discussed in group activity 

- What is the [Birthday Paradox](http://en.wikipedia.org/wiki/Birthday_problem)?
- Why is it generally discussed with hashing?
- In a hash table of 9658 slots, what is the smallest number of records that must be inserted for the probability of a collision to be 61% or more? Use the calculator at this 
[link](https://opendsa-server.cs.vt.edu/ODSA/AV/Hashing/Birthday.html)
- Discuss in groups how the following program works `./src/birthday.cpp`?

## Task 4: Individual (at home)

- Difference between `Separate Chaining` and `Open Addressing` collision handling techniques?

Open Addressing:

Like separate chaining, open addressing is a method for handling collisions. In Open Addressing, all elements are stored in the hash table itself. So at any point, the size of the table must be greater than or equal to the total number of keys (Note that we can increase table size by copying old data if needed). This approach is also known as closed hashing. This entire procedure is based upon probing. We will understand the types of probing ahead:

1. Linear Probing: 

In linear probing, the hash table is searched sequentially that starts from the original location of the hash. If in case the location that we get is already occupied, then we check for the next location. 

    The function used for rehashing is as follows: rehash(key) = (n+1)%table-size. 


Applications of linear probing: 

Linear probing is a collision handling technique used in hashing, where the algorithm looks for the next available slot in the hash table to store the collided key. Some of the applications of linear probing include:

    Symbol tables: Linear probing is commonly used in symbol tables, which are used in compilers and interpreters to store variables and their associated values. Since symbol tables can grow dynamically, linear probing can be used to handle collisions and ensure that variables are stored efficiently.
    Caching: Linear probing can be used in caching systems to store frequently accessed data in memory. When a cache miss occurs, the data can be loaded into the cache using linear probing, and when a collision occurs, the next available slot in the cache can be used to store the data.
    Databases: Linear probing can be used in databases to store records and their associated keys. When a collision occurs, linear probing can be used to find the next available slot to store the record.
    Compiler design: Linear probing can be used in compiler design to implement symbol tables, error recovery mechanisms, and syntax analysis.
    Spell checking: Linear probing can be used in spell-checking software to store the dictionary of words and their associated frequency counts. When a collision occurs, linear probing can be used to store the word in the next available slot.

Overall, linear probing is a simple and efficient method for handling collisions in hash tables, and it can be used in a variety of applications that require efficient storage and retrieval of data.
Challenges in Linear Probing :

    Primary Clustering: One of the problems with linear probing is Primary clustering, many consecutive elements form groups and it starts taking time to find a free slot or to search for an element.  
    Secondary Clustering: Secondary clustering is less severe, two records only have the same collision chain (Probe Sequence) if their initial position is the same.

     Quadratic Probing 

If you observe carefully, then you will understand that the interval between probes will increase proportionally to the hash value. Quadratic probing is a method with the help of which we can solve the problem of clustering that was discussed above.  This method is also known as the mid-square method. In this method, we look for the i2‘th slot in the ith iteration. We always start from the original hash location. If only the location is occupied then we check the other slots.

    let hash(x) be the slot index computed using hash function.  

    If slot hash(x) % S is full, then we try (hash(x) + 1*1) % S
    If (hash(x) + 1*1) % S is also full, then we try (hash(x) + 2*2) % S
    If (hash(x) + 2*2) % S is also full, then we try (hash(x) + 3*3) % S


3. Double Hashing 

The intervals that lie between probes are computed by another hash function. Double hashing is a technique that reduces clustering in an optimized way. In this technique, the increments for the probing sequence are computed by using another hash function. We use another hash function hash2(x) and look for the i*hash2(x) slot in the ith rotation. 

    let hash(x) be the slot index computed using hash function.  

    If slot hash(x) % S is full, then we try (hash(x) + 1*hash2(x)) % S
    If (hash(x) + 1*hash2(x)) % S is also full, then we try (hash(x) + 2*hash2(x)) % S
    If (hash(x) + 2*hash2(x)) % S is also full, then we try (hash(x) + 3*hash2(x)) % S
    …………………………………………..

Open addressing is a collision handling technique used in hashing where, when a collision occurs (i.e., when two or more keys map to the same slot), the algorithm looks for another empty slot in the hash table to store the collided key.

    In linear probing, the algorithm simply looks for the next available slot in the hash table and places the collided key there. If that slot is also occupied, the algorithm continues searching for the next available slot until an empty slot is found. This process is repeated until all collided keys have been stored. Linear probing has the best cache performance but suffers from clustering. One more advantage of Linear probing is easy to compute. 
    In quadratic probing, the algorithm searches for slots in a more spaced-out manner. When a collision occurs, the algorithm looks for the next slot using an equation that involves the original hash value and a quadratic function. If that slot is also occupied, the algorithm increments the value of the quadratic function and tries again. This process is repeated until an empty slot is found. Quadratic probing lies between the two in terms of cache performance and clustering. 
    In double hashing, the algorithm uses a second hash function to determine the next slot to check when a collision occurs. The algorithm calculates a hash value using the original hash function, then uses the second hash function to calculate an offset. The algorithm then checks the slot that is the sum of the original hash value and the offset. If that slot is occupied, the algorithm increments the offset and tries again. This process is repeated until an empty slot is found.  Double hashing has poor cache performance but no clustering. Double hashing requires more computation time as two hash functions need to be computed. 

The choice of collision handling technique can have a significant impact on the performance of a hash table. Linear probing is simple and fast, but it can lead to clustering (i.e., a situation where keys are stored in long contiguous runs) and can degrade performance. Quadratic probing is more spaced out, but it can also lead to clustering and can result in a situation where some slots are never checked. Double hashing is more complex, but it can lead to more even distribution of keys and can provide better performance in some cases.


  https://www.geeksforgeeks.org/open-addressing-collision-handling-technique-in-hashing/

  https://www.geeksforgeeks.org/separate-chaining-collision-handling-technique-in-hashing/


What is Collision? 

Since a hash function gets us a small number for a key which is a big integer or string, there is a possibility that two keys result in the same value. The situation where a newly inserted key maps to an already occupied slot in the hash table is called collision and must be handled using some collision handling technique. 
What are the chances of collisions with the large table? 

Collisions are very likely even if we have a big table to store keys. An important observation is Birthday Paradox. With only 23 persons, the probability that two people have the same birthday is 50%.
How to handle Collisions? 

There are mainly two methods to handle collision: 

    Separate Chaining 
    Open Addressing 

In this article, only separate chaining is discussed. We will be discussing Open addressing in the next post
Separate Chaining:

The idea behind separate chaining is to implement the array as a linked list called a chain. Separate chaining is one of the most popular and commonly used techniques in order to handle collisions.

    The linked list data structure is used to implement this technique. So what happens is, when multiple elements are hashed into the same slot index, then these elements are inserted into a singly-linked list which is known as a chain. 

Here, all those elements that hash into the same slot index are inserted into a linked list. Now, we can use a key K to search in the linked list by just linearly traversing. If the intrinsic key for any entry is equal to K then it means that we have found our entry. If we have reached the end of the linked list and yet we haven’t found our entry then it means that the entry does not exist. Hence, the conclusion is that in separate chaining, if two different elements have the same hash value then we store both the elements in the same linked list one after the other.

Advantages:

    Simple to implement. 
    Hash table never fills up, we can always add more elements to the chain. 
    Less sensitive to the hash function or load factors. 
    It is mostly used when it is unknown how many and how frequently keys may be inserted or deleted. 

Disadvantages: 

    The cache performance of chaining is not good as keys are stored using a linked list. Open addressing provides better cache performance as everything is stored in the same table. 
    Wastage of Space (Some Parts of the hash table are never used) 
    If the chain becomes long, then search time can become O(n) in the worst case
    Uses extra space for links

Performance of Chaining: 

Performance of hashing can be evaluated under the assumption that each key is equally likely to be hashed to any slot of the table (simple uniform hashing).  

    m = Number of slots in hash table
    n = Number of keys to be inserted in hash table

    Load factor α = n/m
    Expected time to search = O(1 + α)
    Expected time to delete = O(1 + α)

    Time to insert = O(1)
    Time complexity of search insert and delete is O(1) if  α is O(1)

- (Bonus) Run the following program and comment on the code `./src/hashtable.cpp`

## Link(s)

- [modulo-calculator](https://www.calculators.org/math/modulo.php)
- [Practice Problems on Hashing](https://www.geeksforgeeks.org/practice-problems-on-hashing/)
