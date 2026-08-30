# Two Sum

## LeetCode
https://leetcode.com/problems/two-sum/

## Difficulty
Easy

## Topic
Array
Hash Table

## Problem

Given an array of integers `nums` and an integer `target`,
return indices of the two numbers such that they add up to target.

## Example

Input:

nums = [2,7,11,15]
target = 9

Output:

[0,1]

## Approach

Use a HashMap to store numbers that we have already seen.

For every number:

1. Calculate complement = target - current number.
2. Check whether complement exists in the HashMap.
3. If yes, return the indices.
4. Otherwise store the current number and its index.

## Complexity

Time: O(n)

Space: O(n)

## Key Learning

A HashMap allows us to find the required complement
in O(1) average time.

## Mistakes

Initially I tried the brute-force approach using two loops,
which gives O(n²) time complexity.

The HashMap approach improves this to O(n).