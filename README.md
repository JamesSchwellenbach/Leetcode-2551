# Leetcode 2551. Put Marbles in Bags (Hard)

# Problem

You have k bags. You are given a 0-indexed integer array weights where weights[i] is the weight of the ith marble. You are also given the integer k.

Divide the marbles into the k bags according to the following rules:

No bag is empty.
If the ith marble and jth marble are in a bag, then all marbles with an index between the ith and jth indices should also be in that same bag.
If a bag consists of all the marbles with an index from i to j inclusively, then the cost of the bag is weights[i] + weights[j].
The score after distributing the marbles is the sum of the costs of all the k bags.

Return the difference between the maximum and minimum scores among marble distributions.

Solution O(NLogN)

Create an array of sums for each neighboring index, the first pair will be index 0 + 1, the second will be index 1 + 2 and so on. Then sort the pair list in ascending order
from there the maximum score will be the sum of the last k-1 values in the pair list and the minimum score will be the first k-1 values in the pair list, so return the sum
of the last k-1 values minus the sum of the first k-1 values.
