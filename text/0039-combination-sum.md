- Start Date: 2021-01-20
- URL: [Combination Sum](https://leetcode.com/problems/combination-sum/)

# DFS Approach

The initial thought to count all combination is counting all elements of candidates in order. With `candidates = [2,3,6,7], target = 7`, we would start with [2, 2, ,2 , 2], [2, 2, 3], [2, 2, 6], [2, 3, 3] and so on. This is a common pattern to use DFS.

