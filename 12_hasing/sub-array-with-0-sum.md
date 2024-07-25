# Sub-array with 0 sum

## Problem Description
Given an array of integers A, find and return whether the given array contains a non-empty subarray with a sum equal to 0.

If the given array contains a sub-array with sum zero return 1, else return 0.

### Problem Constraints
````
1 <= |A| <= 100000
-10^9 <= A[i] <= 10^9
````

### Input Format
````
The only argument given is the integer array A.
````

### Output Format
````
Return whether the given array contains a subarray with a sum equal to 0.
````

### Example Input
````
Input 1:
A = [1, 2, 3, 4, 5]

Input 2:
A = [4, -1, 1]
````

### Example Output
````
Output 1:
0

Output 2:
1
````

### Example Explanation
````
Explanation 1:
No subarray has sum 0.

Explanation 2:
The subarray [-1, 1] has sum 0.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function hasZeroSumSubarray(A) {
    const cumSumSet = new Set();
    let cumSum = 0;

    for (let num of A) {
        cumSum += num;

        // Check if cumSum is 0 or if it has been seen before
        if (cumSum === 0 || cumSumSet.has(cumSum)) {
            return 1;
        }

        // Store the cumSum in the set
        cumSumSet.add(cumSum);
    }

    return 0;
}

// Example Inputs
const A1 = [1, 2, 3, 4, 5];
const A2 = [4, -1, 1];

// Example Outputs
console.log(hasZeroSumSubarray(A1)); // Output: 0
console.log(hasZeroSumSubarray(A2)); // Output: 1
```