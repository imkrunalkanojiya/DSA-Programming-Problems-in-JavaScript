# Factors sort

## Problem Description
You are given an array A of N elements. Sort the given array in increasing order of number of distinct factors of each element, i.e., element having the least number of factors should be the first to be displayed and the number having highest number of factors should be the last one. If 2 elements have same number of factors, then number with less value should come first.

Note: You cannot use any extra space
### Problem Constraints
````
1 <= N <= 10^4
1 <= A[i] <= 10^4
````

### Input Format
````
First argument A is an array of integers.
````

### Output Format
````
Return an array of integers.
````

### Example Input
````
Input 1:
A = [6, 8, 9]

Input 2:
A = [2, 4, 7]
````

### Example Output
````
Output 1:
[9, 6, 8]

Output 2:
[2, 7, 4]
````

### Example Explanation
````
Explanation 1:
The number 9 has 3 factors, 6 has 4 factors and 8 has 4 factors.

Explanation 2:
The number 2 has 2 factors, 7 has 2 factors and 4 has 3 factors.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
// Function to count the number of distinct factors of a given number
function countFactors(num) {
    let count = 0;
    for (let i = 1; i * i <= num; i++) {
        if (num % i === 0) {
            if (i * i === num) {
                count += 1;
            } else {
                count += 2;
            }
        }
    }
    return count;
}

function factorsSort(A) {
    // Sort the array based on the number of factors
    A.sort((a, b) => {
        let factorsA = countFactors(a);
        let factorsB = countFactors(b);
        
        if (factorsA === factorsB) {
            return a - b; // Sort by value if the number of factors is the same
        } else {
            return factorsA - factorsB; // Sort by number of factors
        }
    });

    return A;
}

// Example usage
console.log(factorsSort([6, 8, 9])); // Output: [9, 6, 8]
console.log(factorsSort([2, 4, 7])); // Output: [2, 7, 4]
```