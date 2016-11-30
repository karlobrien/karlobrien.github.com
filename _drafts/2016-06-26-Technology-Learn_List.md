---
layout: post
title:  Tech For Learning
tags:
- node
- javascript
- html5
---
Items that I need to know


* HTML5.
* CSS.
  * Simple page layout
  * Responsive web design.
* Python for machine learning.
* F# for machine learning.
* Single Page Application.

The data B+Tree is an clustered index on the user id, and the email B+Tree is a non clustered index on the email. What is the difference between the two? A non clustered index contains as its value the key to find the relevant record. A clustered index contain the actual record data. In other words, after looking up a non clustered index, we need to go to the clustered index to find the actual data, while if we are using a clustered index, we are done with just one lookup.

# Async Syntax
let! response = req.AsyncGetResponse()
This means to not block on the response
! means continue
@ means concat

# Number Representation (F# For Quantitive Finance)
When we talk about integer representation without any negative numbers, that is, numbers from zero and up, we talk about unsigned integers.
When we talk about integers, denoted as Z, we are talking specifically about machine-precision integers that are represented exactly in the computer with a sequence of bits. Also, an integer is a number that can be written without a fractional or decimal component and is denoted as Z by convention. For example, 0 is represented as 000000..., 1 is represented as ...000001, 2 is represented as ...000010, and so on. As you can see from this pattern, numbers are represented in the power of two. To represent negative numbers, the number range is divided into two halves and uses two's complement.
int -> 32bit -> -127 - 128
long -> 64bit -> -64,000 - 64000 estimate.
floating points are used to model real world things - they are a quantity along a physical line
in machine terms, they are represented by an ieee standard - signed (1bit), exponent (11bits) and mantissa (52 bits)
1.2345 = 12345 (mantissa) X 10^-4

Binary representation
Floating-point number
0x0000000000000000
0.0
0x3ff0000000000000
1.0
0xc000000000000000
-2.0
0x4000000000000000
2.0
0x402E000000000000
15.0

Big O Notation
Log N - An algorithm with O(log N) performance typically divides the number of items it must consider by a fixed fraction at every step.
This algorithm is typical of many algorithms that have O(log N) performance. At each step, it divides roughly in half the number of items it must consider.
Full Binary tree - O(log n) steps

Node: FindItem(Integer: target_value)
    Node: test_node = <root of tree>

    Do Forever
      // If we fell off the tree. The value isn't present.
      If (test_node == null) Return null

      If (target_value == test_node.Value) Then
          // test_node holds the target value. This is the node we want.
          Return test_node
      Else If (target_value < test_node.Value) Then
          // Move to the left child.
          test_node = test_node.LeftChild
      Else
          // Move to the right child.
          test_node = test_node.RightChild
      End If
    End Do
End FindItem

The logarithmic function log(N) grows relatively slowly as N increases, so algorithms with O(log N) performance generally are fast enough to be useful.

See Essential Algorithms book on why the base value does not matter.

O(N) - The function N grows more quickly than log(N) and sqrt(N) but still not too quickly, so most algorithms that have O(N) performance work quite well in practice.

O(N Log N) - Suppose an algorithm loops over all the items in its problem set and then, for each loop, performs some sort of O(log N) calculation on that item. In that case, the algorithm has O(N × log N) or O(N log N) performance.

For example, suppose you have built a sorted tree containing N items as described earlier. You also have an array of N values and you want to know which values in the array are also in the tree.

One approach would be to loop through the values in the array. For each value, you could use the method described earlier to search the tree for that value. The algorithm examines N items and for each it performs log(N) steps so the total runtime is O(N log N).

Many sorting algorithms that work by comparing items have an O(N log N) runtime. In fact, it can be proven that any algorithm that sorts by comparing items must use at least O(N log N) steps, so this is the best you can do, at least in Big O notation. Some algorithms are still faster than others because of the constants that Big O notation ignores.

O(N2) - An algorithm that loops over all its inputs and then for each input loops over the inputs again has O(N2) performance.

O(2N) - Exponential functions such as 2N grow extremely quickly, so they are practical for only small problems. Typically algorithms with these runtimes look for optimal selection of the inputs.
Knapsack problem - This may seem like an easy problem, but the only known algorithms for finding the best possible solution essentially require you to examine every possible combination of items.
use heuristics to get best approximate result.

O(N!) - Traveling salesman


To find GCD, use euclid's algorithm.
Integer: GCD(Integer: A, Integer: B)
    While (B != 0)
        Integer: remainder = A Mod B
        // GCD(A, B) = GCD(B, remainder)
        A = B
        B = remainder
    End While
    Return A
End GCD
