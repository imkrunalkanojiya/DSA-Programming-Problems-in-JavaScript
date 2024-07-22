# Any base to decimal

## Problem Description
You are given a number A. You are also given a base B. A is a number on base B.
You are required to convert the number A into its corresponding value in decimal number system.

### Problem Constraints
````
0 <= A <= 10^9
2 <= B <= 9
````

### Input Format
````
First argument A is an integer.
Second argument B is an integer.
````

### Output Format
````
Return an integer.
````

### Example Input
````
Input 1:
A = 1010
B = 2

Input 2:
A = 22 
B = 3
````

### Example Output
````
Output 1:
10

Output 2:
8
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
function anyBaseToDecimal(A, B){
        const newA = String(A);
        let ans = 0;
        let start = 0;
        for(let i = newA.length - 1 ; i >= 0 ; i--){
            ans = ans + (Number(newA[i]) * Math.pow(B,start))
            start++
        }
        return ans
}
```