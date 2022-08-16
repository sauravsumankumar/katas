202208161728
Name: **Count the Digit**
Link: [Codewars](https://www.codewars.com/kata/566fc12495810954b1000030)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Count the Digit

Take an integer `n (n >= 0)` and a digit `d (0 <= d <= 9)` as an integer.
Square all numbers `k (0 <= k <= n)` between 0 and n.
Count the numbers of digits `d` used in the writing of all the `k**2`.
Call `nb_dig` (or `nbDig` or ...) the function taking `n` and `d` as parameters and returning this count.

**Examples**:

```js
n = 10, d = 1 
the k*k are 0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100
We are using the digit 1 in: 1, 16, 81, 100. The total count is then 4.

nb_dig(25, 1) returns 11 since
the k*k that contain the digit 1 are:
1, 16, 81, 100, 121, 144, 169, 196, 361, 441.
So there are 11 digits 1 for the squares of numbers between 0 and 25.
```

---

## Solution1

``` javascript
function nbDig(n, d) {
  if (n < 0 || d < 0) return 
  if (d > 9) return 
  
  let numsArr = [], numberOfDigits = 0
  for(let i=0; i <= n; i++) numsArr.push(i**2)

  const findDigits = numsArr
  .map(e=>`${e}`.split('')
       .map(n=>+n===d&&numberOfDigits++))
  return numberOfDigits
}
```

## Solution2

``` javascript
function nbDig(n, d) {
  if (n < 0 || d < 0) return 
  if (d > 9) return 
  
  let numsArr = [], numberOfDigits = 0
  for(let i=0; i <= n; i++) numsArr.push(i)
  
  const square = numsArr.map(e=>e**2)
  const findDigits = square
          .map(e=>`${e}`.split('')     .map(n=>+n===d&&numberOfDigits++))
  return numberOfDigits
}
```