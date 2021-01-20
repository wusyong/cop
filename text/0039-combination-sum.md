- Start Date: 2021-01-20
- URL: [Combination Sum](https://leetcode.com/problems/combination-sum/)

# DFS Approach

The initial thought to count all combination is counting all elements of candidates in order. With `candidates = [2,3,6,7], target = 7`, we would start with [2, 2, ,2 , 2], [2, 2, 3], [2, 2, 6], [2, 3, 3] and so on. This is a common pattern to use DFS.

- Sort the candidate because the description warns us it is in any order.
- DFS usually would run a function recursively, so we define another function `dfs` and take all inputs with it. We also need a vector to store the `result` and a vector to record current `combination`.
- We define another parameter `remaing` to determine the current remaining value that could add to the `combination`. The first call of DFS functoin would pass the target value.
- The loop inside the function would iterate the whole `candidates` everytime since same value can be added repetively. We need to add another condition to make sure `remaining` is equal or greater than current element value in `candidates`. Otherwise, we consider this depth branch is done, and we stop the loop to return.
- The loop will push current `candidates` element value to `combination` and call the `dfs` again to proceed to deeper depth. When the call is returned. We pop current `candidates` element value and iterate to next one.
- To terminate the recursion, we need to add a condition before the loop which determine if the remaining value is zero. If so, that means the `combination` is right. We push it to `result` and return.
- After the iteration is done, the `result` would contain all combinations we need.