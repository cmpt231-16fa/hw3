---
layout: page
title: "HW3: CMPT231"
subtitle: "Lecture 3, ch6-7"
ext-js: "https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=AM_CHTML"
---

{% include policies.md %}

### HW3 (20pts)
1. *(3pts)* Assuming all distinct keys, what are all the possible locations
  for the **smallest** element in a **max heap**? Why? 

2. *(5pts)* Demonstrate **heap sort** on the following input: <br/>
  `[ 12, 16, 7, 11, 19, 3, 6, 10, 5, 8, 14, 9, 15 ]`

3. *(2pts)*

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
