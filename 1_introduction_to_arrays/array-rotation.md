# Array Rotation

## Problem Description
Given an integer array A of size N and an integer B, you have to return the same array after rotating it B times towards the right.


### Problem Constraints
````
1 <= N <= 10^5
1 <= A[i] <=10^9
1 <= B <= 10^9
````

### Input Format
````
The first argument given is the integer array A.
The second argument given is the integer B.
````

### Output Format
````
Return the array A after rotating it B times to the right
````

### Example Input
````
Input 1:
A = [1, 2, 3, 4]
B = 2

Input 2:
A = [2, 5, 6]
B = 1
````

### Example Output
````
Output 1:
[3, 4, 1, 2]

Output 2:
[6, 2, 5]
````

### Example Explanation
````
Explanation 1:
Rotate towards the right 2 times - [1, 2, 3, 4] => [4, 1, 2, 3] => [3, 4, 1, 2]

Explanation 2:
Rotate towards the right 1 time - [2, 5, 6] => [6, 2, 5]
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function rotateArray(A, B) {
    const N = A.length;
    const result = new Array(N).fill(0);

    for (let i = 0; i < N; i++) {
        result[(i + B) % N] = A[i];
    }
    return result;
}
```