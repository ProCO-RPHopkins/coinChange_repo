# Coin Change

Problem Description
Given an integer array coins representing coins of different denominations and an integer amount representing a total amount of money, find the fewest number of coins needed to make up that amount. If it’s impossible to make up the given amount using the available coins, return -1.

Approach
Dynamic programming to solve this problem.

1. Initialize an array dp to store minimum number of coins needed for each amount from 0 to amount.
2. Set dp[0] to 0 (base case: 0 coins needed for amount 0).
3. Iterate through each coin denomination:
    - For each coin, update dp array by considering the current coin:
        - If i - coin (i is current amount) is a valid index and dp[i - coin] is not infinity, update dp[i] to be the minimum of its current value and dp[i - coin] + 1.
Finally, return dp[amount] if it’s not infinity (meaning the amount can be made up), otherwise return -1.
