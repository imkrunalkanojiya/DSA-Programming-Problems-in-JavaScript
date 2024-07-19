# DSA Programming Problems in JavaScript

Welcome to the repository of Data Structures and Algorithms (DSA) programming problems solved using JavaScript. This collection includes a variety of problems categorized by their types and complexity. Each problem is accompanied by a solution.

## Table of Contents

1. [Introduction To Arrays](#array-problems)
2. [Bit Manipulations](#bit-manipulations)

## Array Problems

| Problem | Description | Solution |
| ------- | ----------- | -------- |
| Array Rotation | Given an integer array A of size N and an integer B, you have to return the same array after rotating it B times towards the right.| [View](./1_introduction_to_arrays/array-rotation.md) |
| Count Of Elements | Given an array A of N integers. Count the number of elements that have at least 1 elements greater than itself.| [View](./1_introduction_to_arrays/count-of-elements.md) |
| Good Pair | Given an array A and an integer B. A pair(i, j) in the array is a good pair if i != j and (A[i] + A[j] == B). Check if any good pair exist or not. | [View](./1_introduction_to_arrays/good-pair.md) |
| Linear Search - Multiple Occurences | Given an array A and an integer B, find the number of occurrences of B in A. | [View](./1_introduction_to_arrays/linear-search-multiple-occurences.md) |
| Max Min of an Array | Given an array A of size N. You need to find the sum of Maximum and Minimum element in the given array. | [View](./1_introduction_to_arrays/max-min-of-array.md) |
| Reverse in a range | Given an array A of N integers and also given two integers B and C. Reverse the elements of the array A within the given inclusive range [B, C]. | [View](./1_introduction_to_arrays/reverse-in-range.md) |
| Equilibrium index of an array | Your task is to find the equilibrium index of the given array | [View](./2_arrays_prefix_sum/equilibrium-index-of-an-array.md) |
| Even numbers in a range | You are given an array A of length N and Q queries given by the 2D array B of size Q×2. | [View](./2_arrays_prefix_sum/even-numbers-in-range.md) |
| In-place Prefix Sum | Given an array A of N integers. Construct prefix sum of the array in the given array itself. | [View](./2_arrays_prefix_sum/in-place-prefix-sum.md) |
| Product array puzzle | Given an array of integers A, find and return the product array of the same size where the ith element of the product array will be equal to the product of all the elements divided by the ith element of the array. | [View](./2_arrays_prefix_sum/product-array-puzzle.md) |
| Range Sum Query | You are given an integer array A of length N. You are also given a 2D integer array B with dimensions M x 2, where each row denotes a [L, R] query. For each query, you have to find the sum of all elements from L to R indices in A (0 - indexed). | [View](./2_arrays_prefix_sum/range-sum-query.md) |
| Closest MinMax | Given an array A, find the size of the smallest subarray such that it contains at least one occurrence of the maximum value of the array and at least one occurrence of the minimum value of the array. | [View](./3_arrays_carry_forword/closest-min-max.md) |
| Leaders in an array | Given an integer array A containing N distinct integers, you have to find all the leaders in array A. An element is a leader if it is strictly greater than all the elements to its right side. | [View](./3_arrays_carry_forword/leaders-in-an-array.md) |
| Special Subsequences "AG" | You have given a string A having Uppercase English letters. You have to find how many times subsequence "AG" is there in the given string. | [View](./3_arrays_carry_forword/special-subsequences.md) |
| Generate all subarrays | You are given an array A of N integers. Return a 2D array consisting of all the subarrays of the array | [View](./4_arrays_subarrays/generate-all-subarrays.md) |
| Maximum Subarray Easy | You are given an integer array C of size A. Now you need to find a subarray (contiguous elements) so that the sum of contiguous elements is maximum. But the sum must not exceed B. | [View](./4_arrays_subarrays/maximum-subarray-easy.md) |
| Subarray in given range | Given an array A of length N, return the subarray from B to C. | [View](./4_arrays_subarrays/subarray-in-given-range.md) |
| Sum of All Subarrays | You are given an integer array A of length N. You have to find the sum of all subarray sums of A. | [View](./4_arrays_subarrays/sum-of-all-subarrays.md) |
| Anti Diagonals | Give a N * N square matrix A, return an array of its anti-diagonals. Look at the example for more details. | [View](./5_arrays_2d/anti-diagonals.md) |
| Column Sum | You are given a 2D integer matrix A, return a 1D integer array containing column-wise sums of original matrix. | [View](./5_arrays_2d/column-sum.md) |
| Main Diagonal Sum | You are given a N X N integer matrix. You have to find the sum of all the main diagonal elements of A. Main diagonal of a matrix A is a collection of elements A[i, j] such that i = j. | [View](./5_arrays_2d/main-diagonal-sum.md) |
| Matrix Transpose | Given a 2D integer array A, return the transpose of A. | [View](./5_arrays_2d/matrix-transpose.md) |
| Minor Diagonal Sum | You are given a N X N integer matrix. You have to find the sum of all the minor diagonal elements of A. | [View](./5_arrays_2d/minor-diagonal-sum.md) |
| Rotate Matrix | You are given a n x n 2D matrix A representing an image. | [View](./5_arrays_2d/rotate-matrix.md) |
| Row Sum | Find Row Sum of given A array. | [View](./5_arrays_2d/row-sum.md) |
| Minimum Swaps | Given an array of integers A and an integer B, find and return the minimum number of swaps required to bring all the numbers less than or equal to B together. | [View](./6_arrays_sliding_window/minimum-swaps.md) |
| Spiral Order Matrix II | Given an integer A, generate a square matrix filled with elements from 1 to A2 in spiral order and return the generated square matrix. | [View](./6_arrays_sliding_window/spiral-order-matrix-2.md) |
| Subarray with given sum and length |Given an array A of length N. Also given are integers B and C. Return 1 if there exists a subarray with length B having sum C and 0 otherwise | [View](./6_arrays_sliding_window/subarray-with-given-sum-and-length.md) |
| Sum of even indices | You are given an array A of length N and Q queries given by the 2D array B of size Q*2. Each query consists of two integers B[i][0] and B[i][1]. | [View](./7_arrays_extra_problems/sum-of-even-indices.md) |

## Bit Manipulations

| Problem | Description | Solution |
| ------- | ----------- | -------- |
| Any base to decimal | You are given a number A. You are also given a base B. A is a number on base B. You are required to convert the number A into its corresponding value in decimal number system.| [View](./8_bit_manipulations/any-base-to-decimal.md) |
| Check bit | You are given two integers A and B. Return 1 if B-th bit in A is set. Return 0 if B-th bit in A is unset| [View](./8_bit_manipulations/check-bit.md) |
| Decimal to Any Base | Given a decimal number A and a base B, convert it into its equivalent number in base B. | [View](./8_bit_manipulations/decimal-to-any-base.md) |
| Number of 1 Bits | Write a function that takes an integer and returns the number of 1 bits present in its binary representation. | [View](./8_bit_manipulations/number-of-1-bits.md) |
| Set Bit | You are given two integers A and B. Set the A-th bit and B-th bit in 0, and return output in decimal Number System. | [View](./8_bit_manipulations/set-bit.md) |
| Single Number | Given an array of integers A, every element appears twice except for one. Find that integer that occurs once. | [View](./8_bit_manipulations/single-number.md) |
| Unset i-th bit | You are given two integers A and B. If B-th bit in A is set, make it unset. If B-th bit in A is unset, leave as it is. | [View](./8_bit_manipulations/unset-i-th-bit.md) |


## Support
If you find the content of this repo interesting and helpful, use the “Buy me a Coffee” link below to buy me a coffee.

<a href="https://buymeacoffee.com/krunalkanojiya" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>

![gif](https://media.giphy.com/media/gTURHJs4e2Ies/giphy.gif)

## Licence
MIT Licence by TechAlgoSpotlight.com

![photo](https://techalgospotlight.com/wp-content/uploads/2024/06/Group-9.png)