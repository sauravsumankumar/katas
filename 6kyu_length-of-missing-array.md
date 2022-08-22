202208222150
Name: **Length of missing array**
Link: [Codewars](https://www.codewars.com/kata/57b6f5aadb5b3d0ae3000611)
Level:  [[6 kyu]]
Tags: [[Arrays]] [[Algorithms]]

---

# Length of missing array

You get an array of arrays.  
If you sort the arrays by their length, you will see, that their length-values are consecutive.  
But one array is missing!  
  
You have to write a method, that return the length of the missing array.

**Example**:

``` javascript
[[1, 2], [4, 5, 1, 1], [1], [5, 6, 7, 8, 9]] --> 3
```

---

## Solution

``` javascript
const getLengthOfMissingArray = (arr) => {
  const lengths = (arr || [])
    .map(a => a ? a.length : 0)
    .sort((a, b) => a - b);
  
  if (lengths.includes(0)) return 0

  for (let i = 0; i < lengths.length - 1; i++) {
    if (lengths[i] + 1 !== lengths[i + 1]) return lengths[i] + 1
  }
  return 0
}
```