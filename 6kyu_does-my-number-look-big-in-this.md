202209111826
Name: **Does my number look big in this?**
Link: [Codewars](https://www.codewars.com/kata/5287e858c6b5a9678200083c/)
Level:  [[6 kyu]]
Tags: [[Algorithms]]

---

# Does my number look big in this?

A [Narcissistic Number](https://en.wikipedia.org/wiki/Narcissistic_number) is a positive number which is the sum of its own digits, each raised to the power of the number of digits in a given base. In this Kata, we will restrict ourselves to decimal (base 10).

For example, take 153 (3 digits), which is narcisstic:

```
    1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153
```

and 1652 (4 digits), which isn't:

```
    1^4 + 6^4 + 5^4 + 2^4 = 1 + 1296 + 625 + 16 = 1938
```

The Challenge:

Your code must return **true** or **false** (not 'true' and 'false') depending upon whether the given number is a Narcissistic number in base 10. This may be **True** and **False** in your language, e.g. PHP.

Error checking for text strings or other invalid inputs is not required, only valid positive non-zero integers will be passed into the function.

---

## Solution 1

``` javascript
const narcissistic=n=>{
  const toDigits = `${n}`.split('').map(e=>+e),
        digitsNum = toDigits.length,
        sumOfDigits = toDigits
                         .map(e=>e**digitsNum)
                         .reduce((cur,acc)=>cur+acc,0)
  return sumOfDigits === n
}
```


## Solution 2

``` javascript
const narcissistic=(n)=>{
  const toNumbers = `${n}`.split('').map(e=>+e)
  const numLenghts = toNumbers.length
  const result = toNumbers.map(e=>e**numLenghts).reduce((cur,acc)=>cur+acc,0)
  return result === n
}
```
