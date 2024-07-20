# Noble Integer

## Problem Description
Given an integer array A, find if an integer p exists in the array such that the number of integers greater than p in the array equals p.

### Problem Constraints
````
1 <= |A| <= 2*10^5
-108 <= A[i] <= 10^8
````

### Input Format
````
First and only argument is an integer array A.
````

### Output Format
````
Return 1 if any such integer p is present else, return -1.
````

### Example Input
````
Input 1:
A = [3, 2, 1, 3]

Input 2:
A = [1, 1, 3, 3]
````

### Example Output
````
Output 1:
1

Output 2:
-1
````

### Example Explanation
````
Explanation 1:
For integer 2, there are 2 greater elements in the array..

Explanation 2:
There exist no integer satisfying the required conditions.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function findNobleInteger(A) {
    // Sort the array in ascending order
    A.sort((a, b) => a - b);
    
    const n = A.length;

    for (let i = 0; i < n; i++) {
        // If this is the last element or the next element is different
        if (i < n - 1 && A[i] == A[i + 1]) {
            continue;
        }
        // Number of elements greater than A[i] is n - i - 1
        if (A[i] == n - i - 1) {
            return 1;
        }
    }

    return -1;
}

// Example usage
console.log(findNobleInteger([3, 2, 1, 3])); // Output: 1
console.log(findNobleInteger([1, 1, 3, 3])); // Output: -1
```