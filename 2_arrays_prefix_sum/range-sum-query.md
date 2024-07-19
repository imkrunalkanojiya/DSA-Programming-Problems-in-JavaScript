# Range Sum Query

## Problem Description
You are given an integer array A of length N. You are also given a 2D integer array B with dimensions M x 2, where each row denotes a [L, R] query. For each query, you have to find the sum of all elements from L to R indices in A (0 - indexed).

More formally, find A[L] + A[L + 1] + A[L + 2] +... + A[R - 1] + A[R] for each query.

### Problem Constraints
````
1 <= N, M <= 10^5
1 <= A[i] <= 10^9
0 <= L <= R < N
````

### Input Format
````
The first argument is the integer array A.
The second argument is the 2D integer array B.
````

### Output Format
````
Return an integer array of length M where ith element is the answer for ith query in B.
````

### Example Input
````
Input 1:
A = [1, 2, 3, 4, 5]
B = [[0, 3], [1, 2]]

Input 2:
A = [2, 2, 2]
B = [[0, 0], [1, 2]]
````

### Example Output
````
Output 1:
[10, 5]

Output 2:
[2, 4]
````

### Example Explanation
````
Explanation 1:
The sum of all elements of A[0 ... 3] = 1 + 2 + 3 + 4 = 10.
The sum of all elements of A[1 ... 2] = 2 + 3 = 5.

Explanation 2:
The sum of all elements of A[0 ... 0] = 2 = 2.
The sum of all elements of A[1 ... 2] = 2 + 2 = 4.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function rangeSumQuery(A, B){
        const preFixSum = [];
        const rangeSum = []
        preFixSum[0] = A[0];
        for(let i = 1; i <A.length ; i++){
            preFixSum[i] = preFixSum[i - 1] + A[i]
        }
        for(let j = 0; j < B.length ; j++){
            if(B[j][0] == 0){
                rangeSum.push(preFixSum[B[j][1]])
            }else{
                rangeSum.push(preFixSum[B[j][1]] - preFixSum[B[j][0] - 1])
            }

        }
        return rangeSum
}
```