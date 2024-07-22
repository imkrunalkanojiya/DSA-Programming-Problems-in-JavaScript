# Longest Palindromic Substring

## Problem Description
Given a string A of size N, find and return the longest palindromic substring in A.

Substring of string A is A[i...j] where 0 <= i <= j < len(A)

Palindrome string:
A string which reads the same backwards. More formally, A is palindrome if reverse(A) = A.

Incase of conflict, return the substring which occurs first ( with the least starting index).

### Problem Constraints
````
1 <= N <= 6000
````

### Input Format
````
First and only argument is a string A.
````

### Output Format
````
Return a string denoting the longest palindromic substring of string A.
````

### Example Input
````
Input 1:
A = "aaaabaaa"

Input 2:
A = "abba"
````

### Example Output
````
Output 1:
"aaabaaa"

Output 2:
"abba"
````

### Example Explanation
````
Explanation 1:
We can see that longest palindromic substring is of length 7 and the string is "aaabaaa".

Explanation 2:
We can see that longest palindromic substring is of length 4 and the string is "abba".
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function longestPalindromicSubstring(A){
    let maxPalindrone = 1;
    let start = 0;
    let end = 1;

    // for each character in A, check if it is the center of a palindrome of odd length
    for (let i = 1; i < A.length - 1; i++) {
        let length = 0;
        let s = i - 1;
        let e = i + 1;

        // check if the character is the center of a palindrome of odd length
        // and expand the palindrome to the left and right as long as the characters match
        while (s >= 0 && e < A.length && A[s] === A[e]) {
            length += 2;
            s--;
            e++;
        }

        // if the length of the palindrome is greater than the current max, update the max
        if (maxPalindrone < length) {
            maxPalindrone = length;
            start = s + 1;
            end = e;
        }
    }

    // for each character in A, check if it is the center of a palindrome of even length
    for (let i = 0; i < A.length - 1; i++) {

        // check if the character is the center of a palindrome of even length
        if (A[i] === A[i + 1]) {
            let length = 2;
            let s = i - 1;
            let e = i + 2;

            // expand the palindrome to the left and right as long as the characters match
            while (s >= 0 && e < A.length && A[s] === A[e]) {
                length += 2;
                s--;
                e++;
            }

            // if the length of the palindrome is greater than the current max, update the max
            if (maxPalindrone < length) {
                maxPalindrone = length;
                start = s + 1;
                end = e;
            }
        }
    }

    return A.slice(start, end);
}
```