# Count distinct elements

## Problem Description
Given an array A of N integers, return the number of unique elements in the array.

### Problem Constraints
````
1 <= N <= 10^5
1 <= A[i] <= 10^9
````

### Input Format
````
First argument A is an array of integers.
````

### Output Format
````
Return an integer.
````

### Example Input
````
Input 1:
A = [3, 4, 3, 6, 6]

Input 2:
A = [3, 3, 3, 9, 0, 1, 0]
````

### Example Output
````
Output 1:
3

Output 2:
4
````

### Example Explanation
````
Explanation 1:
The distinct elements of the array are 3, 4 and 6.

Explanation 2:
The distinct elements of the array are 3, 9, 0 and 1.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function countDistinctElements(A) {
    const uniqueElements = new Set(A);
    return uniqueElements.size;
}

// Example Inputs
const A1 = [3, 4, 3, 6, 6];
const A2 = [3, 3, 3, 9, 0, 1, 0];

// Example Outputs
console.log(countDistinctElements(A1)); // Output: 3
console.log(countDistinctElements(A2)); // Output: 4
```