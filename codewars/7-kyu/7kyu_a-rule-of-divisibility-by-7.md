202208082120
Name: **A Rule of Divisibilty by 7**
Link: [Codewars](https://www.codewars.com/kata/55e6f5e58f7817808e00002e)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Rule of Divisibility by 7

Your task is to return to the function `seven(m)` (m integer >= 0) an array (or a pair, depending on the language) of numbers, the first being the _last_ number `m` with at most 2 digits obtained by your function (this last `m` will be divisible or not by 7), the second one being the number of steps to get the result.

**Example**:

``` js
seven(371) should return [35, 1]
seven(1603) should return [7, 2]
seven(477557101) should return [28, 7]
```

---

## Solution

``` javascript
const seven = n => {
  let counter = 0
  while (n.toString().length > 2){
    counter++
    n = Math.floor(n / 10) - (n % 10) * 2
  }
  return [n, counter]
}
```