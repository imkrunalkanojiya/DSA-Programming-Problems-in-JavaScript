# toupper()

## Problem Description
You are given a function to_upper() consisting of a character array A.

Convert each character of A into Uppercase character if it exists. If the Uppercase of a character does not exist, it remains unmodified.
The lowercase letters from a to z is converted to uppercase letters from A to Z respectively.

Return the uppercase version of the given character array.

### Problem Constraints
````
1 <= |A| <= 10^5
````

### Input Format
````
The only argument is a character array A.
````

### Output Format
````
Return the uppercase version of the given character array.
````

### Example Input
````
Input 1:
A = ['S', 'c', 'A', 'L', 'E', 'r', 'A', 'c', 'a', 'D', 'e', 'm', 'y']

Input 2:
A = ['S', 'c', 'a', 'L', 'e', 'R', '#', '2', '0', '2', '0']
````

### Example Output
````
Output 1:
['S', 'C', 'A', 'L', 'E', 'R', 'A', 'C', 'A', 'D', 'E', 'M', 'Y']

Output 2:
['S', 'C', 'A', 'L', 'E', 'R', '#', '2', '0', '2', '0']
````

### Example Explanation
````
Explanation 1:
All the characters in the returned array are in uppercase alphabets.

Explanation 2:
Since there is no Uppercase version for '#', '2'and '0'.  It remains unchanged. Rest of the Lowercase alphabets are converted to Uppercase accordingly.
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function toUppercase(A){
        for(let i = 0 ; i < A.length ; i++){
            if(A[i] >= "a" && A[i] <= "z"){
                A[i] = String.fromCharCode(A[i].charCodeAt(0) ^ 32)
            }
        }
        return A
}
```