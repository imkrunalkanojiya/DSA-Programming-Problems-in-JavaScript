# Divisibility by 3

## Problem Description
Given a number in the form of an array A of size N. Each of the digits of the number is represented by A[i]. Check if the number is divisible by 3.

### Problem Constraints
````
1 <= N <= 10^5
0 <= A[i] <= 9
A[1] ≠ 0
````

### Input Format
````
Given an integer array representing the number
````

### Output Format
````
Return 1 if the number is divisible by 3 and return 0 otherwise.
````

### Example Input
````
Input 1:
A = [1, 2, 3]

Input 2:
A = [1, 0, 0, 1, 2]
````

### Example Output
````
Output 1:
1

Output 2:
0
````

### Example Explanation
````
Explanation 1:
The number 123 is divisible by 3.

Explanation 2:
The number 10012 is not divisible by 3.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function isDivisibleBy3(A) {
    let sum = 0;
    for (let i = 0; i < A.length; i++) {
        sum += A[i];
    }
    return sum % 3 === 0 ? 1 : 0;
}

// Example usage:
console.log(isDivisibleBy3([1, 2, 3])); // Output: 1
console.log(isDivisibleBy3([1, 0, 0, 1, 2])); // Output: 0
```