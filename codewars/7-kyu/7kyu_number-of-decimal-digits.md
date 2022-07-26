202207261108
Name: **Number of Decimal Digits**
Link: [Codewars](https://www.codewars.com/kata/58fa273ca6d84c158e000052/)
Level:  [[7 kyu]]
Tags: [[Strings]] [[Fundamentals]]

---

# Number of Decimal Digits

Determine the total number of digits in the integer (`n>=0`) given as input to the function. For example, 9 is a single digit, 66 has 2 digits and 128685 has 6 digits. Be careful to avoid overflows / under flows.

All inputs will be valid.

---

## Solution 1

``` javascript
function digits(n) {
  if (!Number.isInteger(n)) return 'Fail!'  
  const decimals = `${n}`.length
  return decimals
}
```

## Solution 2

``` javascript
digits=n=>`${n}`.length
```