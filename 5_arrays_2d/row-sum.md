# Row Sum

## Problem Description
Find Row Sum of given A array.

### Problem Constraints
````
1 <= A.size() <= 10^3
1 <= A[i].size() <= 10^3
1 <= A[i][j] <= 10^3
````

### Input Format
````
First argument A is a 2D array of integers.(2D matrix).
````

### Output Format
````
Return an array containing row-wise sums of original matrix.
````

### Example Input
````
Input 1:
[1,2,3,4]
[5,6,7,8]
[9,2,3,4]
````

### Example Output
````
Output 1:
[10,26,18]
````

### Example Explanation
````
Explanation 1:
Row 1 = 1+2+3+4 = 10
Row 2 = 5+6+7+8 = 26
Row 3 = 9+2+3+4 = 18
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function rowSum(A){
        for(let i = 0 ; i < A.length ; i++){
            let sum = 0;
            for(let j = 0 ; j < A[i].length ; j++){
                sum = Number(sum) + Number(A[i][j])
            }
            A[i] = sum
        }
        return A
}
```