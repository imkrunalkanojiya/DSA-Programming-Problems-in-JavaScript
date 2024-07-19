# Count of elements

## Problem Description
Given an array A of N integers. Count the number of elements that have at least 1 elements greater than itself.

### Problem Constraints
````
1 <= N <= 10^5
1 <= A[i] <= 10^9    
````

### Input Format
````
First and only argument is an array of integers A.
````

### Output Format
````
Return the count of elements.
````

### Example Input
````
Input 1:
A = [3, 1, 2]

Input 2:
A = [5, 5, 3]
````

### Example Output
````
Output 1:
2

Output 2:
1
````

### Example Explanation
````
Explanation 1:
The elements that have at least 1 element greater than itself are 1 and 2

Explanation 2:
The elements that have at least 1 element greater than itself is 3
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function countElements(A) {
    let maxSoFar = -Infinity;
    let count = 0;
    
    for (let i = 0; i < A.length; i++) {
        if (A[i] > maxSoFar) {
            maxSoFar = A[i];
            count++;
        }
    }
    
    return count;
}
```