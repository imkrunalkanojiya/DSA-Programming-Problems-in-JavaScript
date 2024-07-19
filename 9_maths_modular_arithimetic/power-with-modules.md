# Power with Modules

## Problem Description
You are given A, B and C .
Calculate the value of (A ^ B) % C

### Problem Constraints
````
1 <= A <= 10^9
0 <= B <= 10^5
1 <= C <= 10^9
````

### Input Format
````
Given three integers A, B and C.
````

### Output Format
````
Return an integer
````

### Example Input
````
Input 1:
A = 2
B = 3
C = 3

Input 2:
A = 5
B = 2
C = 4
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
(2 ^ 3) % 3 = 8 % 3 = 2

Explanation 2:
(5 ^ 2) % 4 = 25 % 4 = 1
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function powerMod(A, B, C) {
    if (B === 0) return 1 % C;  // Any number to the power of 0 is 1, but we should return 1 % C

    let half = powerMod(A, Math.floor(B / 2), C);
    half = (half * half) % C;

    if (B % 2 !== 0) {
        half = (half * A) % C;
    }

    return half;
}

// Example usage:
console.log(powerMod(2, 3, 3)); // Output: 2
console.log(powerMod(5, 2, 4)); // Output: 1
```