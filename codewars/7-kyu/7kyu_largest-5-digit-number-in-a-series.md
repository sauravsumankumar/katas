202209111816
Name: **Largest 5 digit number in a series**
Link: [Codewars](https://codewars.com/kata/51675d17e0c1bed195000001)
Level: [[7 kyu]]
Tags: [[Algorithms]]

---

# Largest 5 digit number in a series

In the following 6 digit number:

```
283910
```

`91` is the greatest sequence of 2 consecutive digits.

In the following 10 digit number:

```
1234567890
```

`67890` is the greatest sequence of 5 consecutive digits.

Complete the solution so that it returns the greatest sequence of five consecutive digits found within the number given. The number will be passed in as a string of only digits. It should return a five digit integer. The number passed may be as large as 1000 digits.

_Adapted from ProjectEuler.net

---

## Solution

``` js
solution=(s)=>+`${s}`.split('').map((e,i,a)=>a.slice(i,i+5).join('')).sort((a,b)=>b-a).slice(0,1)
```