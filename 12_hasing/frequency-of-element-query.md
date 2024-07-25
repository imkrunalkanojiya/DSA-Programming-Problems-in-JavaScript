# Frequency of element query

## Problem Description
Given an array A. You have some integers given in the array B.
For the i-th number, find the frequency of B[i] in the array A and return a list containing all the frequencies.

### Problem Constraints
````
1 <= |A| <= 10^5
1 <= |B| <= 10^5
1 <= A[i] <= 10^5
1 <= B[i] <= 10^5
````

### Input Format
````
First argument A is an array of integers.
Second argument B is an array of integers denoting the queries.
````

### Output Format
````
Return an array of integers containing frequency of the each element in B.
````

### Example Input
````
Input 1:
A = [1, 2, 1, 1]
B = [1, 2]

Input 2:
A = [2, 5, 9, 2, 8]
B = [3, 2]
````

### Example Output
````
Output 1:
[3, 1]

Output 2:
[0, 2]
````

### Example Explanation
````
Explanation 1:
The frequency of 1 in the array A is 3.
The frequency of 2 in the array A is 1.

Explanation 2:
The frequency of 3 in the array A is 0.
The frequency of 2 in the array A is 2.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function frequencyOfElements(A, B) {
    // Step 1: Count the frequency of each element in A
    const frequencyMap = {};
    for (let num of A) {
        if (frequencyMap[num]) {
            frequencyMap[num]++;
        } else {
            frequencyMap[num] = 1;
        }
    }

    // Step 2: Prepare the result for each element in B
    const result = [];
    for (let query of B) {
        result.push(frequencyMap[query] || 0);
    }

    return result;
}

// Example Inputs
const A1 = [1, 2, 1, 1];
const B1 = [1, 2];

const A2 = [2, 5, 9, 2, 8];
const B2 = [3, 2];

// Example Outputs
console.log(frequencyOfElements(A1, B1)); // Output: [3, 1]
console.log(frequencyOfElements(A2, B2)); // Output: [0, 2]
```