# Largest Number

## Problem Description
Given an array A of non-negative integers, arrange them such that they form the largest number.

Note: The result may be very large, so you need to return a string instead of an integer.

### Problem Constraints
````
1 <= len(A) <= 100000
0 <= A[i] <= 2*109
````

### Input Format
````
The first argument is an array of integers.
````

### Output Format
````
Return a string representing the largest number.
````

### Example Input
````
Input 1:
A = [3, 30, 34, 5, 9]

Input 2:
A = [2, 3, 9, 0]
````

### Example Output
````
Output 1:
"9534330"

Output 2:
"9320"
````

### Example Explanation
````
Explanation 1:
Reorder the numbers to [9, 5, 34, 3, 30] to form the largest number.

Explanation 2:
Reorder the numbers to [9, 3, 2, 0] to form the largest number 9320.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function largestNumber(A) {
    if (A.length === 0) return "";

    // Custom comparator to sort based on concatenation results
    A.sort((a, b) => {
        let order1 = '' + a + b;
        let order2 = '' + b + a;
        return order2.localeCompare(order1);
    });

    // Edge case: if the highest number is 0, return "0"
    if (A[0] == 0) return "0";

    // Join the sorted array to form the largest number
    return A.join('');
}

// Example usage
console.log(largestNumber([3, 30, 34, 5, 9])); // Output: "9534330"
console.log(largestNumber([2, 3, 9, 0]));       // Output: "9320"
```