202207252243
Name: **Leap Years**
Link: [Codewars](https://www.codewars.com/kata/526c7363236867513f0005ca)
Level:  [[7 kyu]]
Tags: [[Date Time]] [[Algorithms]]

---

# Leap Years

In this kata you should simply determine, whether a given year is a leap year or not. In case you don't know the rules, here they are:

1.  Years divisible by 4 are leap years
2.  Years divisible by 100 are **not** leap years
3.  Years divisible by 400 are leap years

**Notes**:

Only valid years (positive integers) will be tested, so you don't have to validate them

Examples can be found in the test fixture.

---

## Solution

``` javascript
isLeapYear=year=>(year % 100 !== 0 && year % 4 === 0) || year % 400 === 0
```