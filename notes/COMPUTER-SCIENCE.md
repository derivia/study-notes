~ This file was cloned and adapted from the project [coding-interview-university](https://github.com/andreasbm/web-skills/) which is licensed under [coding-interview-university-license](../licenses/coding-interview-university.jwasham)

## Table of Contents
- [Algorithmic complexity and Big-o](#algorithmic-complexity-and-big-o)
- [Data Structures](#data-structures)
    - [Arrays](#arrays)
    - [Linked Lists](#linked-lists)
    - [Stack](#stack)
    - [Queue](#queue)
    - [Hash table](#hash-table)
    - [Binary search](#binary-search)
    - [Bitwise operations](#bitwise-operations)
- [Trees](#trees--intro)
    - [Binary search trees: BSTs](#binary-search-trees-bsts)
    - [Heap / Priority Queue / Binary Heap](#heap--priority-queue--binary-heap)
    - [Balanced search trees](#balanced-search-trees)
- [Sorting](#sorting)
- [Graphs](#graphs)
- [Recursion](#recursion)
- [Dynamic Programming](#dynamic-programming)
- [Design Patterns](#design-patterns)
- [Combinatorics (n choose k) & Probability](#combinatorics-n-choose-k--probability)
- [NP, NP-Complete and Approximation Algorithms](#np-np-complete-and-approximation-algorithms)
- [How computers process a program](#how-computers-process-a-program)
- [Caches](#caches)
- [Processes and Threads](#processes-and-threads)
- [Testing](#testing)
- [String searching & manipulations](#string-searching--manipulations)
- [Tries](#tries)
- [Floating Point Numbers](#floating-point-numbers)
- [Unicode](#unicode)
- [Endianness](#endianness)
- [Networking](#networking)
- [Final Review](#final-review)
- [Additional Books](#additional-books)
- [System Design, Scalability, Data Handling](#system-design-scalability-data-handling) (if you have 4+ years experience)
- [Compilers](#compilers)

## Additional Learning
- [Information theory](#information-theory)
- [Parity & Hamming Code](#parity-hamming-code)
- [Entropy](#entropy)
- [Cryptography](#cryptography)
- [Compression](#compression)
- [Computer Security](#computer-security)
- [Garbage collection](#garbage-collection)
- [Parallel Programming](#parallel-programming)
- [Messaging, Serialization, and Queueing Systems](#messaging-serialization-and-queueing-systems)
- [A](#a)
- [Fast Fourier Transform](#fast-fourier-transform)
- [Bloom Filter](#bloom-filter)
- [HyperLogLog](#hyperloglog)
- [Locality-Sensitive Hashing](#locality-sensitive-hashing)
- [van Emde Boas Trees](#van-emde-boas-trees)
- [Augmented Data Structures](#augmented-data-structures)
- [Balanced search trees](#balanced-search-trees)
- [Skip lists](#skip-lists)
- [Network Flows](#network-flows)
- [Disjoint Sets & Union Find](#disjoint-sets--union-find)
- [Math for Fast Processing](#math-for-fast-processing)
- [Linear Programming](#linear-programming-videos)
- [Geometry, Convex hull](#geometry-convex-hull-videos)
- [Discrete math](#discrete-math)
- [SOLID](#solid)
- [Union-find](#union-find)
- [More Dynamic Programming](#more-dynamic-programming-videos)
- [Advanced Graph Processing](#advanced-graph-processing-videos)
- [MIT Probability](#mit-probability-mathy-and-go-slowly-which-is-good-for-mathy-things-videos)
- [String Matching](#string-matching)
- [More Sorting](#more-sorting)
- [Video Series](#video-series)
- [Computer Science Courses](#computer-science-courses)
- [Papers](#papers)

### Getting the job
- [Update Your Resume](#update-your-resume)
- [Find a Job](#find-a-job)
- [Interview Process & General Interview Prep](#interview-process--general-interview-prep)
- [Be thinking of for when the interview comes](#be-thinking-of-for-when-the-interview-comes)
- [Have questions for the interviewer](#have-questions-for-the-interviewer)
- [Once You've Got The Job](#once-youve-got-the-job)

## Algorithmic complexity and Big-O

- Understand how to express the complexity of an algorithm in terms of Big-O.
- [X] [Harvard CS50 - Asymptotic Notation](https://www.youtube.com/watch?v=iOq5kSKqeR4)
- [X] [Big O Notations (general quick tutorial)](https://www.youtube.com/watch?v=V6mKVRU1evU)
- [-] [Big O Notation (and Omega and Theta) - best mathematical explanation](https://www.youtube.com/watch?v=ei-A_wy5Yxw&index=2&list=PL1BaGV1cIH4UhkL8a9bJGG356covJ76qN)
- [X] [Cheat sheet](http://bigocheatsheet.com/)
- [X] [[Review] Big-O notation in 5 minutes](https://youtu.be/__vX2sjlpXU)

## Data Structures

### Arrays
- [ ] About Arrays:
    - [Arrays CS50 Harvard University](https://www.youtube.com/watch?v=tI_tIZFyKBw&t=3009s)
    - [Arrays](https://www.coursera.org/lecture/data-structures/arrays-OsBSF)
    - [UC Berkeley CS61B - Linear and Multi-Dim Arrays](https://archive.org/details/ucberkeley_webcast_Wp8oiO_CZZE) (Start watching from 15m 32s)
    - [Dynamic Arrays](https://www.coursera.org/lecture/data-structures/dynamic-arrays-EwbnV)
    - [Jagged Arrays](https://www.youtube.com/watch?v=1jtrQqYpt7g)
### Linked Lists
- [ ] Description:
    - [ ] [Linked Lists CS50 Harvard University](https://www.youtube.com/watch?v=2T-A_GFuoTo&t=650s) - this builds the intuition.
    - [ ] [Singly Linked Lists](https://www.coursera.org/lecture/data-structures/singly-linked-lists-kHhgK)
    - [ ] [CS 61B - Linked Lists 1](https://archive.org/details/ucberkeley_webcast_htzJdKoEmO0)
    - [ ] [CS 61B - Linked Lists 2](https://archive.org/details/ucberkeley_webcast_-c4I3gFYe3w)
    - [ ] [[Review] Linked lists in 4 minutes](https://youtu.be/F8AbOfQwl1c)
- [ ] [C Code](https://www.youtube.com/watch?v=QN6FPiD0Gzo)
        - not the whole video, just portions about Node struct and memory allocation
- [ ] Linked List vs Arrays:
    - [Core Linked Lists Vs Arrays](https://www.coursera.org/lecture/data-structures-optimizing-performance/core-linked-lists-vs-arrays-rjBs9)
    - [In The Real World Linked Lists Vs Arrays](https://www.coursera.org/lecture/data-structures-optimizing-performance/in-the-real-world-lists-vs-arrays-QUaUd)
- [ ] [Why you should avoid linked lists](https://www.youtube.com/watch?v=YQs6IC-vgmo)
- [ ] Gotcha: you need pointer to pointer knowledge:
    (for when you pass a pointer to a function that may change the address where that pointer points)
    This page is just to get a grasp on ptr to ptr. I don't recommend this list traversal style. Readability and maintainability suffer due to cleverness.
    - [Pointers to Pointers](https://www.eskimo.com/~scs/cclass/int/sx8.html)
- [ ] Implement (I did with tail pointer & without):
    - [ ] size() - returns the number of data elements in the list
    - [ ] empty() - bool returns true if empty
    - [ ] value_at(index) - returns the value of the nth item (starting at 0 for first)
    - [ ] push_front(value) - adds an item to the front of the list
    - [ ] pop_front() - remove the front item and return its value
    - [ ] push_back(value) - adds an item at the end
    - [ ] pop_back() - removes end item and returns its value
    - [ ] front() - get the value of the front item
    - [ ] back() - get the value of the end item
    - [ ] insert(index, value) - insert value at index, so the current item at that index is pointed to by the new item at the index
    - [ ] erase(index) - removes node at given index
    - [ ] value_n_from_end(n) - returns the value of the node at the nth position from the end of the list
    - [ ] reverse() - reverses the list
    - [ ] remove_value(value) - removes the first item in the list with this value
### Stack
- [ ] [Stacks](https://www.coursera.org/lecture/data-structures/stacks-UdKzQ)
- [ ] [[Review] Stacks in 3 minutes](https://youtu.be/KcT3aVgrrpU)
### Queue
- [ ] [Queue](https://www.coursera.org/lecture/data-structures/queues-EShpq)
- [ ] [Circular buffer/FIFO](https://en.wikipedia.org/wiki/Circular_buffer)
- [ ] [[Review] Queues in 3 minutes](https://youtu.be/D6gu-_tmEpQ)
- [ ] Implement using linked-list, with tail pointer:
    - enqueue(value) - adds value at a position at the tail
    - dequeue() - returns value and removes least recently added element (front)
    - empty()
- [ ] Implement using a fixed-sized array:
    - enqueue(value) - adds item at end of available storage
    - dequeue() - returns value and removes least recently added element
    - empty()
    - full()
- [ ] Cost:
    - a bad implementation using a linked list where you enqueue at the head and dequeue at the tail would be O(n)
        because you'd need the next to last element, causing a full traversal of each dequeue
    - enqueue: O(1) (amortized, linked list and array [probing])
    - dequeue: O(1) (linked list and array)
    - empty: O(1) (linked list and array)
### Hash table
- [ ] Videos:
    - [ ] [Hashing with Chaining](https://www.youtube.com/watch?v=0M_kIqhwbFo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=8)
    - [ ] [Table Doubling, Karp-Rabin](https://www.youtube.com/watch?v=BRO7mVIFt08&index=9&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [[Review] Hash tables in 4 minutes](https://youtu.be/knV86FlSXJ8)

### Binary search
- [X] [Binary Search](https://www.youtube.com/watch?v=D5SrAga1pno)
- [X] [Binary Search](https://www.khanacademy.org/computing/computer-science/algorithms/binary-search/a/binary-search)
- [X] [detail](https://www.topcoder.com/thrive/articles/Binary%20Search)
- [X] [blueprint](https://leetcode.com/discuss/general-discussion/786126/python-powerful-ultimate-binary-search-template-solved-many-problems)
- [X] [[Review] Binary search in 4 minutes](https://youtu.be/fDKIpRe8GW4)
- [X] Implement:
    - binary search (on a sorted array of integers)
    - binary search using recursion
### Bitwise operations
- [X] [Bits cheat sheet](https://github.com/jwasham/coding-interview-university/blob/main/extras/cheat%20sheets/bits-cheat-sheet.pdf)
    - you should know many of the powers of 2 from (2^1 to 2^16 and 2^32)
- [X] Get a really good understanding of manipulating bits with: &, |, ^, ~, >>, <<
    - [X] [words](https://en.wikipedia.org/wiki/Word_%28computer_architecture%29)
    - [X] [Bit Manipulation](https://www.youtube.com/watch?v=7jkIUgLC29I)
    - [X] [C Programming Tutorial 2-10: Bitwise Operators](https://www.youtube.com/watch?v=d0AwjSpNXR0)
    - [X] [Bit Manipulation](https://en.wikipedia.org/wiki/Bit_manipulation)
    - [X] [Bitwise Operation](https://en.wikipedia.org/wiki/Bitwise_operation)
    - [X] [Bithacks](https://graphics.stanford.edu/~seander/bithacks.html)
    - [X] [The Bit Twiddler](https://bits.stephan-brumme.com/)
    - [X] [The Bit Twiddler Interactive](https://bits.stephan-brumme.com/interactive.html)
    - [X] [Bit Hacks](https://www.youtube.com/watch?v=ZusiKXcz_ac)
    - [X] [Practice Operations](https://pconrad.github.io/old_pconrad_cs16/topics/bitOps/)
- [ ] 2s and 1s complement
    - [Binary: Plusses & Minuses (Why We Use Two's Complement)](https://www.youtube.com/watch?v=lKTsv6iVxV4)
    - [1s Complement](https://en.wikipedia.org/wiki/Ones%27_complement)
    - [2s Complement](https://en.wikipedia.org/wiki/Two%27s_complement)
- [ ] Count set bits
    - [4 ways to count bits in a byte](https://youtu.be/Hzuzo9NJrlc)
    - [Count Bits](https://graphics.stanford.edu/~seander/bithacks.html#CountBitsSetKernighan)
    - [How To Count The Number Of Set Bits In a 32 Bit Integer](http://stackoverflow.com/questions/109023/how-to-count-the-number-of-set-bits-in-a-32-bit-integer)
- [X] Swap values:
    - [Swap](https://bits.stephan-brumme.com/swap.html)
- [ ] Absolute value:
    - [Absolute Integer](https://bits.stephan-brumme.com/absInteger.html)

### Trees - Intro
- [ ] [Intro to Trees](https://www.coursera.org/lecture/data-structures/trees-95qda)
- [ ] [Tree Traversal](https://www.coursera.org/lecture/data-structures/tree-traversal-fr51b)
- [ ] [BFS(breadth-first search) and DFS(depth-first search)](https://www.youtube.com/watch?v=uWL6FJhq5fM)
    - BFS notes:
       - level order (BFS, using queue)
       - time complexity: O(n)
       - space complexity: best: O(1), worst: O(n/2) = O(n)
    - DFS notes:
        - time complexity: O(n)
        - space complexity:
            best: O(log n) - avg. height of tree
            worst: O(n)
        - inorder (DFS: left, self, right)
        - postorder (DFS: left, right, self)
        - preorder (DFS: self, left, right)
- [ ] [[Review] Breadth-first search in 4 minutes](https://youtu.be/HZ5YTanv5QE)
- [ ] [[Review] Depth-first search in 4 minutes](https://youtu.be/Urx87-NMm6c)
- [ ] [[Review] Tree Traversal (playlist) in 11 minutes](https://www.youtube.com/playlist?list=PL9xmBV_5YoZO1JC2RgEi04nLy6D-rKk6b)
### Binary search trees: BSTs
- [ ] [Binary Search Tree Review](https://www.youtube.com/watch?v=x6At0nzX92o&index=1&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
- [ ] [Introduction](https://www.coursera.org/learn/data-structures/lecture/E7cXP/introduction)
- [ ] [MIT](https://www.youtube.com/watch?v=76dhtgZt38A&ab_channel=MITOpenCourseWare)
- C/C++:
    - [ ] [Binary search tree - Implementation in C/C++](https://www.youtube.com/watch?v=COZK7NATh4k&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=28)
    - [ ] [BST implementation - memory allocation in stack and heap](https://www.youtube.com/watch?v=hWokyBoo0aI&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=29)
    - [ ] [Find min and max element in a binary search tree](https://www.youtube.com/watch?v=Ut90klNN264&index=30&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
    - [ ] [Find the height of a binary tree](https://www.youtube.com/watch?v=_pnqMz5nrRs&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=31)
    - [ ] [Binary tree traversal - breadth-first and depth-first strategies](https://www.youtube.com/watch?v=9RHO6jU--GU&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=32)
    - [ ] [Binary tree: Level Order Traversal](https://www.youtube.com/watch?v=86g8jAQug04&index=33&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
    - [ ] [Binary tree traversal: Preorder, Inorder, Postorder](https://www.youtube.com/watch?v=gm8DUJJhmY4&index=34&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
    - [ ] [Check if a binary tree is a binary search tree or not](https://www.youtube.com/watch?v=yEwSGhSsT0U&index=35&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
    - [ ] [Delete a node from Binary Search Tree](https://www.youtube.com/watch?v=gcULXE7ViZw&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=36)
    - [ ] [Inorder Successor in a binary search tree](https://www.youtube.com/watch?v=5cPbNCrdotA&index=37&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
- [ ] Implement:
    - [ ] [insert    // insert value into tree](https://leetcode.com/problems/insert-into-a-binary-search-tree/submissions/987660183/)
    - [ ] get_node_count // get count of values stored
    - [ ] print_values // prints the values in the tree, from min to max
    - [ ] delete_tree
    - [ ] is_in_tree // returns true if a given value exists in the tree
    - [ ] [get_height // returns the height in nodes (single node's height is 1)](https://www.geeksforgeeks.org/find-the-maximum-depth-or-height-of-a-tree/)
    - [ ] get_min   // returns the minimum value stored in the tree
    - [ ] get_max   // returns the maximum value stored in the tree
    - [ ] [is_binary_search_tree](https://leetcode.com/problems/validate-binary-search-tree/)
    - [ ] delete_value
    - [ ] get_successor // returns the next-highest value in the tree after given value, -1 if none
### Heap / Priority Queue / Binary Heap
- visualized as a tree, but is usually linear in storage (array, linked list)
- [ ] [Heap](https://en.wikipedia.org/wiki/Heap_(data_structure))
- [ ] [Introduction](https://www.coursera.org/lecture/data-structures/introduction-2OpTs)
- [ ] [Binary Trees](https://www.coursera.org/learn/data-structures/lecture/GRV2q/binary-trees)
- [ ] [Tree Height Remark](https://www.coursera.org/learn/data-structures/supplement/S5xxz/tree-height-remark)
- [ ] [Basic Operations](https://www.coursera.org/learn/data-structures/lecture/0g1dl/basic-operations)
- [ ] [Complete Binary Trees](https://www.coursera.org/learn/data-structures/lecture/gl5Ni/complete-binary-trees)
- [ ] [Pseudocode](https://www.coursera.org/learn/data-structures/lecture/HxQo9/pseudocode)
- [ ] [Heap Sort - jumps to start](https://youtu.be/odNJmw5TOEE?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3291)
- [ ] [Heap Sort](https://www.coursera.org/lecture/data-structures/heap-sort-hSzMO)
- [ ] [Building a heap](https://www.coursera.org/lecture/data-structures/building-a-heap-dwrOS)
- [ ] [MIT: Heaps and Heap Sort](https://www.youtube.com/watch?v=B7hVxCmfPtM&index=4&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
- [ ] [CS 61B Lecture 24: Priority Queues](https://archive.org/details/ucberkeley_webcast_yIUFT6AKBGE)
- [ ] [Linear Time BuildHeap (max-heap)](https://www.youtube.com/watch?v=MiyLo8adrWw)
- [ ] [[Review] Heap (playlist) in 13 minutes](https://www.youtube.com/playlist?list=PL9xmBV_5YoZNsyqgPW-DNwUeT8F8uhWc6)
- [ ] Implement a max-heap:
    - [ ] insert
    - [ ] sift_up - needed for insert
    - [ ] get_max - returns the max item, without removing it
    - [ ] get_size() - return number of elements stored
    - [ ] is_empty() - returns true if the heap contains no elements
    - [ ] extract_max - returns the max item, removing it
    - [ ] sift_down - needed for extract_max
    - [ ] remove(x) - removes item at index x
    - [ ] heapify - create a heap from an array of elements, needed for heap_sort
    - [ ] heap_sort() - take an unsorted array and turn it into a sorted array in place using a max heap or min heap
## Sorting
- [ ] Notes:
    - Implement sorts & know best case/worst case, average complexity of each:
        - no bubble sort - it's terrible - O(n^2), except when n <= 16
    - [ ] Stability in sorting algorithms ("Is Quicksort stable?")
        - [Sorting Algorithm Stability](https://en.wikipedia.org/wiki/Sorting_algorithm#Stability)
        - [Stability In Sorting Algorithms](http://stackoverflow.com/questions/1517793/stability-in-sorting-algorithms)
        - [Stability In Sorting Algorithms](http://www.geeksforgeeks.org/stability-in-sorting-algorithms/)
        - [Sorting Algorithms - Stability](http://homepages.math.uic.edu/~leon/cs-mcs401-s08/handouts/stability.pdf)
    - [ ] Which algorithms can be used on linked lists? Which on arrays? Which of both?
        - I wouldn't recommend sorting a linked list, but merge sort is doable.
        - [Merge Sort For Linked List](http://www.geeksforgeeks.org/merge-sort-for-linked-list/)
- [ ] [Sedgewick - Mergesort](https://www.coursera.org/learn/algorithms-part1/home/week/3)
    - [ ] [1. Mergesort](https://www.coursera.org/lecture/algorithms-part1/mergesort-ARWDq)
    - [ ] [2. Bottom-up Mergesort](https://www.coursera.org/learn/algorithms-part1/lecture/PWNEl/bottom-up-mergesort)
    - [ ] [3. Sorting Complexity](https://www.coursera.org/lecture/algorithms-part1/sorting-complexity-xAltF)
    - [ ] [4. Comparators](https://www.coursera.org/lecture/algorithms-part1/comparators-9FYhS)
    - [ ] [5. Stability](https://www.coursera.org/learn/algorithms-part1/lecture/pvvLZ/stability)
- [ ] [Sedgewick - Quicksort](https://www.coursera.org/learn/algorithms-part1/home/week/3)
    - [ ] [1. Quicksort](https://www.coursera.org/lecture/algorithms-part1/quicksort-vjvnC)
    - [ ] [2. Selection](https://www.coursera.org/lecture/algorithms-part1/selection-UQxFT)
    - [ ] [3. Duplicate Keys](https://www.coursera.org/lecture/algorithms-part1/duplicate-keys-XvjPd)
    - [ ] [4. System Sorts](https://www.coursera.org/lecture/algorithms-part1/system-sorts-QBNZ7)
- [ ] UC Berkeley:
    - [ ] [CS 61B Lecture 29: Sorting I](https://archive.org/details/ucberkeley_webcast_EiUvYS2DT6I)
    - [ ] [CS 61B Lecture 30: Sorting II](https://archive.org/details/ucberkeley_webcast_2hTY3t80Qsk)
    - [ ] [CS 61B Lecture 32: Sorting III](https://archive.org/details/ucberkeley_webcast_Y6LOLpxg6Dc)
    - [ ] [CS 61B Lecture 33: Sorting V](https://archive.org/details/ucberkeley_webcast_qNMQ4ly43p4)
    - [ ] [CS 61B 2014-04-21: Radix Sort](https://archive.org/details/ucberkeley_webcast_pvbBMd-3NoI)
- [ ] [Bubble Sort](https://www.youtube.com/watch?v=P00xJgWzz2c&index=1&list=PL89B61F78B552C1AB)
- [ ] [Analyzing Bubble Sort](https://www.youtube.com/watch?v=ni_zk257Nqo&index=7&list=PL89B61F78B552C1AB)
- [ ] [Insertion Sort, Merge Sort](https://www.youtube.com/watch?v=Kg4bqzAqRBM&index=3&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
- [ ] [Insertion Sort](https://www.youtube.com/watch?v=c4BRHC7kTaQ&index=2&list=PL89B61F78B552C1AB)
- [ ] [Merge Sort](https://www.youtube.com/watch?v=GCae1WNvnZM&index=3&list=PL89B61F78B552C1AB)
- [ ] [Quicksort](https://www.youtube.com/watch?v=y_G9BkAm6B8&index=4&list=PL89B61F78B552C1AB)
- [ ] [Selection Sort](https://www.youtube.com/watch?v=6nDMgr0-Yyo&index=8&list=PL89B61F78B552C1AB)
- [ ] [[Review] Sorting (playlist) in 18 minutes](https://www.youtube.com/playlist?list=PL9xmBV_5YoZOZSbGAXAPIq1BeUf4j20pl)
    - [ ] [Quick sort in 4 minutes](https://youtu.be/Hoixgm4-P4M)
    - [ ] [Heap sort in 4 minutes](https://youtu.be/2DmK_H7IdTo)
    - [ ] [Merge sort in 3 minutes](https://youtu.be/4VqmGXwpLqc)
    - [ ] [Bubble sort in 2 minutes](https://youtu.be/xli_FI7CuzA)
    - [ ] [Selection sort in 3 minutes](https://youtu.be/g-PGLbMth_g)
    - [ ] [Insertion sort in 2 minutes](https://youtu.be/JU767SDMDvA)
- [ ] Implement:
    - [ ] Mergesort: O(n log n) average and worst case
    - [ ] Quicksort O(n log n) average case
    - Selection sort and insertion sort are both O(n^2) average and worst-case
    - For heapsort, see Heap data structure above
- [ ] Not required, but I recommended them:
    - [ ] [Sedgewick - Radix Sorts](https://www.coursera.org/learn/algorithms-part2/home/week/3)
        - [ ] [1. Strings in Java](https://www.coursera.org/learn/algorithms-part2/lecture/vGHvb/strings-in-java)
        - [ ] [2. Key Indexed Counting](https://www.coursera.org/lecture/algorithms-part2/key-indexed-counting-2pi1Z)
        - [ ] [3. Least Significant Digit First String Radix Sort](https://www.coursera.org/learn/algorithms-part2/lecture/c1U7L/lsd-radix-sort)
        - [ ] [4. Most Significant Digit First String Radix Sort](https://www.coursera.org/learn/algorithms-part2/lecture/gFxwG/msd-radix-sort)
        - [ ] [5. 3 Way Radix Quicksort](https://www.coursera.org/lecture/algorithms-part2/3-way-radix-quicksort-crkd5)
        - [ ] [6. Suffix Arrays](https://www.coursera.org/learn/algorithms-part2/lecture/TH18W/suffix-arrays)
    - [ ] [Radix Sort](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#radixSort)
    - [ ] [Radix Sort](https://www.youtube.com/watch?v=xhr26ia4k38)
    - [ ] [Radix Sort, Counting Sort (linear time given constraints)](https://www.youtube.com/watch?v=Nz1KZXbghj8&index=7&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [Randomization: Matrix Multiply, Quicksort, Freivalds' algorithm](https://www.youtube.com/watch?v=cNB2lADK3_s&index=8&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [Sorting in Linear Time](https://www.youtube.com/watch?v=pOKy3RZbSws&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf&index=14)

### Graphs

Graphs can be used to represent many problems in computer science, so this section is long, like trees and sorting.

- Notes:
    - There are 4 basic ways to represent a graph in memory:
        - objects and pointers
        - adjacency matrix
        - adjacency list
        - adjacency map
    - Familiarize yourself with each representation and its pros & cons
    - BFS and DFS - know their computational complexity, their trade-offs, and how to implement them in real code
    - When asked a question, look for a graph-based solution first, then move on if none

- [ ] MIT:
    - [ ] [Breadth-First Search](https://www.youtube.com/watch?v=oFVYVzlvk9c&t=14s&ab_channel=MITOpenCourseWare)
    - [ ] [Depth-First Search](https://www.youtube.com/watch?v=IBfWDYSffUU&t=32s&ab_channel=MITOpenCourseWare)

- [ ] Skiena Lectures - great intro:
    - [ ] [CSE373 2020 - Lecture 10 - Graph Data Structures](https://www.youtube.com/watch?v=Sjk0xqWWPCc&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=10)
    - [ ] [CSE373 2020 - Lecture 11 - Graph Traversal](https://www.youtube.com/watch?v=ZTwjXj81NVY&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=11)
    - [ ] [CSE373 2020 - Lecture 12 - Depth First Search](https://www.youtube.com/watch?v=KyordYB3BOs&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=12)
    - [ ] [CSE373 2020 - Lecture 13 - Minimum Spanning Trees](https://www.youtube.com/watch?v=oolm2VnJUKw&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=13)
    - [ ] [CSE373 2020 - Lecture 14 - Minimum Spanning Trees (con't)](https://www.youtube.com/watch?v=RktgPx0MarY&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=14)
    - [ ] [CSE373 2020 - Lecture 15 - Graph Algorithms (con't 2)](https://www.youtube.com/watch?v=MUe5DXRhyAo&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=15)

- [ ] Graphs (review and more):
    - [ ] [6.006 Single-Source Shortest Paths Problem](https://www.youtube.com/watch?v=Aa2sqUhIn-E&index=15&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [6.006 Dijkstra](https://www.youtube.com/watch?v=NSHizBK9JD8&t=1731s&ab_channel=MITOpenCourseWare)
    - [ ] [6.006 Bellman-Ford](https://www.youtube.com/watch?v=f9cVS_URPc0&ab_channel=MITOpenCourseWare)
    - [ ] [6.006 Speeding Up Dijkstra](https://www.youtube.com/watch?v=CHvQ3q_gJ7E&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=18)
    - [ ] [Aduni: Graph Algorithms I - Topological Sorting, Minimum Spanning Trees, Prim's Algorithm -  Lecture 6]( https://www.youtube.com/watch?v=i_AQT_XfvD8&index=6&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
    - [ ] [Aduni: Graph Algorithms II - DFS, BFS, Kruskal's Algorithm, Union Find Data Structure - Lecture 7]( https://www.youtube.com/watch?v=ufj5_bppBsA&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=7)
    - [ ] [Aduni: Graph Algorithms III: Shortest Path - Lecture 8](https://www.youtube.com/watch?v=DiedsPsMKXc&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=8)
    - [ ] [Aduni: Graph Alg. IV: Intro to geometric algorithms - Lecture 9](https://www.youtube.com/watch?v=XIAQRlNkJAw&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=9)
    - [ ] [CS 61B 2014: Weighted graphs](https://archive.org/details/ucberkeley_webcast_zFbq8vOZ_0k)
    - [ ] [Greedy Algorithms: Minimum Spanning Tree](https://www.youtube.com/watch?v=tKwnms5iRBU&index=16&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [Strongly Connected Components Kosaraju's Algorithm Graph Algorithm](https://www.youtube.com/watch?v=RpgcYiky7uw)
    - [ ] [[Review] Shortest Path Algorithms (playlist) in 16 minutes](https://www.youtube.com/playlist?list=PL9xmBV_5YoZO-Y-H3xIC9DGSfVYJng9Yw)
    - [ ] [[Review] Minimum Spanning Trees (playlist) in 4 minutes](https://www.youtube.com/playlist?list=PL9xmBV_5YoZObEi3Hf6lmyW-CBfs7nkOV)

- Full Coursera Course:
    - [ ] [Algorithms on Graphs](https://www.coursera.org/learn/algorithms-on-graphs/home/welcome)

- I'll implement:
    - [ ] DFS with adjacency list (recursive)
    - [ ] DFS with adjacency list (iterative with stack)
    - [ ] DFS with adjacency matrix (recursive)
    - [ ] DFS with adjacency matrix (iterative with stack)
    - [ ] BFS with adjacency list
    - [ ] BFS with adjacency matrix
    - [ ] single-source shortest path (Dijkstra)
    - [ ] minimum spanning tree
    - DFS-based algorithms (see Aduni videos above):
        - [ ] check for a cycle (needed for topological sort, since we'll check for the cycle before starting)
        - [ ] topological sort
        - [ ] count connected components in a graph
        - [ ] list strongly connected components
        - [ ] check for bipartite graph

### Recursion
- [ ] Stanford lectures on recursion & backtracking:
    - [ ] [Lecture 8 | Programming Abstractions](https://www.youtube.com/watch?v=gl3emqCuueQ&list=PLFE6E58F856038C69&index=8)
    - [ ] [Lecture 9 | Programming Abstractions](https://www.youtube.com/watch?v=uFJhEPrbycQ&list=PLFE6E58F856038C69&index=9)
    - [ ] [Lecture 10 | Programming Abstractions](https://www.youtube.com/watch?v=NdF1QDTRkck&index=10&list=PLFE6E58F856038C69)
    - [ ] [Lecture 11 | Programming Abstractions](https://www.youtube.com/watch?v=p-gpaIGRCQI&list=PLFE6E58F856038C69&index=11)
- When it is appropriate to use it?
- How is tail recursion better than not?
    - [ ] [What Is Tail Recursion Why Is It So Bad?](https://www.quora.com/What-is-tail-recursion-Why-is-it-so-bad)
    - [ ] [Tail Recursion](https://www.coursera.org/lecture/programming-languages/tail-recursion-YZic1)
- [ ] [5 Simple Steps for Solving Any Recursive Problem](https://youtu.be/ngCos392W4w)

### Dynamic Programming
- Each DP soluble problem must be defined as a recursion relation, and coming up with it can be tricky.
- I suggest looking at many examples of DP problems until you have a solid understanding of the pattern involved.
- [ ] Videos:
    - [ ] [Skiena: CSE373 2020 - Lecture 19 - Introduction to Dynamic Programming](https://www.youtube.com/watch?v=wAA0AMfcJHQ&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=18)
    - [ ] [Skiena: CSE373 2020 - Lecture 20 - Edit Distance](https://www.youtube.com/watch?v=T3A4jlHlhtA&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=19)
    - [ ] [Skiena: CSE373 2020 - Lecture 20 - Edit Distance (continued)](https://www.youtube.com/watch?v=iPnPVcZmRbE&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=20)
    - [ ] [Skiena: CSE373 2020 - Lecture 21 - Dynamic Programming](https://www.youtube.com/watch?v=2xPE4Wq8coQ&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=21)
    - [ ] [Skiena: CSE373 2020 - Lecture 22 - Dynamic Programming and Review](https://www.youtube.com/watch?v=Yh3RzqQGsyI&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=22)
    - [ ] [Simonson: Dynamic Programming 0 (starts at 59:18)](https://youtu.be/J5aJEcOr6Eo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3558)
    - [ ] [Simonson: Dynamic Programming I - Lecture 11](https://www.youtube.com/watch?v=0EzHjQ_SOeU&index=11&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
    - [ ] [Simonson: Dynamic programming II - Lecture 12](https://www.youtube.com/watch?v=v1qiRwuJU7g&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=12)
    - [ ] List of individual DP problems (each is short):
        [Dynamic Programming](https://www.youtube.com/playlist?list=PLrmLmBdmIlpsHaNTPP_jHHDx_os9ItYXr)
- [ ] Yale Lecture notes:
    - [ ] [Dynamic Programming](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#dynamicProgramming)
- [ ] Coursera:
    - [ ] [The RNA secondary structure problem](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/80RrW/the-rna-secondary-structure-problem)
    - [ ] [A dynamic programming algorithm](https://www.coursera.org/lecture/algorithmic-thinking-2/a-dynamic-programming-algorithm-PSonq)
    - [ ] [Illustrating the DP algorithm](https://www.coursera.org/lecture/algorithmic-thinking-2/illustrating-the-dp-algorithm-oUEK2)
    - [ ] [Running time of the DP algorithm](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/nfK2r/running-time-of-the-dp-algorithm)
    - [ ] [DP vs. recursive implementation](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/M999a/dp-vs-recursive-implementation)
    - [ ] [Global pairwise sequence alignment](https://www.coursera.org/lecture/algorithmic-thinking-2/global-pairwise-sequence-alignment-UZ7o6)
    - [ ] [Local pairwise sequence alignment](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/WnNau/local-pairwise-sequence-alignment)

### Design patterns
- [ ] [Quick UML review](https://www.youtube.com/watch?v=3cmzqZzwNDM&list=PLGLfVvz_LVvQ5G-LdJ8RLqe-ndo7QITYc&index=3)
- [ ] Learn these patterns:
    - [ ] strategy
    - [ ] singleton
    - [ ] adapter
    - [ ] prototype
    - [ ] decorator
    - [ ] visitor
    - [ ] factory, abstract factory
    - [ ] facade
    - [ ] observer
    - [ ] proxy
    - [ ] delegate
    - [ ] command
    - [ ] state
    - [ ] memento
    - [ ] iterator
    - [ ] composite
    - [ ] flyweight
- [ ] [Series of videos](https://www.youtube.com/playlist?list=PLF206E906175C7E07)
- [ ] [Book: Head First Design Patterns](https://www.amazon.com/Head-First-Design-Patterns-Freeman/dp/0596007124)
- [Handy reference: 101 Design Patterns & Tips for Developers](https://sourcemaking.com/design-patterns-and-tips)

### Combinatorics (n choose k) & Probability
- [ ] [Math Skills: How to find Factorial, Permutation, and Combination (Choose)](https://www.youtube.com/watch?v=8RRo6Ti9d0U)
- [ ] [Make School: Probability](https://www.youtube.com/watch?v=sZkAAk9Wwa4)
- [ ] [Make School: More Probability and Markov Chains](https://www.youtube.com/watch?v=dNaJg-mLobQ)
- [ ] Khan Academy:
    - Course layout:
        - [ ] [Basic Theoretical Probability](https://www.khanacademy.org/math/probability/probability-and-combinatorics-topic)
    - Just the videos - 41 (each are simple and each are short):
        - [ ] [Probability Explained](https://www.youtube.com/watch?v=uzkc-qNVoOk&list=PLC58778F28211FA19)

### NP, NP-Complete and Approximation Algorithms
- Know about the most famous classes of NP-complete problems, such as the traveling salesman and the knapsack problem,
    and be able to recognize them when an interviewer asks you them in disguise.
- Know what NP-complete means.
- [ ] [Computational Complexity](https://www.youtube.com/watch?v=moPtwq_cVH8&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=23)
- [ ] Simonson:
    - [ ] [Greedy Algs. II & Intro to NP-Completeness](https://youtu.be/qcGnJ47Smlo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=2939)
    - [ ] [NP Completeness II & Reductions](https://www.youtube.com/watch?v=e0tGC6ZQdQE&index=16&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
    - [ ] [NP Completeness III](https://www.youtube.com/watch?v=fCX1BGT3wjE&index=17&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
    - [ ] [NP Completeness IV](https://www.youtube.com/watch?v=NKLDp3Rch3M&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=18)
- [ ] Skiena:
    - [ ] [CSE373 2020 - Lecture 23 - NP-Completeness](https://www.youtube.com/watch?v=ItHp5laE1VE&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=23)
    - [ ] [CSE373 2020 - Lecture 24 - Satisfiability](https://www.youtube.com/watch?v=inaFJeCzGxU&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=24)
    - [ ] [CSE373 2020 - Lecture 25 - More NP-Completeness](https://www.youtube.com/watch?v=B-bhKxjZLlc&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=25)
    - [ ] [CSE373 2020 - Lecture 26 - NP-Completeness Challenge](https://www.youtube.com/watch?v=_EzetTkG_Cc&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=26)
- [ ] [Complexity: P, NP, NP-completeness, Reductions](https://www.youtube.com/watch?v=eHZifpgyH_4&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=22)
- [ ] [Complexity: Approximation Algorithms](https://www.youtube.com/watch?v=MEz1J9wY2iM&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=24)
- [ ] [Complexity: Fixed-Parameter Algorithms](https://www.youtube.com/watch?v=4q-jmGrmxKs&index=25&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
- Peter Norvig discusses near-optimal solutions to the traveling salesman problem:
    - [Jupyter Notebook](http://nbviewer.jupyter.org/url/norvig.com/ipython/TSP.ipynb)
- Pages 1048 - 1140 in CLRS if you have it.

### How computers process a program
- [X] [How CPU executes a program](https://www.youtube.com/watch?v=XM4lGflQFvA)
- [X] [How computers calculate - ALU](https://youtu.be/1I5ZMmrOfnA)
- [X] [Registers and RAM](https://youtu.be/fpnE6UAfbtU)
- [X] [The Central Processing Unit (CPU)](https://youtu.be/FZGugFqdr60)
- [X] [Instructions and Programs](https://youtu.be/zltgXvg6r3k)

### @TODO: Caches
- [X] LRU cache:
    - [X] [The Magic of LRU Cache (100 Days of Google Dev)](https://www.youtube.com/watch?v=R5ON3iwx78M)
    - [X] [Implementing LRU](https://www.youtube.com/watch?v=bq6N7Ym81iI)
    - [X] [LeetCode - 146 LRU Cache (C++)](https://www.youtube.com/watch?v=8-FZRAjR7qU)
- [ ] CPU cache:
    - [ ] [MIT 6.004 L15: The Memory Hierarchy](https://www.youtube.com/watch?v=vjYF_fAZI5E&list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-&index=24)
    - [ ] [MIT 6.004 L16: Cache Issues](https://www.youtube.com/watch?v=ajgC3-pyGlk&index=25&list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-)

### @TODO: Processes and Threads
- [ ] Computer Science 162 - Operating Systems:
    - for processes and threads see videos 1-11
    - [Operating Systems and System Programming](https://archive.org/details/ucberkeley-webcast-PL-XXv-cvA_iBDyz-ba4yDskqMDY6A1w_c)
- [What Is The Difference Between A Process And A Thread?](https://www.quora.com/What-is-the-difference-between-a-process-and-a-thread)
- Covers:
    - Processes, Threads, Concurrency issues
        - Difference between processes and threads
        - Processes
        - Threads
        - Locks
        - Mutexes
        - Semaphores
        - Monitors
        - How do they work?
        - Deadlock
        - Livelock
    - CPU activity, interrupts, context switching
    - Modern concurrency constructs with multicore processors
    - [Paging, segmentation, and virtual memory](https://youtu.be/O4nwUqQodAg)
    - [Interrupts](https://youtu.be/iKlAWIKEyuw)
    - Process resource needs (memory: code, static storage, stack, heap, and also file descriptors, i/o)
    - Thread resource needs (shares above (minus stack) with other threads in the same process but each has its own PC, stack counter, registers, and stack)
    - Forking is really copy on write (read-only) until the new process writes to memory, then it does a full copy.
    - Context switching
        - [How context switching is initiated by the operating system and underlying hardware?](https://www.javatpoint.com/what-is-the-context-switching-in-the-operating-system)
- [ ] [threads in C++ (series - 10 videos)](https://www.youtube.com/playlist?list=PL5jc9xFGsL8E12so1wlMS0r0hTQoJL74M)
- [ ] [CS 377 Spring '14: Operating Systems from University of Massachusetts](https://www.youtube.com/playlist?list=PLacuG5pysFbDQU8kKxbUh4K5c1iL5_k7k)
- [ ] concurrency in Python:
    - [ ] [Short series on threads](https://www.youtube.com/playlist?list=PL1H1sBF1VAKVMONJWJkmUh6_p8g4F2oy1)
    - [ ] [Python Threads](https://www.youtube.com/watch?v=Bs7vPNbB9JM)
    - [ ] [Understanding the Python GIL (2010)](https://www.youtube.com/watch?v=Obt-vMVdM8s)
        - [reference](http://www.dabeaz.com/GIL)
    - [ ] [David Beazley - Python Concurrency From the Ground Up LIVE! - PyCon 2015](https://www.youtube.com/watch?v=MCs5OvhV9S4)
    - [ ] [Keynote David Beazley - Topics of Interest (Python Asyncio)](https://www.youtube.com/watch?v=ZzfHjytDceU)
    - [ ] [Mutex in Python](https://www.youtube.com/watch?v=0zaPs8OtyKY)

### @TODO: Testing
- To cover:
    - how unit testing works
    - what are mock objects
    - what is integration testing
    - what is dependency injection
- [ ] [Agile Software Testing with James Bach](https://www.youtube.com/watch?v=SAhJf36_u5U)
- [ ] [Open Lecture by James Bach on Software Testing](https://www.youtube.com/watch?v=ILkT_HV9DVU)
- [ ] [Steve Freeman - Test-Driven Development (that’s not what we meant)](https://vimeo.com/83960706)
    - [slides](http://gotocon.com/dl/goto-berlin-2013/slides/SteveFreeman_TestDrivenDevelopmentThatsNotWhatWeMeant.pdf)
- [ ] Dependency injection:
    - [ ] [video](https://www.youtube.com/watch?v=IKD2-MAkXyQ)
    - [ ] [Tao Of Testing](http://jasonpolites.github.io/tao-of-testing/ch3-1.1.html)
- [ ] [How to write tests](http://jasonpolites.github.io/tao-of-testing/ch4-1.1.html)

### String searching & manipulations
- [ ] [Sedgewick - Suffix Arrays](https://www.coursera.org/learn/algorithms-part2/lecture/TH18W/suffix-arrays)
- [ ] [Sedgewick - Substring Search](https://www.coursera.org/learn/algorithms-part2/home/week/4)
    - [ ] [1. Introduction to Substring Search](https://www.coursera.org/lecture/algorithms-part2/introduction-to-substring-search-n3ZpG)
    - [ ] [2. Brute-Force Substring Search](https://www.coursera.org/learn/algorithms-part2/lecture/2Kn5i/brute-force-substring-search)
    - [ ] [3. Knuth-Morris Pratt](https://www.coursera.org/learn/algorithms-part2/lecture/TAtDr/knuth-morris-pratt)
    - [ ] [4. Boyer-Moore](https://www.coursera.org/learn/algorithms-part2/lecture/CYxOT/boyer-moore)
    - [ ] [5. Rabin-Karp](https://www.coursera.org/lecture/algorithms-part2/rabin-karp-3KiqT)
- [ ] [Search pattern in a text](https://www.coursera.org/learn/data-structures/lecture/tAfHI/search-pattern-in-text)

### Tries
- There are different kinds of tries. Some have prefixes, some don't, and some use strings instead of bits
    to track the path
- I read through the code, but will not implement
- [ ] [Sedgewick - Tries](https://www.coursera.org/learn/algorithms-part2/home/week/4)
    - [ ] [1. R Way Tries](https://www.coursera.org/learn/algorithms-part2/lecture/CPVdr/r-way-tries)
    - [ ] [2. Ternary Search Tries](https://www.coursera.org/learn/algorithms-part2/lecture/yQM8K/ternary-search-tries)
    - [ ] [3. Character Based Operations](https://www.coursera.org/learn/algorithms-part2/lecture/jwNmV/character-based-operations)
- [ ] [Notes on Data Structures and Programming Techniques](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Tries)
- [ ] Short course videos:
    - [ ] [Introduction To Tries](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/08Xyf/core-introduction-to-tries)
    - [ ] [Performance Of Tries](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/PvlZW/core-performance-of-tries)
    - [ ] [Implementing A Trie](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/DFvd3/core-implementing-a-trie)
- [ ] [The Trie: A Neglected Data Structure](https://www.toptal.com/java/the-trie-a-neglected-data-structure)
- [ ] [TopCoder - Using Tries](https://www.topcoder.com/thrive/articles/Using%20Tries)
- [ ] [Stanford Lecture (real-world use case)](https://www.youtube.com/watch?v=TJ8SkcUSdbU)
- [ ] [MIT, Advanced Data Structures, Strings (can get pretty obscure about halfway through)](https://www.youtube.com/watch?v=NinWEPPrkDQ&index=16&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf)

### Floating Point Numbers
- [ ] simple 8-bit: [Representation of Floating Point Numbers - 1 (video - there is an error in calculations - see video description)](https://www.youtube.com/watch?v=ji3SfClm8TU)

### @TODO: Unicode
- [ ] [The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets]( http://www.joelonsoftware.com/articles/Unicode.html)
- [ ] [What Every Programmer Absolutely, Positively Needs To Know About Encodings And Character Sets To Work With Text](http://kunststube.net/encoding/)

### Endianness
- [ ] [Big And Little Endian](https://web.archive.org/web/20180107141940/http://www.cs.umd.edu:80/class/sum2003/cmsc311/Notes/Data/endian.html)
- [ ] [Big Endian Vs Little Endian](https://www.youtube.com/watch?v=JrNF0KRAlyo)
- [ ] [Big And Little Endian Inside/Out](https://www.youtube.com/watch?v=oBSuXP-1Tc0)

### Networking
- [ ] [Khan Academy](https://www.khanacademy.org/computing/code-org/computers-and-the-internet)
- [ ] [UDP and TCP: Comparison of Transport Protocols](https://www.youtube.com/watch?v=Vdc8TCESIg8)
- [ ] [TCP/IP and the OSI Model Explained!](https://www.youtube.com/watch?v=e5DEVa9eSN0)
- [ ] [Packet Transmission across the Internet. Networking & TCP/IP tutorial.](https://www.youtube.com/watch?v=nomyRJehhnM)
- [ ] [HTTP](https://www.youtube.com/watch?v=WGJrLqtX7As)
- [ ] [SSL and HTTPS](https://www.youtube.com/watch?v=S2iBR2ZlZf0)
- [ ] [SSL/TLS](https://www.youtube.com/watch?v=Rp3iZUvXWlM)
- [ ] [HTTP 2.0](https://www.youtube.com/watch?v=E9FxNzv1Tr8)
- [ ] [Video Series](https://www.youtube.com/playlist?list=PLEbnTDJUr_IegfoqO4iPnPYQui46QqT0j)
- [ ] [Subnetting Demystified - Part 5 CIDR Notation](https://www.youtube.com/watch?v=t5xYI0jzOf4)
- [ ] Sockets:
    - [ ] [Java - Sockets - Introduction](https://www.youtube.com/watch?v=6G_W54zuadg&t=6s)
    - [ ] [Socket Programming](https://www.youtube.com/watch?v=G75vN2mnJeQ)

## Final Review

- [ ] Series of 2-3 minutes short subject videos
    - [Videos](https://www.youtube.com/watch?v=r4r1DZcx1cM&list=PLmVb1OknmNJuC5POdcDv5oCS7_OUkDgpj&index=22)
- [ ] Series of 2-5 minutes short subject videos - Michael Sambol:
    - [Videos](https://www.youtube.com/@MichaelSambol)
    - [Code Examples](https://github.com/msambol/dsa)
- [ ] [Sedgewick Videos - Algorithms I](https://www.coursera.org/learn/algorithms-part1)
- [ ] [Sedgewick Videos - Algorithms II](https://www.coursera.org/learn/algorithms-part2)

## Update Your Resume

- See Resume prep information in the books: "Cracking The Coding Interview" and "Programming Interviews Exposed"
- ["This Is What A GOOD Resume Should Look Like"](https://www.careercup.com/resume),
- ["Step-by-step resume guide"](https://www.techinterviewhandbook.org/resume/guide)

## Interview Process & General Interview Prep

- [ ] [How to Pass the Engineering Interview in 2021](https://davidbyttow.medium.com/how-to-pass-the-engineering-interview-in-2021-45f1b389a1)
- [ ] [Demystifying Tech Recruiting](https://www.youtube.com/watch?v=N233T0epWTs)
- [ ] How to Get a Job at the Big 4:
    - [ ] [How to Get a Job at the Big 4 - Amazon, Facebook, Google & Microsoft](https://www.youtube.com/watch?v=YJZCUhxNCv8)
    - [ ] [How to Get a Job at the Big 4.1 (Follow-up video)](https://www.youtube.com/watch?v=6790FVXWBw8&feature=youtu.be)
- [ ] Cracking The Coding Interview Set 1:
    - [ ] [Gayle L McDowell - Cracking The Coding Interview](https://www.youtube.com/watch?v=rEJzOhC5ZtQ)
    - [ ] [Cracking the Coding Interview with Author Gayle Laakmann McDowell](https://www.youtube.com/watch?v=aClxtDcdpsQ)
- [ ] Cracking the Facebook Coding Interview:
    - [ ] [The Approach](https://www.youtube.com/watch?v=wCl9kvQGHPI)
    - [ ] [Problem Walkthrough](https://www.youtube.com/watch?v=4UWDyJq8jZg)
    - [Grokking the Behavioral Interview (Educative free course)](https://www.educative.io/courses/grokking-the-behavioral-interview):
        - Many times, it’s not your technical competency that holds you back from landing your dream job, it’s how you perform on the behavioral interview.
    - [AlgoMonster (paid course with free content)](https://algo.monster/?utm_campaign=jwasham&utm_medium=referral&utm_content=coding-interview-university&utm_source=github):
      - The crash course for LeetCode. Covers all the patterns condensed from thousands of questions.

Mock Interviews:
- [Gainlo.co: Mock interviewers from big companies](http://www.gainlo.co/#!/) - I used this and it helped me relax for the phone screen and on-site interview
- [Pramp: Mock interviews from/with peers](https://www.pramp.com/) - a peer-to-peer model to practice interviews
- [interviewing.io: Practice mock interview with senior engineers](https://interviewing.io) - anonymous algorithmic/systems design interviews with senior engineers from FAANG anonymously
- [Meetapro: Mock interviews with top FAANG interviewers](https://meetapro.com/?utm_source=ciu) - an Airbnb-style mock interview/coaching platform.
- [Hello Interview: Mock Interviews with Expert Coaches and AI](https://www.hellointerview.com/?utm_source=ciu) - interview directly with AI or with FAANG staff engineers and managers.

## Additional Books

- [The Unix Programming Environment](https://www.amazon.com/dp/013937681X)
- [The Linux Command Line: A Complete Introduction](https://www.amazon.com/dp/1593273894/)
- [TCP/IP Illustrated Series](https://en.wikipedia.org/wiki/TCP/IP_Illustrated)
- [Head First Design Patterns](https://www.amazon.com/gp/product/0596007124/)
- [Design Patterns: Elements of Reusable Object-Oriented Software](https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
- [Algorithm Design Manual](http://www.amazon.com/Algorithm-Design-Manual-Steven-Skiena/dp/1849967202) (Skiena)
    - [Solutions](https://web.archive.org/web/20150404194210/http://www.algorithm.cs.sunysb.edu/algowiki/index.php/The_Algorithms_Design_Manual_(Second_Edition))
- [Algorithms](http://jeffe.cs.illinois.edu/teaching/algorithms/) (Jeff Erickson)
- [Write Great Code: Volume 1: Understanding the Machine](https://www.amazon.com/Write-Great-Code-Understanding-Machine/dp/1593270038)
- [Introduction to Algorithms](https://www.amazon.com/Introduction-Algorithms-fourth-Thomas-Cormen/dp/026204630X)
- [Computer Architecture, Sixth Edition: A Quantitative Approach](https://www.amazon.com/dp/0128119055)

## System Design, Scalability, Data Handling

- Scalability
    - Distill large data sets to single values
    - Transform one data set to another
    - Handling obscenely large amounts of data
- System design
    - features sets
    - interfaces
    - class hierarchies
    - designing a system under certain constraints
    - simplicity and robustness
    - tradeoffs
    - performance analysis and optimization
- [ ] [The System Design Primer](https://github.com/donnemartin/system-design-primer)
- [ ] [System Design from HiredInTech](http://www.hiredintech.com/system-design/)
- [ ] [How Do I Prepare To Answer Design Questions In A Technical Interview?](https://www.quora.com/How-do-I-prepare-to-answer-design-questions-in-a-technical-interview?redirected_qid=1500023)
- [ ] [8 steps guide to ace your system design interview](https://javascript.plainenglish.io/8-steps-guide-to-ace-a-system-design-interview-7a5a797f4d7d)
- [ ] [Database Normalization - 1NF, 2NF, 3NF and 4NF](https://www.youtube.com/watch?v=UrYLYV7WSHM)
- [ ] [System Design Interview](https://github.com/checkcheckzz/system-design-interview) - There are a lot of resources in this one. Look through the articles and examples. I put some of them below
- [ ] [How to ace a systems design interview](https://web.archive.org/web/20120716060051/http://www.palantir.com/2011/10/how-to-rock-a-systems-design-interview/)
- [ ] [Numbers Everyone Should Know](http://everythingisdata.wordpress.com/2009/10/17/numbers-everyone-should-know/)
- [ ] [How long does it take to make a context switch?](http://blog.tsunanet.net/2010/11/how-long-does-it-take-to-make-context.html)
- [ ] [Transactions Across Datacenters](https://www.youtube.com/watch?v=srOgpXECblk)
- [ ] [A plain English introduction to CAP Theorem](http://ksat.me/a-plain-english-introduction-to-cap-theorem)
- [ ] [MIT 6.824: Distributed Systems, Spring 2020](https://www.youtube.com/watch?v=cQP8WApzIQQ&list=PLrw6a1wE39_tb2fErI4-WkMbsvGQk9_UB)
- [ ] Consensus Algorithms:
    - [ ] Paxos - [Paxos Agreement - Computerphile](https://www.youtube.com/watch?v=s8JqcZtvnsM)
    - [ ] Raft - [An Introduction to the Raft Distributed Consensus Algorithm](https://www.youtube.com/watch?v=P9Ydif5_qvE)
        - [ ] [Easy-to-read paper](https://raft.github.io/)
        - [ ] [Infographic](http://thesecretlivesofdata.com/raft/)
- [ ] [Consistent Hashing](http://www.tom-e-white.com/2007/11/consistent-hashing.html)
- [ ] [NoSQL Patterns](http://horicky.blogspot.com/2009/11/nosql-patterns.html)
- [ ] Scalability:
    - [ ] [Great overview](https://www.youtube.com/watch?v=-W9F__D3oY4)
    - [ ] [Clones](http://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones)
    - [ ] [Database](http://www.lecloud.net/post/7994751381/scalability-for-dummies-part-2-database)
    - [ ] [Cache](http://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache)
    - [ ] [Asynchronism](http://www.lecloud.net/post/9699762917/scalability-for-dummies-part-4-asynchronism)
    - [ ] [Scalable Web Architecture and Distributed Systems](http://www.aosabook.org/en/distsys.html)
    - [ ] [Fallacies of Distributed Computing Explained](https://pages.cs.wisc.edu/~zuyu/files/fallacies.pdf)
    - [ ] [Jeff Dean - Building Software Systems At Google and Lessons Learned](https://www.youtube.com/watch?v=modXC5IWTJI)
    - [ ] [Introduction to Architecting Systems for Scale](http://lethain.com/introduction-to-architecting-systems-for-scale/)
    - [ ] [Scaling mobile games to a global audience using App Engine and Cloud Datastore](https://www.youtube.com/watch?v=9nWyWwY2Onc)
    - [ ] [How Google Does Planet-Scale Engineering for Planet-Scale Infra](https://www.youtube.com/watch?v=H4vMcD7zKM0)
    - [ ] [The Importance of Algorithms](https://www.topcoder.com/thrive/articles/The%20Importance%20of%20Algorithms)
    - [ ] [Sharding](http://highscalability.com/blog/2009/8/6/an-unorthodox-approach-to-database-design-the-coming-of-the.html)
    - [ ] [Engineering for the Long Game - Astrid Atkinson Keynote](https://www.youtube.com/watch?v=p0jGmgIrf_M&list=PLRXxvay_m8gqVlExPC5DG3TGWJTaBgqSA&index=4)
    - [ ] [7 Years Of YouTube Scalability Lessons In 30 Minutes](http://highscalability.com/blog/2012/3/26/7-years-of-youtube-scalability-lessons-in-30-minutes.html)
        - [video](https://www.youtube.com/watch?v=G-lGCC4KKok)
    - [ ] [How PayPal Scaled To Billions Of Transactions Daily Using Just 8VMs](http://highscalability.com/blog/2016/8/15/how-paypal-scaled-to-billions-of-transactions-daily-using-ju.html)
    - [ ] [How to Remove Duplicates in Large Datasets](https://blog.clevertap.com/how-to-remove-duplicates-in-large-datasets/)
    - [ ] [A look inside Etsy's scale and engineering culture with Jon Cowie](https://www.youtube.com/watch?v=3vV4YiqKm1o)
    - [ ] [What Led Amazon to its Own Microservices Architecture](http://thenewstack.io/led-amazon-microservices-architecture/)
    - [ ] [To Compress Or Not To Compress, That Was Uber's Question](https://eng.uber.com/trip-data-squeeze/)
    - [ ] [When Should Approximate Query Processing Be Used?](http://highscalability.com/blog/2016/2/25/when-should-approximate-query-processing-be-used.html)
    - [ ] [Google's Transition From Single Datacenter To Failover, To A Native Multihomed Architecture]( http://highscalability.com/blog/2016/2/23/googles-transition-from-single-datacenter-to-failover-to-a-n.html)
    - [ ] [The Image Optimization Technology That Serves Millions Of Requests Per Day](http://highscalability.com/blog/2016/6/15/the-image-optimization-technology-that-serves-millions-of-re.html)
    - [ ] [A Patreon Architecture Short](http://highscalability.com/blog/2016/2/1/a-patreon-architecture-short.html)
    - [ ] [Tinder: How Does One Of The Largest Recommendation Engines Decide Who You'll See Next?](http://highscalability.com/blog/2016/1/27/tinder-how-does-one-of-the-largest-recommendation-engines-de.html)
    - [ ] [Design Of A Modern Cache](http://highscalability.com/blog/2016/1/25/design-of-a-modern-cache.html)
    - [ ] [Live Video Streaming At Facebook Scale](http://highscalability.com/blog/2016/1/13/live-video-streaming-at-facebook-scale.html)
    - [ ] [A Beginner's Guide To Scaling To 11 Million+ Users On Amazon's AWS](http://highscalability.com/blog/2016/1/11/a-beginners-guide-to-scaling-to-11-million-users-on-amazons.html)
    - [ ] [A 360 Degree View Of The Entire Netflix Stack](http://highscalability.com/blog/2015/11/9/a-360-degree-view-of-the-entire-netflix-stack.html)
    - [ ] [Latency Is Everywhere And It Costs You Sales - How To Crush It](http://highscalability.com/latency-everywhere-and-it-costs-you-sales-how-crush-it)
    - [ ] [What Powers Instagram: Hundreds of Instances, Dozens of Technologies](http://instagram-engineering.tumblr.com/post/13649370142/what-powers-instagram-hundreds-of-instances)
    - [ ] [Salesforce Architecture - How They Handle 1.3 Billion Transactions A Day](http://highscalability.com/blog/2013/9/23/salesforce-architecture-how-they-handle-13-billion-transacti.html)
    - [ ] [ESPN's Architecture At Scale - Operating At 100,000 Duh Nuh Nuhs Per Second](http://highscalability.com/blog/2013/11/4/espns-architecture-at-scale-operating-at-100000-duh-nuh-nuhs.html)
    - [ ] See "Messaging, Serialization, and Queueing Systems" way below for info on some of the technologies that can glue services together
    - [ ] Twitter:
        - [O'Reilly MySQL CE 2011: Jeremy Cole, "Big and Small Data at @Twitter"](https://www.youtube.com/watch?v=5cKTP36HVgI)
        - [Timelines at Scale](https://www.infoq.com/presentations/Twitter-Timeline-Scalability)
    - For even more, see the "Mining Massive Datasets" video series in the [Video Series](#video-series) section
- [ ] Practicing the system design process: Here are some ideas to try working through on paper, each with some documentation on how it was handled in the real world:
    - review: [The System Design Primer](https://github.com/donnemartin/system-design-primer)
    - [System Design from HiredInTech](http://www.hiredintech.com/system-design/)
    - [cheat sheet](https://github.com/jwasham/coding-interview-university/blob/main/extras/cheat%20sheets/system-design.pdf)
    - flow:
        1. Understand the problem and scope:
            - Define the use cases, with the interviewer's help
            - Suggest additional features
            - Remove items that the interviewer deems out of scope
            - Assume high availability is required, add as a use case
        2. Think about constraints:
            - Ask how many requests per month
            - Ask how many requests per second (they may volunteer it or make you do the math)
            - Estimate reads vs. writes percentage
            - Keep the 80/20 rule in mind when estimating
            - How much data is written per second
            - Total storage required over 5 years
            - How much data read per second
        3. Abstract design:
            - Layers (service, data, caching)
            - Infrastructure: load balancing, messaging
            - Rough overview of any key algorithm that drives the service
            - Consider bottlenecks and determine solutions
    - Exercises:
        - [Design a random unique ID generation system](https://blog.twitter.com/2010/announcing-snowflake)
        - [Design a key-value database](http://www.slideshare.net/dvirsky/introduction-to-redis)
        - [Design a picture sharing system](http://highscalability.com/blog/2011/12/6/instagram-architecture-14-million-users-terabytes-of-photos.html)
        - [Design a recommendation system](http://ijcai13.org/files/tutorial_slides/td3.pdf)
        - [Design a URL-shortener system: copied from above](http://www.hiredintech.com/system-design/the-system-design-process/)
        - [Design a cache system](https://web.archive.org/web/20220217064329/https://adayinthelifeof.nl/2011/02/06/memcache-internals/)

## Additional Learning

### Information theory
- [Khan Academy](https://www.khanacademy.org/computing/computer-science/informationtheory)
- More about Markov processes:
    - [Core Markov Text Generation](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/waxgx/core-markov-text-generation)
    - [Core Implementing Markov Text Generation](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/gZhiC/core-implementing-markov-text-generation)
    - [Project = Markov Text Generation Walk Through](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/EUjrq/project-markov-text-generation-walk-through)
- See more in the MIT 6.050J Information and Entropy

### Parity & Hamming Code
- [Intro](https://www.youtube.com/watch?v=q-3BctoUpHE)
- [Parity](https://www.youtube.com/watch?v=DdMcAUlxh1M)
- Hamming Code:
    - [Error detection](https://www.youtube.com/watch?v=1A_NcXxdoCc)
    - [Error correction](https://www.youtube.com/watch?v=JAMLuxdHH8o)
- [Error Checking](https://www.youtube.com/watch?v=wbH2VxzmoZk)

### Entropy
- [Information Theory, Claude Shannon, Entropy, Redundancy, Data Compression & Bits](https://youtu.be/JnJq3Py0dyM?t=176)

### Cryptography
- [Khan Academy Series](https://www.khanacademy.org/computing/computer-science/cryptography)
- [Cryptography: Hash Functions](https://www.youtube.com/watch?v=KqqOXndnvic&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=30)
- [Cryptography: Encryption](https://www.youtube.com/watch?v=9TNI2wHmaeI&index=31&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

### Compression
- Computerphile:
    - [Compression](https://www.youtube.com/watch?v=Lto-ajuqW3w)
    - [Entropy in Compression](https://www.youtube.com/watch?v=M5c_RFKVkko)
    - [Upside Down Trees (Huffman Trees)](https://www.youtube.com/watch?v=umTbivyJoiI)
    - [EXTRA BITS/TRITS - Huffman Trees](https://www.youtube.com/watch?v=DV8efuB3h2g)
    - [Elegant Compression in Text (The LZ 77 Method)](https://www.youtube.com/watch?v=goOa3DGezUA)
    - [Text Compression Meets Probabilities](https://www.youtube.com/watch?v=cCDCfoHTsaU)
- [Compressor Head videos](https://www.youtube.com/playlist?list=PLOU2XLYxmsIJGErt5rrCqaSGTMyyqNt2H)
- [(optional) Google Developers Live: GZIP is not enough!](https://www.youtube.com/watch?v=whGwm0Lky2s)

### Computer Security
- [MIT](https://www.youtube.com/playlist?list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Introduction, Threat Models](https://www.youtube.com/watch?v=GqmQg-cszw4&index=1&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Control Hijacking Attacks](https://www.youtube.com/watch?v=6bwzNg5qQ0o&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=2)
    - [Buffer Overflow Exploits and Defenses](https://www.youtube.com/watch?v=drQyrzRoRiA&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=3)
    - [Privilege Separation](https://www.youtube.com/watch?v=6SIJmoE9L9g&index=4&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Capabilities](https://www.youtube.com/watch?v=8VqTSY-11F4&index=5&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Sandboxing Native Code](https://www.youtube.com/watch?v=VEV74hwASeU&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=6)
    - [Web Security Model](https://www.youtube.com/watch?v=chkFBigodIw&index=7&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Securing Web Applications](https://www.youtube.com/watch?v=EBQIGy1ROLY&index=8&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Symbolic Execution](https://www.youtube.com/watch?v=yRVZPvHYHzw&index=9&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Network Security](https://www.youtube.com/watch?v=SIEVvk3NVuk&index=11&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Network Protocols](https://www.youtube.com/watch?v=QOtA76ga_fY&index=12&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
    - [Side-Channel Attacks](https://www.youtube.com/watch?v=PuVMkSEcPiI&index=15&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)

### Garbage collection
- [Deep Dive Java: Garbage Collection is Good!](https://www.infoq.com/presentations/garbage-collection-benefits)

### Messaging, Serialization, and Queueing Systems
- [Thrift](https://thrift.apache.org/)
    - [Tutorial](http://thrift-tutorial.readthedocs.io/en/latest/intro.html)
- [Protocol Buffers](https://developers.google.com/protocol-buffers/)
    - [Tutorials](https://developers.google.com/protocol-buffers/docs/tutorials)
- [gRPC](http://www.grpc.io/)
    - [gRPC 101 for Java Developers](https://www.youtube.com/watch?v=5tmPvSe7xXQ&list=PLcTqM9n_dieN0k1nSeN36Z_ppKnvMJoly&index=1)
- [Redis](http://redis.io/)
    - [Tutorial](http://try.redis.io/)
- [Amazon SQS (queue)](https://aws.amazon.com/sqs/)
- [Amazon SNS (pub-sub)](https://aws.amazon.com/sns/)
- [RabbitMQ](https://www.rabbitmq.com/)
    - [Get Started](https://www.rabbitmq.com/getstarted.html)
- [Celery](http://www.celeryproject.org/)
    - [First Steps With Celery](http://docs.celeryproject.org/en/latest/getting-started/first-steps-with-celery.html)
- [ZeroMQ](http://zeromq.org/)
    - [Intro - Read The Manual](http://zeromq.org/intro:read-the-manual)
- [ActiveMQ](http://activemq.apache.org/)
- [Kafka](http://kafka.apache.org/documentation.html#introduction)
- [MessagePack](http://msgpack.org/index.html)
- [Avro](https://avro.apache.org/)

### A*
- [A Search Algorithm](https://en.wikipedia.org/wiki/A*_search_algorithm)
- [A* Pathfinding (E01: algorithm explanation)](https://www.youtube.com/watch?v=-L-WgKMFuhE)

### Fast Fourier Transform
- [An Interactive Guide To The Fourier Transform](https://betterexplained.com/articles/an-interactive-guide-to-the-fourier-transform/)
- [What is a Fourier transform? What is it used for?](http://www.askamathematician.com/2012/09/q-what-is-a-fourier-transform-what-is-it-used-for/)
- [What is the Fourier Transform?](https://www.youtube.com/watch?v=Xxut2PN-V8Q)
- [Divide & Conquer: FFT](https://www.youtube.com/watch?v=iTMn0Kt18tg&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=4)
- [Understanding The FFT](http://jakevdp.github.io/blog/2013/08/28/understanding-the-fft/)

### Bloom Filter
- Given a Bloom filter with m bits and k hashing functions, both insertion and membership testing are O(k)
- [Bloom Filters](https://www.youtube.com/watch?v=-SuTGoFYjZs)
- [Bloom Filters | Mining of Massive Datasets | Stanford University](https://www.youtube.com/watch?v=qBTdukbzc78)
- [Tutorial](http://billmill.org/bloomfilter-tutorial/)
- [How To Write A Bloom Filter App](http://blog.michaelschmatz.com/2016/04/11/how-to-write-a-bloom-filter-cpp/)

### HyperLogLog
- [How To Count A Billion Distinct Objects Using Only 1.5KB Of Memory](http://highscalability.com/blog/2012/4/5/big-data-counting-how-to-count-a-billion-distinct-objects-us.html)

### Locality-Sensitive Hashing
- Used to determine the similarity of documents
- The opposite of MD5 or SHA which are used to determine if 2 documents/strings are exactly the same
- [Simhashing (hopefully) made simple](http://ferd.ca/simhashing-hopefully-made-simple.html)

### van Emde Boas Trees
- [Divide & Conquer: van Emde Boas Trees](https://www.youtube.com/watch?v=hmReJCupbNU&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=6)
- [MIT Lecture Notes](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-046j-design-and-analysis-of-algorithms-spring-2012/lecture-notes/MIT6_046JS12_lec15.pdf)

### Augmented Data Structures
- [CS 61B Lecture 39: Augmenting Data Structures](https://archive.org/details/ucberkeley_webcast_zksIj9O8_jc)

### Balanced search trees
- Know at least one type of balanced binary tree (and know how it's implemented):
- "Among balanced search trees, AVL and 2/3 trees are now passé and red-black trees seem to be more popular.
    A particularly interesting self-organizing data structure is the splay tree, which uses rotations
    to move any accessed key to the root." - Skiena
- Of these, I chose to implement a splay tree. From what I've read, you won't implement a
    balanced search tree in your interview. But I wanted exposure to coding one up
    and let's face it, splay trees are the bee's knees. I did read a lot of red-black tree code
    - Splay tree: insert, search, delete functions
    If you end up implementing a red/black tree try just these:
    - Search and insertion functions, skipping delete
- I want to learn more about B-Tree since it's used so widely with very large data sets
- [Self-balancing binary search tree](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree)
- AVL trees
    - In practice:
        From what I can tell, these aren't used much in practice, but I could see where they would be:
        The AVL tree is another structure supporting O(log n) search, insertion, and removal. It is more rigidly
        balanced than red–black trees, leading to slower insertion and removal but faster retrieval. This makes it
        attractive for data structures that may be built once and loaded without reconstruction, such as language
        dictionaries (or program dictionaries, such as the opcodes of an assembler or interpreter)
    - [MIT AVL Trees / AVL Sort](https://www.youtube.com/watch?v=FNeL18KsWPc&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=6)
    - [AVL Trees](https://www.coursera.org/learn/data-structures/lecture/Qq5E0/avl-trees)
    - [AVL Tree Implementation](https://www.coursera.org/learn/data-structures/lecture/PKEBC/avl-tree-implementation)
    - [Split And Merge](https://www.coursera.org/learn/data-structures/lecture/22BgE/split-and-merge)
    - [[Review] AVL Trees (playlist) in 19 minutes](https://www.youtube.com/playlist?list=PL9xmBV_5YoZOUFgdIeOPuH6cfSnNRMau-)
- Splay trees
    - In practice:
        Splay trees are typically used in the implementation of caches, memory allocators, routers, garbage collectors,
        data compression, ropes (replacement of string used for long text strings), in Windows NT (in the virtual memory,
        networking and file system code) etc
    - [CS 61B: Splay Trees](https://archive.org/details/ucberkeley_webcast_G5QIXywcJlY)
    - MIT Lecture: Splay Trees:
        - Gets very mathy, but watch the last 10 minutes for sure.
        - [Video](https://www.youtube.com/watch?v=QnPl_Y6EqMo)
- Red/black trees
    - These are a translation of a 2-3 tree (see below).
    - In practice:
        Red–black trees offer worst-case guarantees for insertion time, deletion time, and search time.
        Not only does this make them valuable in time-sensitive applications such as real-time applications,
        but it makes them valuable building blocks in other data structures that provide worst-case guarantees;
        for example, many data structures used in computational geometry can be based on red-black trees, and
        the Completely Fair Scheduler used in current Linux kernels uses red–black trees. In version 8 of Java,
        the Collection HashMap has been modified such that instead of using a LinkedList to store identical elements with poor
        hashcodes, a Red-Black tree is used
    - [Aduni - Algorithms - Lecture 4 (link jumps to the starting point)](https://youtu.be/1W3x0f_RmUo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3871)
    - [Aduni - Algorithms - Lecture 5](https://www.youtube.com/watch?v=hm2GHwyKF1o&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=5)
    - [Red-Black Tree](https://en.wikipedia.org/wiki/Red%E2%80%93black_tree)
    - [An Introduction To Binary Search And Red Black Tree](https://www.topcoder.com/thrive/articles/An%20Introduction%20to%20Binary%20Search%20and%20Red-Black%20Trees)
    - [[Review] Red-Black Trees (playlist) in 30 minutes](https://www.youtube.com/playlist?list=PL9xmBV_5YoZNqDI8qfOZgzbqahCUmUEin)
- 2-3 search trees
    - In practice:
        2-3 trees have faster inserts at the expense of slower searches (since height is more compared to AVL trees).
    - You would use 2-3 trees very rarely because its implementation involves different types of nodes. Instead, people use Red-Black trees.
    - [23-Tree Intuition and Definition](https://www.youtube.com/watch?v=C3SsdUqasD4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=2)
    - [Binary View of 23-Tree](https://www.youtube.com/watch?v=iYvBtGKsqSg&index=3&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
    - [2-3 Trees (student recitation)](https://www.youtube.com/watch?v=TOb1tuEZ2X4&index=5&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
- 2-3-4 Trees (aka 2-4 trees)
    - In practice:
        For every 2-4 trees, there are corresponding red–black trees with data elements in the same order. The insertion and deletion
        operations on 2-4 trees are also equivalent to color-flipping and rotations in red–black trees. This makes 2-4 trees an
        important tool for understanding the logic behind red-black trees, and this is why many introductory algorithm texts introduce
        2-4 trees just before red–black trees, even though 2-4 trees are not often used in practice.
    - [CS 61B Lecture 26: Balanced Search Trees](https://archive.org/details/ucberkeley_webcast_zqrqYXkth6Q)
    - [Bottom Up 234-Trees](https://www.youtube.com/watch?v=DQdMYevEyE4&index=4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
    - [Top Down 234-Trees](https://www.youtube.com/watch?v=2679VQ26Fp4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=5)
- N-ary (K-ary, M-ary) trees
    - note: the N or K is the branching factor (max branches)
    - binary trees are a 2-ary tree, with branching factor = 2
    - 2-3 trees are 3-ary
    - [K-Ary Tree](https://en.wikipedia.org/wiki/K-ary_tree)
- B-Trees
    - Fun fact: it's a mystery, but the B could stand for Boeing, Balanced, or Bayer (co-inventor).
    - In Practice:
        B-trees are widely used in databases. Most modern filesystems use B-trees (or Variants). In addition to
        its use in databases, the B-tree is also used in filesystems to allow quick random access to an arbitrary
        block in a particular file. The basic problem is turning the file block address into a disk block
        (or perhaps to a cylinder head sector) address
    - [B-Tree](https://en.wikipedia.org/wiki/B-tree)
    - [B-Tree Datastructure](http://btechsmartclass.com/data_structures/b-trees.html)
    - [Introduction to B-Trees](https://www.youtube.com/watch?v=I22wEC1tTGo&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=6)
    - [B-Tree Definition and Insertion](https://www.youtube.com/watch?v=s3bCdZGrgpA&index=7&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
    - [B-Tree Deletion](https://www.youtube.com/watch?v=svfnVhJOfMc&index=8&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
    - [MIT 6.851 - Memory Hierarchy Models](https://www.youtube.com/watch?v=V3omVLzI0WE&index=7&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf)
            - covers cache-oblivious B-Trees, very interesting data structures
            - the first 37 minutes are very technical, and may be skipped (B is block size, cache line size)
    - [[Review] B-Trees (playlist) in 26 minutes](https://www.youtube.com/playlist?list=PL9xmBV_5YoZNFPPv98DjTdD9X6UI9KMHz)
- k-D Trees
    - Great for finding a number of points in a rectangle or higher-dimensional object
    - A good fit for k-nearest neighbors
    - [kNN K-d tree algorithm](https://www.youtube.com/watch?v=Y4ZgLlDfKDg)
- Treap
    - Combination of a binary search tree and a heap
    - [Treap](https://en.wikipedia.org/wiki/Treap)
    - [Data Structures: Treaps explained](https://www.youtube.com/watch?v=6podLUYinH8)
    - [Applications in set operations](https://www.cs.cmu.edu/~scandal/papers/treaps-spaa98.pdf)

### Skip lists
- "These are somewhat of a cult data structure" - Skiena
- [Randomization: Skip Lists](https://www.youtube.com/watch?v=2g9OSRKJuzM&index=10&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
- [For animations and a little more detail](https://en.wikipedia.org/wiki/Skip_list)

### Network Flows
- [Ford-Fulkerson in 5 minutes — Step by step example](https://www.youtube.com/watch?v=Tl90tNtKvxs)
- [Ford-Fulkerson Algorithm](https://www.youtube.com/watch?v=v1VgJmkEJW0)
- [Network Flows](https://www.youtube.com/watch?v=2vhN4Ice5jI)

### Disjoint Sets & Union Find
- [UCB 61B - Disjoint Sets; Sorting & selection](https://archive.org/details/ucberkeley_webcast_MAEGXTwmUsI)
- [Sedgewick Algorithms - Union-Find](https://www.coursera.org/learn/algorithms-part1/home/week/1)

### Math for Fast Processing
- [Integer Arithmetic, Karatsuba Multiplication](https://www.youtube.com/watch?v=eCaXlAaN2uE&index=11&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
- [The Chinese Remainder Theorem (used in cryptography)](https://www.youtube.com/watch?v=ru7mWZJlRQg)

### Linear Programming
- [Linear Programming](https://www.youtube.com/watch?v=M4K6HYLHREQ)
- [Finding minimum cost](https://www.youtube.com/watch?v=2ACJ9ewUC6U)
- [Finding maximum value](https://www.youtube.com/watch?v=8AA_81xI3ik)
- [Solve Linear Equations with Python - Simplex Algorithm](https://www.youtube.com/watch?v=44pAWI7v5Zk)

### Geometry, Convex hull
- [Graph Alg. IV: Intro to geometric algorithms - Lecture 9](https://youtu.be/XIAQRlNkJAw?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3164)
- [Geometric Algorithms: Graham & Jarvis - Lecture 10](https://www.youtube.com/watch?v=J5aJEcOr6Eo&index=10&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
- [Divide & Conquer: Convex Hull, Median Finding](https://www.youtube.com/watch?v=EzeYI7p9MjU&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=2)

### Discrete math
- [Computer Science 70, 001 - Spring 2015 - Discrete Mathematics and Probability Theory](http://www.infocobuild.com/education/audio-video-courses/computer-science/cs70-spring2015-berkeley.html)
- [Discrete Mathematics by Shai Simonson](https://www.youtube.com/playlist?list=PLWX710qNZo_sNlSWRMVIh6kfTjolNaZ8t)
- [Discrete Mathematics By IIT Ropar NPTEL](https://nptel.ac.in/courses/106/106/106106183/)

### SOLID
- [ ] [Bob Martin SOLID Principles of Object Oriented and Agile Design](https://www.youtube.com/watch?v=TMuno5RZNeE)
- [ ] S - [Single Responsibility Principle](http://www.oodesign.com/single-responsibility-principle.html) | [Single responsibility to each Object](http://www.javacodegeeks.com/2011/11/solid-single-responsibility-principle.html)
    - [more flavor](https://docs.google.com/open?id=0ByOwmqah_nuGNHEtcU5OekdDMkk)
- [ ] O - [Open/Closed Principle](http://www.oodesign.com/open-close-principle.html)  | [On production level Objects are ready for extension but not for modification](https://en.wikipedia.org/wiki/Open/closed_principle)
    - [more flavor](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgN2M5MTkwM2EtNWFkZC00ZTI3LWFjZTUtNTFhZGZiYmUzODc1&hl=en)
- [ ] L - [Liskov Substitution Principle](http://www.oodesign.com/liskov-s-substitution-principle.html) | [Base Class and Derived class follow ‘IS A’ Principle](http://stackoverflow.com/questions/56860/what-is-the-liskov-substitution-principle)
    - [more flavor](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgNzAzZjA5ZmItNjU3NS00MzQ5LTkwYjMtMDJhNDU5ZTM0MTlh&hl=en)
- [ ] I - [Interface segregation principle](http://www.oodesign.com/interface-segregation-principle.html) | Clients should not be forced to implement interfaces they don't use
    - [Interface Segregation Principle in 5 minutes](https://www.youtube.com/watch?v=3CtAfl7aXAQ)
    - [more flavor](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgOTViYjJhYzMtMzYxMC00MzFjLWJjMzYtOGJiMDc5N2JkYmJi&hl=en)
- [ ] D -[Dependency Inversion principle](http://www.oodesign.com/dependency-inversion-principle.html) | Reduce the dependency In composition of objects.
    - [Why Is The Dependency Inversion Principle And Why Is It Important](http://stackoverflow.com/questions/62539/what-is-the-dependency-inversion-principle-and-why-is-it-important)
    - [more flavor](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgMjdlMWIzNGUtZTQ0NC00ZjQ5LTkwYzQtZjRhMDRlNTQ3ZGMz&hl=en)

### Union-Find
- [Overview](https://www.coursera.org/learn/data-structures/lecture/JssSY/overview)
- [Naive Implementation](https://www.coursera.org/learn/data-structures/lecture/EM5D0/naive-implementations)
- [Trees](https://www.coursera.org/learn/data-structures/lecture/Mxu0w/trees)
- [Union By Rank](https://www.coursera.org/learn/data-structures/lecture/qb4c2/union-by-rank)
- [Path Compression](https://www.coursera.org/learn/data-structures/lecture/Q9CVI/path-compression)
- [Analysis Options](https://www.coursera.org/learn/data-structures/lecture/GQQLN/analysis-optional)

### More Dynamic Programming
- [6.006: Dynamic Programming I: Fibonacci, Shortest Paths](https://www.youtube.com/watch?v=r4-cftqTcdI&ab_channel=MITOpenCourseWare)
- [6.006: Dynamic Programming II: Text Justification, Blackjack](https://www.youtube.com/watch?v=KLBCUx1is2c&ab_channel=MITOpenCourseWare)
- [6.006: DP III: Parenthesization, Edit Distance, Knapsack](https://www.youtube.com/watch?v=TDo3r5M1LNo&ab_channel=MITOpenCourseWare)
- [6.006: DP IV: Guitar Fingering, Tetris, Super Mario Bros.](https://www.youtube.com/watch?v=i9OAOk0CUQE&ab_channel=MITOpenCourseWare)
- [6.046: Dynamic Programming & Advanced DP](https://www.youtube.com/watch?v=Tw1k46ywN6E&index=14&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
- [6.046: Dynamic Programming: All-Pairs Shortest Paths](https://www.youtube.com/watch?v=NzgFUwOaoIw&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=15)
- [6.046: Dynamic Programming (student recitation)](https://www.youtube.com/watch?v=krZI60lKPek&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=12)

### Advanced Graph Processing
- [Synchronous Distributed Algorithms: Symmetry-Breaking. Shortest-Paths Spanning Trees](https://www.youtube.com/watch?v=mUBmcbbJNf4&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=27)
- [Asynchronous Distributed Algorithms: Shortest-Paths Spanning Trees](https://www.youtube.com/watch?v=kQ-UQAzcnzA&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=28)

### MIT Probability (mathy, and go slowly, which is good for mathy things):
- [MIT 6.042J - Probability Introduction](https://www.youtube.com/watch?v=SmFwFdESMHI&index=18&list=PLB7540DEDD482705B)
- [MIT 6.042J - Conditional Probability](https://www.youtube.com/watch?v=E6FbvM-FGZ8&index=19&list=PLB7540DEDD482705B)
- [MIT 6.042J - Independence](https://www.youtube.com/watch?v=l1BCv3qqW4A&index=20&list=PLB7540DEDD482705B)
- [MIT 6.042J - Random Variables](https://www.youtube.com/watch?v=MOfhhFaQdjw&list=PLB7540DEDD482705B&index=21)
- [MIT 6.042J - Expectation I](https://www.youtube.com/watch?v=gGlMSe7uEkA&index=22&list=PLB7540DEDD482705B)
- [MIT 6.042J - Expectation II](https://www.youtube.com/watch?v=oI9fMUqgfxY&index=23&list=PLB7540DEDD482705B)
- [MIT 6.042J - Large Deviations](https://www.youtube.com/watch?v=q4mwO2qS2z4&index=24&list=PLB7540DEDD482705B)
- [MIT 6.042J - Random Walks](https://www.youtube.com/watch?v=56iFMY8QW2k&list=PLB7540DEDD482705B&index=25)

### String Matching
- Rabin-Karp:
    - [Rabin Karps Algorithm](https://www.coursera.org/lecture/data-structures/rabin-karps-algorithm-c0Qkw)
    - [Precomputing](https://www.coursera.org/learn/data-structures/lecture/nYrc8/optimization-precomputation)
    - [Optimization: Implementation and Analysis](https://www.coursera.org/learn/data-structures/lecture/h4ZLc/optimization-implementation-and-analysis)
    - [Table Doubling, Karp-Rabin](https://www.youtube.com/watch?v=BRO7mVIFt08&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=9)
    - [Rolling Hashes, Amortized Analysis](https://www.youtube.com/watch?v=w6nuXg0BISo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=32)
- Knuth-Morris-Pratt (KMP):
    - [TThe Knuth-Morris-Pratt (KMP) String Matching Algorithm](https://www.youtube.com/watch?v=5i7oKodCRJo)
- Boyer–Moore string search algorithm
    - [Boyer-Moore String Search Algorithm](https://en.wikipedia.org/wiki/Boyer%E2%80%93Moore_string_search_algorithm)
    - [Advanced String Searching Boyer-Moore-Horspool Algorithms](https://www.youtube.com/watch?v=QDZpzctPf10)
- [Coursera: Algorithms on Strings](https://www.coursera.org/learn/algorithms-on-strings/home/week/1)
    - starts off great, but by the time it gets past KMP it gets more complicated than it needs to be
    - nice explanation of tries
    - can be skipped

### More Sorting
- Stanford lectures on sorting:
    - [Lecture 15 | Programming Abstractions](https://www.youtube.com/watch?v=ENp00xylP7c&index=15&list=PLFE6E58F856038C69)
    - [Lecture 16 | Programming Abstractions](https://www.youtube.com/watch?v=y4M9IVgrVKo&index=16&list=PLFE6E58F856038C69)
- Shai Simonson:
    - [Algorithms - Sorting - Lecture 2](https://www.youtube.com/watch?v=odNJmw5TOEE&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=2)
    - [Algorithms - Sorting II - Lecture 3](https://www.youtube.com/watch?v=hj8YKFTFKEE&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=3)
- Steven Skiena lectures on sorting:
    - [CSE373 2020 - Mergesort/Quicksort](https://www.youtube.com/watch?v=jUf-UQ3a0kg&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=8)
    - [CSE373 2020 - Linear Sorting](https://www.youtube.com/watch?v=0ksyQKmre84&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=9)

## Video Series

- [List of individual Dynamic Programming problems (each is short)](https://www.youtube.com/playlist?list=PLrmLmBdmIlpsHaNTPP_jHHDx_os9ItYXr)
- [x86 Architecture, Assembly, Applications](https://www.youtube.com/playlist?list=PL038BE01D3BAEFDB0)
- [MIT 18.06 Linear Algebra, Spring 2005](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8)
- [Excellent - MIT Calculus Revisited: Single Variable Calculus](https://www.youtube.com/playlist?list=PL3B08AE665AB9002A)
- [Skiena lectures from Algorithm Design Manual - CSE373 2020 - Analysis of Algorithms](https://www.youtube.com/watch?v=22hwcnXIGgk&list=PLOtl7M3yp-DX6ic0HGT0PUX_wiNmkWkXx&index=1)
- [UC Berkeley 61B (Spring 2014): Data Structures](https://archive.org/details/ucberkeley-webcast-PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd)
- [UC Berkeley 61B (Fall 2006): Data Structures](https://archive.org/details/ucberkeley-webcast-PL4BBB74C7D2A1049C)
- [UC Berkeley 61C: Machine Structures](https://archive.org/details/ucberkeley-webcast-PL-XXv-cvA_iCl2-D-FS5mk0jFF6cYSJs_)
- [OOSE: Software Dev Using UML and Java](https://www.youtube.com/playlist?list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)
- [MIT 6.004: Computation Structures](https://www.youtube.com/playlist?list=PLDSlqjcPpoL64CJdF0Qee5oWqGS6we_Yu)
- [Carnegie Mellon - Computer Architecture Lectures](https://www.youtube.com/playlist?list=PL5PHm2jkkXmi5CxxI7b3JCL1TWybTDtKq)
- [MIT 6.006: Intro to Algorithms](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&nohtml5=False)
- [MIT 6.033: Computer System Engineering](https://www.youtube.com/watch?v=zm2VP0kHl1M&list=PL6535748F59DCA484)
- [MIT 6.034 Artificial Intelligence, Fall 2010](https://www.youtube.com/playlist?list=PLUl4u3cNGP63gFHB6xb-kVBiQHYe_4hSi)
- [MIT 6.042J: Mathematics for Computer Science, Fall 2010](https://www.youtube.com/watch?v=L3LMbpZIKhQ&list=PLB7540DEDD482705B)
- [MIT 6.046: Design and Analysis of Algorithms](https://www.youtube.com/watch?v=2P-yW7LQr08&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
- [MIT 6.824: Distributed Systems, Spring 2020](https://www.youtube.com/watch?v=cQP8WApzIQQ&list=PLrw6a1wE39_tb2fErI4-WkMbsvGQk9_UB)
- [MIT 6.851: Advanced Data Structures](https://www.youtube.com/watch?v=T0yzrZL1py0&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf&index=1)
- [MIT 6.854: Advanced Algorithms, Spring 2016](https://www.youtube.com/playlist?list=PL6ogFv-ieghdoGKGg2Bik3Gl1glBTEu8c)
- [Harvard COMPSCI 224: Advanced Algorithms](https://www.youtube.com/playlist?list=PL2SOU6wwxB0uP4rJgf5ayhHWgw7akUWSf)
- [MIT 6.858 Computer Systems Security, Fall 2014](https://www.youtube.com/watch?v=GqmQg-cszw4&index=1&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
- [Stanford: Programming Paradigms](https://www.youtube.com/playlist?list=PL9D558D49CA734A02)
- [Introduction to Cryptography by Christof Paar](https://www.youtube.com/playlist?list=PL6N5qY2nvvJE8X75VkXglSrVhLv1tVcfy)
    - [Course Website along with Slides and Problem Sets](http://www.crypto-textbook.com/)
- [Mining Massive Datasets - Stanford University](https://www.youtube.com/playlist?list=PLLssT5z_DsK9JDLcT8T62VtzwyW9LNepV)
- [Graph Theory by Sarada Herke](https://www.youtube.com/user/DrSaradaHerke/playlists?shelf_id=5&view=50&sort=dd)

## Computer Science Courses

- [Directory of Online CS Courses](https://github.com/open-source-society/computer-science)
- [Directory of CS Courses (many with online lectures)](https://github.com/prakhar1989/awesome-courses)

## Algorithms implementation

- [Multiple Algorithms implementation by Princeton University](https://algs4.cs.princeton.edu/code)

## Papers

- [Love classic papers?](https://www.cs.cmu.edu/~crary/819-f09/)
- [1978: Communicating Sequential Processes](http://spinroot.com/courses/summer/Papers/hoare_1978.pdf)
    - [implemented in Go](https://godoc.org/github.com/thomas11/csp)
- [2003: The Google File System](http://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf)
    - replaced by Colossus in 2012
- [2004: MapReduce: Simplified Data Processing on Large Clusters]( http://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf)
    - mostly replaced by Cloud Dataflow?
- [2006: Bigtable: A Distributed Storage System for Structured Data](https://static.googleusercontent.com/media/research.google.com/en//archive/bigtable-osdi06.pdf)
- [2006: The Chubby Lock Service for Loosely-Coupled Distributed Systems](https://research.google.com/archive/chubby-osdi06.pdf)
- [2007: Dynamo: Amazon’s Highly Available Key-value Store](http://s3.amazonaws.com/AllThingsDistributed/sosp/amazon-dynamo-sosp2007.pdf)
    - The Dynamo paper kicked off the NoSQL revolution
- [2007: What Every Programmer Should Know About Memory (very long, and the author encourages skipping of some sections)](https://www.akkadia.org/drepper/cpumemory.pdf)
- 2012: AddressSanitizer: A Fast Address Sanity Checker:
    - [paper](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/37752.pdf)
    - [video](https://www.usenix.org/conference/atc12/technical-sessions/presentation/serebryany)
- 2013: Spanner: Google’s Globally-Distributed Database:
    - [paper](http://static.googleusercontent.com/media/research.google.com/en//archive/spanner-osdi2012.pdf)
    - [video](https://www.usenix.org/node/170855)
- [2015: Continuous Pipelines at Google](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43790.pdf)
- [2015: High-Availability at Massive Scale: Building Google’s Data Infrastructure for Ads](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44686.pdf)
- [2015: How Developers Search for Code: A Case Study](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43835.pdf)
- More papers: [1,000 papers](https://github.com/0voice/computer_expert_paper)
