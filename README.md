# Softnerve_Tech_Assement
**Question 1 : Leader in the Array**

Given a unsorted array, kindly find the leader in array . An element is called the leader of an 
array if there is no element greater than it on the right side
* Test case
  * int arr[] = {7, 10, 4, 10, 6, 5, 2}, n = 7;
  * 10 6 5 2

**Solutions**

```
def leader_the_array(arr,n):
    ans = []
    ans.append(arr[n-1])
    for i in range(n-2,-1,-1):
        if arr[i] > ans[len(ans)-1]:
            ans.append(arr[i])
    return ans[::-1]
```
**Question 2 :Best Time to Buy and Sell StocK**

You are given an array prices where prices[i] is the price of a given stock on the ith day.
You want to maximize your profit by choosing a single day to buy one stock and choosing a 
different day in the future to sell that stock.
Return the maximum profit you can achieve from this transaction. If you cannot achieve any 
profit, return 0.
* Test case
  * Input: prices = [7,1,5,3,6,4]
  * Output: 5
  * Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5
  * Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell
  * Input: prices = [7,6,4,3,1]
  * Output: 0
  * Explanation: In this case, no transactions are done and the max profit = 0

**Constraints:**

* **1 <= prices.length <= 105**
* **0 <= prices[i] <= 104**

**Solutions**

```
def maxProfit(prices):
    profit, left, right = 0 , 0, 1
    while right < len(prices):
        if prices[right] > prices[left]:
            cur_profit = prices[right] - prices[left]
            profit = max(cur_profit,profit)
        else:
            left = right
        right += 1
    return profit
```

**Question 3:Sum of All Subset XOR Totals**

The XOR total of an array is defined as the bitwise XOR of all its elements, or 0 if the array is 
empty.
For example, the XOR total of the array [2,5,6] is 2 XOR 5 XOR 6 = 1.
Given an array nums, return the sum of all XOR totals for every subset of nums.
Note: Subsets with the same elements should be counted multiple times.
An array a is a subset of an array b if a can be obtained from b by deleting some (possibly zero) 
elements of b.
* Test Case
  * Input: nums = [1,3]
  * Output: 6
  * Explanation: The 4 subsets of [1,3] are:
    - The empty subset has an XOR total of 0.
    - [1] has an XOR total of 1
    - [3] has an XOR total of 3
    - [1,3] has an XOR total of 1 XOR 3 = 2
    - 0 + 1 + 3 + 2 = 6
  * Input: nums = [5,1,6]
  * Output: 28
  * Explanation: The 8 subsets of [5,1,6] are:
    - The empty subset has an XOR total of 0
    - [5] has an XOR total of 5
    - [1] has an XOR total of 1.
    - [6] has an XOR total of 6.
    - [5,1] has an XOR total of 5 XOR 1 = 4
    - [5,6] has an XOR total of 5 XOR 6 = 3
    - [1,6] has an XOR total of 1 XOR 6 = 7
    - [5,1,6] has an XOR total of 5 XOR 1 XOR 6 = 2
    - 0 + 5 + 1 + 6 + 4 + 3 + 7 + 2 = 28

**Solutions**

```
def xorSum(arr):
    bits,n = 0,len(arr)
    for i in range(n):
        bits |= arr[i]
    ans = bits * pow(2, n-1)
    return ans
```

**1.	Rating in scale of DSA**

* 7 out of 10
* problem solving in array I am very good at it.
* In algorithmis I like to use Divide And conquer method

**2.	Leetcode / hacker rank. code chef ranking**
* Codewar Rating  is 921 kata
* and Leaderboard Position is 31,761
* Leetcode highest rating is 1477 and ranking was 7129
* code chef highest rating is 1536 and global ranking was 2867

**3.	Deep learning rating – (Mentioned if worked in GAN Related project)**
* 6 out of 10

