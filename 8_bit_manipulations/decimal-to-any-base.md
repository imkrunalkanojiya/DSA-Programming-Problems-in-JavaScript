# Decimal to Any Base

## Problem Description
Given a decimal number A and a base B, convert it into its equivalent number in base B.

### Problem Constraints
````
0 <= A <= 512
2 <= B <= 10
````

### Input Format
````
The first argument will be decimal number A.
The second argument will be base B.
````

### Output Format
````
Return the conversion of A in base B.
````

### Example Input
````
Input 1:
A = 4
B = 3

Input 2:
A = 4
B = 2 
````

### Example Output
````
Output 1:
11

Output 2:
100
````

### Example Explanation
````
Explanation 1:
The decimal 10 in base 2 is 1010.

Explanation 2:
The decimal 8 in base 3 is 22.
````

### Output
``` javascript showLineNumbers copy filename="JavaScript"
function decimalToBase(A, B) {
    if (A === 0) return '0';

    let result = '';
    while (A > 0) {
        let remainder = A % B;
        result = remainder + result;
        A = Math.floor(A / B);
    }

    return result;
}

// Example usage:
console.log(decimalToBase(4, 3)); // Output: "11"
console.log(decimalToBase(4, 2)); // Output: "100"
```