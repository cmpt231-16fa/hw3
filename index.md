---
layout: page
title: "HW3: CMPT231"
subtitle: "Lecture 3, ch6-7"
ext-js: "https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=AM_CHTML"
---

{% include policies.md %}

### HW3 (20pts)
1. *(3pts)* Assuming all distinct keys, what are all the possible locations
  for the **smallest** element in a **max heap**? Where do they lie in the
  **array** representation?

2. *(4pts)* Demonstrate **heap sort** on the following input (same as in HW1 and HW2): <br/>
  `[ 35, 50, 44, 61, 17, 75, 23, 9 ]`

3. *(3pts)* Now that you've sorted the same array using insertion sort, merge sort, and heap sort, **count** the number of *operations* in each:
  + For *insertion sort*, count the number of **assignments** when a value is written into the array.
  + For *merge sort*, count the number of **copies** performed, including *both* when elements are copied to temporary arrays and when they are copied back.
  + For *heap sort*, count the number of **swaps** (each swap counts as one operation).

4. Java's standard library for sorting `Array`s uses (as of Oracle Java 7)
  a **"dual-pivot"** variant of Quicksort due to Yaroslavskiy et al. (2009).
  + a. *(5pts)* Research Yaroslavskiy's algorithm and **describe** how
    it works.  How does its behaviour differ from Quicksort on 
    **pre-sorted** or partially pre-sorted data?
    (There are several kinds of dual-pivot algorithms; focus on the one
    by Yaroslavskiy. The Java library also adds a few optimisations
    that you can ignore.)
    If you found code or a reference somewhere that helped you,
    include a link to it as a citation.
  + b. *(5pts)* Present your own **pseudocode** implementation
    of Yaroslavskiy's Quicksort.
    It should be your own work (i.e., not cut-and-paste, you need to
    understand how it works), but if you found code that helped you,
    include a link to it.
