# Closest MinMax

## Problem Description
Given an array A, find the size of the smallest subarray such that it contains at least one occurrence of the maximum value of the array and at least one occurrence of the minimum value of the array.


### Problem Constraints
````
1 <= |A| <= 2000
````

### Input Format
````
First and only argument is vector A
````

### Output Format
````
Return the length of the smallest subarray which has at least one occurrence of minimum and maximum element of the array
````

### Example Input
````
Input 1:
A = [1, 3, 2]

Input 2:
A = [2, 6, 1, 6, 9]
````

### Example Output
````
Output 1:
2

Output 2:
3
````

### Example Explanation
````
Explanation 1:
Take the 1st and 2nd elements as they are the minimum and maximum elements respectievly.

Explanation 2:
Take the last 3 elements of the array.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function closestMinMaxSize(A) {
    let minIndex = -1;
    let maxIndex = -1;
    let minMaxSize = Infinity;

    const min = Math.min(...A);
    const max = Math.max(...A);

    A.forEach((value, index) => {
        if (value === min) {
            minIndex = index;
        }
        if (value === max) {
            maxIndex = index;
        }
        if (minIndex !== -1 && maxIndex !== -1) {
            minMaxSize = Math.min(minMaxSize, Math.abs(maxIndex - minIndex) + 1);
        }
    });

    return minMaxSize;
}

const A1 = [1, 3, 2];
const A2 = [2, 6, 1, 6, 9];

console.log("Output 1:", closestMinMaxSize(A1));
console.log("Output 2:", closestMinMaxSize(A2));
```