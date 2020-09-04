---
layout: post
title: Summation of numbers from 1 to n
---



Question of interest: Given an integer n, find the sum of numbers from 1 to n.


You can obviously do it brute force method but that would take longer so to reduce that effort we can use a nifty trick.

Lets give ourselves an example here. Lets have n = 10 and say that we want to find the sum of numbers from 1 to 10.

Lets write this out to see the trick.

1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10 + 11

The key obervation here is that if you take two numbers x and y and set them to 1 and 11 respectively, the sum will equal 12.
now what if you take 2 and 10? Ahhhhh. The sum is equal to 12 as well. If you keep doing this u will realize all of them of this 
pattern add up to 12! Now the question here is can we make a general formula from this observation?
Fortunately yes. since each pair of opposite numbers add up to the same number, you can say that there are going to be 
x instances of the sum y for instance. So for this example it would be x * (12). What would x be? since there are n numbers 
and since each sum is made from 2 numbers there would be n/2 numbers being added to the same sum. Therefore the sum would be


n/2 * (x1 + xn)

This is way easier to compute and could take seconds with a calulcator.

