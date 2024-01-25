
# LeetCode Challenge D39 

## Overview

Welcome to my LeetCode solution repository! This project addresses the coding challenge presented by [2144. Minimum Cost of Buying Candies With Discount](https://leetcode.com/problems/minimum-cost-of-buying-candies-with-discount/). Below, you'll find details about the problem, my approach to solving it, and the implemented solution.

## Problem Statement
A shop is selling candies at a discount. For  **every two**  candies sold, the shop gives a  **third**  candy for  **free**.

The customer can choose  **any**  candy to take away for free as long as the cost of the chosen candy is less than or equal to the  **minimum**  cost of the two candies bought.

-   For example, if there are  `4`  candies with costs  `1`,  `2`,  `3`, and  `4`, and the customer buys candies with costs  `2`  and  `3`, they can take the candy with cost  `1`  for free, but not the candy with cost  `4`.

Given a  **0-indexed**  integer array  `cost`, where  `cost[i]`  denotes the cost of the  `ith`  candy, return  _the  **minimum cost**  of buying  **all**  the candies_.

**Example**
> **Input:** cost = [1,2,3]
> 
>**Output:** 5
> 
>**Explanation:** We buy the candies with costs 2 and 3, and take the candy with cost 1 for free.
The total cost of buying all candies is 2 + 3 = 5. This is the **only** way we can buy the candies.
Note that we cannot buy candies with costs 1 and 3, and then take the candy with cost 2 for free.
The cost of the free candy has to be less than or equal to the minimum cost of the purchased candies.

**Language Used**
> Java

**Difficulty**
> Easy

## Solution Overview

The array of candy costs, represented by the `cost` parameter, is first sorted in ascending order using `Arrays.sort(cost)`. The algorithm then iterates through the sorted array from the highest cost to the lowest. For every two candies purchased, the cost of the cheaper candy is added to the `mincost` variable. The `count` variable is employed to keep track of the number of candies purchased, ensuring that for every pair, a third candy is obtained for free. The process repeats until all candies are considered. The final result is the minimum cost required to buy all candies with the discount. The algorithm focuses on pairing candies to maximize the number of free candies received and, subsequently, minimizing the overall cost.
