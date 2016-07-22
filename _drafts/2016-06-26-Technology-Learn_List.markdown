---
layout: post
title:  "Tech For Learning"
date:   2016-06-25
categories: software nodejs javascript html5
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

# Number Representation
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
