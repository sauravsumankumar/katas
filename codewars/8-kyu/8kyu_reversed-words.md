202209111810
Name: **Reversed Words**
Link: [Codewars](https://www.codewars.com/kata/51c8991dee245d7ddf00000e/)
Level:  [[8 kyu]]
Tags: [[Strings]] [[Algorithms]]

---

# Reversed Words

Complete the solution so that it reverses all of the words within the string passed in.

**Example**

``` js
"The greatest victory is that which requires no battle" --> "battle no requires which that is victory greatest The"
```
---

## Solution

``` javascript
const reverseWords = str => str.split(' ').reverse().join(` `);
```