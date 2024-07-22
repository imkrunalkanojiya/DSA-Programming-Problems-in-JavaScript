# Number of 1 Bits

## Problem Description
Write a function that takes an integer and returns the number of 1 bits present in its binary representation.

### Problem Constraints
````
1 <= A <= 10^9
````

### Input Format
````
First and only argument contains integer A
````

### Output Format
````
Return an integer
````

### Example Input
````
Input 1:
11

Input 2:
6
````

### Example Output
````
Output 1:
3

Output 2:
2
````

### Example Explanation
````
Explanation 1:
11 is represented as 1011 in binary.

Explanation 2:
6 is represented as 110 in binary.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function numberOfIBit(A){
        let count = 0;
        for(let i = 0 ; i < 32 ; i++){
            if((1 << i) & A){
                count = count + 1;
            }
        }
        return count
}
```