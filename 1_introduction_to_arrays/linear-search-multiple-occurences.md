# Linear Search - Multiple Occurences

## Problem Description
Given an array A and an integer B, find the number of occurrences of B in A.

### Problem Constraints
````
1 <= B, Ai <= 10^9
1 <= |A| <= 10^5
````

### Input Format
````
Given an integer array A and an integer B.
````

### Output Format
````
Return an integer, number of occurrences of B in A.
````

### Example Input
````
Input 1:
A = [1, 2, 2], B = 2 

Input 2:
A = [1, 2, 1], B = 3
````

### Example Output
````
Output 1:
2

Output 2:
0 
````

### Example Explanation
````
Explanation 1:
Element at index 2, 3 is equal to 2 hence count is 2. 

Explanation 2:
There is no element equal to 3 in the array.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function countOccurrences(A, B) {
    return A.filter(val => val === B).length;
}

// Test cases
const arr1 = [1, 2, 2];
const val1 = 2;
console.log(countOccurrences(arr1, val1)); // Output: 2

const arr2 = [1, 2, 1];
const val2 = 3;
console.log(countOccurrences(arr2, val2)); // Output: 0
```