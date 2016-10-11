---
layout: page
title: "HW3 Solns: CMPT231"
subtitle: "Lecture 3, ch5-6"
ext-js: "https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=AM_CHTML"
---

### HW3 Solutions (20pts)

+ (1) *(3pts)* Locations for **smallest** element in a **max heap**? Why? 

  To satisfy the max-heap property, the smallest element cannot have any
  children.  So it must be one of the leaves.  In a binary heap, the leaves
  are in the last half of the array.

+ (2) *(4pts)* Demonstrate **heap sort**:

  Below I only show the underlying array representation; trees would be
  just fine and easier to read.

  Heapify step:

  |  35  |  50  |  44  |  61  |  17  |  75  |  23  |   9  |
  |------|------|------|------|------|------|------|------|
  |  35  |  50  |**75**|  61  |  17  |**44**|  23  |   9  |
  |  35  |**61**|  75  |**50**|  17  |  44  |  23  |   9  |
  |**75**|  61  |**35**|  50  |  17  |  44  |  23  |   9  |
  |  75  |  61  |**44**|  50  |  17  |**35**|  23  |   9  |

  Sorting step:

  |** 9**|  61  |  44  |  50  |  17  |  35  |  23  |**75**|
  |------|------|------|------|------|------|------|------|
  |**61**|** 9**|  44  |  50  |  17  |  35  |  23  |  75  |
  |  61  |**50**|  44  |** 9**|  17  |  35  |  23  |  75  |
  |**23**|  50  |  44  |   9  |  17  |  35  |**61**|  75  |
  |**50**|**23**|  44  |   9  |  17  |  35  |  61  |  75  |
  |**35**|  23  |  44  |   9  |  17  |**50**|  61  |  75  |
  |**44**|  23  |**35**|   9  |  17  |  50  |  61  |  75  |
  |**17**|  23  |  35  |   9  |**44**|  50  |  61  |  75  |
  |**35**|  23  |**17**|   9  |  44  |  50  |  61  |  75  |
  |** 9**|  23  |  17  |**35**|  44  |  50  |  61  |  75  |
  |**23**|** 9**|  17  |  35  |  44  |  50  |  61  |  75  |
  |**17**|   9  |**23**|  35  |  44  |  50  |  61  |  75  |
  |** 9**|**17**|  23  |  35  |  44  |  50  |  61  |  75  |

+ (3) *(3pts)*
  + **insertion sort**: 21 assignments
  + **merge sort**: 48 copies
  + **heap sort**: 17 swaps 

+ (4a) *(5pts)* **Describe** Yaroslavskiy's algorithm:

  Yaroslavskiy's original paper can be found online
  (although I wasn't able to find a legal copy).

  Brad Lyon has made [a nice visualisation](https://learnforeverlearn.com/yaro_web/)
  of Yaroslavskiy's dual-pivot.

  In the original formulation, the two pivots are chosen to be the
  first and last elements of the (sub-)array.  For fully pre-sorted
  input, this still gives worst-case \`O(n^2)\` behaviour, as all the
  other elements will be in "Part II", in-between the two pivots.

  Yaroslavskiy's paper mentions a tweak ("additional improvement"),
  choosing the two pivots to be 1/3 and 2/3 of the way through the array.
  For pre-sorted input, this gives nice \`O(n lg n)\` behaviour,
  partitioning the array equally into thirds.

+ (4b) *(5pts)* **Pseudocode**:

  The [Princeton algorithms textbook](http://algs4.cs.princeton.edu/23quicksort/QuickDualPivot.java.html) site has a sample solution in Java.

  Yaroslavskiy also provided sample Java code in his original 2009 paper.

