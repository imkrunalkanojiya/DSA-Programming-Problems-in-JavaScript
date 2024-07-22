# Count Sort

## Problem Description
Given an array A. Sort this array using Count Sort Algorithm and return the sorted array.

### Problem Constraints
````
1 <= |A| <= 10^5
1 <= A[i] <= 10^5
````

### Input Format
````
The first argument is an integer array A.
````

### Output Format
````
Return an integer array that is the sorted array A.
````

### Example Input
````
Input 1:
A = [1, 3, 1]

Input 2:
A = [4, 2, 1, 3]
````

### Example Output
````
Output 1:
[1, 1, 3]

Output 2:
[1, 2, 3, 4]
````

### Example Explanation
````
Explanation 1:
The array in sorted order is [1, 1, 3].

Explanation 2:
The array in sorted order is [1, 2, 3, 4].
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function countSort(A){
        let max = 0;
        for(let i = 0 ; i < A.length ; i++){
            if(A[i] > max){
                max = A[i]
            }
        }    
        let countArr = Array(Number(max) + 1).fill(0)
        for(let i = 0 ; i < A.length ; i++){
            countArr[A[i]]++
        }
        let index = 0
        for(let i = 0 ; i < countArr.length ; i++){
            while(countArr[i] > 0){
                A[index] = i;
                index++;
                countArr[i]--;
            }
        }
        return A
}
```