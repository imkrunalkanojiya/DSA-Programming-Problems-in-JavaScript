# Product array puzzle

## Problem Description
Given an array of integers A, find and return the product array of the same size where the ith element of the product array will be equal to the product of all the elements divided by the ith element of the array.

Note: It is always possible to form the product array with integer (32 bit) values. Solve it without using the division operator.

### Problem Constraints
````
2 <= length of the array <= 1000
1 <= A[i] <= 10
````

### Input Format
````
The only argument given is the integer array A.
````

### Output Format
````
Return the product array.
````

### Example Input
````
Input 1:
A = [1, 2, 3, 4, 5]

Input 2:
A = [5, 1, 10, 1]
````

### Example Output
````
Output 1:
[120, 60, 40, 30, 24]

Output 2:
[10, 50, 5, 50]
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function productArray(A) {
    const n = A.length;
    const leftProducts = new Array(n).fill(0);
    const rightProducts = new Array(n).fill(0);
    const productArray = new Array(n).fill(0);

    leftProducts[0] = 1;
    rightProducts[n - 1] = 1;

    // Calculating products of elements to the left
    for (let i = 1; i < n; i++) {
        leftProducts[i] = A[i - 1] * leftProducts[i - 1];
    }

    // Calculating products of elements to the right
    for (let i = n - 2; i >= 0; i--) {
        rightProducts[i] = A[i + 1] * rightProducts[i + 1];
    }

    // Calculate the product array
    for (let i = 0; i < n; i++) {
        productArray[i] = leftProducts[i] * rightProducts[i];
    }

    return productArray;
}
```