202207261039
Name: **Sort the Gift Code**
Link: [Codewars](https://www.codewars.com/kata/52aeb2f3ad0e952f560005d3)
Level:  [[7 kyu]]
Tags: [[Sorting]] [[Strings]] [[Fundamentals]]
 
---

# Sort the Gift Code

Write a function called `sortGiftCode`/`sort_gift_code`/`SortGiftCode` that accepts a string containing up to 26 unique alphabetical characters, and returns a string containing the same characters in alphabetical order.

``` javascript
"abcdef"                      -- => "abcdef"
"pqksuvy"                     -- => "kpqsuvy"
"zyxwvutsrqponmlkjihgfedcba"  -- => "abcdefghijklmnopqrstuvwxyz"
```
---

## Solution

``` javascript
sortGiftCode=s=>s.split('').map(e=>e.charCodeAt()).sort((a,b)=>a-b).map(e=>String.fromCharCode(e)).join('')
```