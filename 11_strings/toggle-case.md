# Toggle Case

## Problem Description
You are given a character string A having length N, consisting of only lowercase and uppercase latin letters.

You have to toggle case of each character of string A. For e.g 'A' is changed to 'a', 'e' is changed to 'E', etc.

### Problem Constraints
````
1 <= N <= 10^5
A[i] ∈ ['a'-'z', 'A'-'Z']
````

### Input Format
````
First and only argument is a character string A.
````

### Output Format
````
Return a character string.
````

### Example Input
````
Input 1:
A = "Hello" 

Input 2:
A = "tHiSiSaStRiNg"
````

### Example Output
````
Output 1:
hELLO

Output 2:
ThIsIsAsTrInG 
````

### Example Explanation
````
Explanation 1:
'H' changes to 'h'
'e' changes to 'E'
'l' changes to 'L'
'l' changes to 'L'
'o' changes to 'O'

Explanation 2:
"tHiSiSaStRiNg" changes to "ThIsIsAsTrInG".
````

### Output

``` javascript showLineNumbers copy filename="JavaScript"
function toggleCase(A){
        let newA = ""
        for(let i = 0 ; i < A.length ; i++){
            if(A[i] >= "A" && A[i] <= "Z"){
                newA += String.fromCharCode(A[i].charCodeAt(0) ^ 32)
            }else{
                newA += String.fromCharCode(A[i].charCodeAt(0) ^ 32)
            }
        }
        return newA
}
```