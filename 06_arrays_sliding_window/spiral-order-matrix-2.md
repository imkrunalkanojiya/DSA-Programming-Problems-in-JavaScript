# Spiral Order Matrix II

## Problem Description
Given an integer A, generate a square matrix filled with elements from 1 to A2 in spiral order and return the generated square matrix.

### Problem Constraints
````
1 <= A <= 1000
````

### Input Format
````
First and only argument is integer A
````

### Output Format
````
Return a 2-D matrix which consists of the elements added in spiral order.
````

### Example Input
````
Input 1:
1

Input 2:
2
````

### Example Output
````
Output 1:
[ [1] ]

Output 2:
[ [1, 2], 
  [4, 3] ]
````

### Example Explanation
````
Explanation 1:
Only 1 is to be arranged.

Explanation 2:
1 --> 2
      |
      |
4<--- 3
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function spiralOrderMatrixII(A){
        
        const matrix = Array.from({ length: A }, () => Array(A).fill(0));
        let top = 0;
        let bottom = A - 1;
        let left = 0;
        let right =  A - 1;

        let current = 1;

        while(current <= A*A){
            for(let i = left ; i <= right ; i++){
                matrix[top][i] = current;
                current++;
            }
            top++;
            
            for(let i = top ; i <= bottom ; i++){
                matrix[i][right] = current;
                current++;
            }
            right--
            
            for(let i = right ; i >= left ; i--){
                matrix[bottom][i] = current;
                current++
            }
            bottom--;
            
            for(let i = bottom ; i >= top ; i--){
                matrix[i][left] = current;
                current++;
            }
            left++
        }

        return matrix
}
```