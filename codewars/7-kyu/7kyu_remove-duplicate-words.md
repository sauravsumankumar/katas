202207252129
Name: **Remove duplicate words**
Link: [Codewars](https://www.codewars.com/kata/5b39e3772ae7545f650000fc)
Level:  [[7 kyu]]
Tags: [[Strings]] [[Regular Expressions]] [[Algorithms]]
 
---

# Remove duplicate words

Your task is to remove all duplicate words from a string, leaving only single (first) words entries.

**Example**:

``` javascript
// Input:

'alpha beta beta gamma gamma gamma delta alpha beta beta gamma gamma gamma delta'

// Output:

'alpha beta gamma delta'

```


---

## Solution

``` javascript
removeDuplicateWords=s=>[...new Set(s.split(" "))].join(" ");
```