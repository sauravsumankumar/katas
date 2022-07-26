202207261029
Name: **Largest pair sum in array**
Link: [Codewars](https://www.codewars.com/kata/556196a6091a7e7f58000018)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Largest pair sum in array

Given a sequence of numbers, find the largest pair sum in the sequence.

**Example**:

``` javascript
[10, 14, 2, 23, 19] -->  42 (= 23 + 19)
[99, 2, 2, 23, 19]  --> 122 (= 99 + 23)
```

Input sequence contains minimum two elements and every element is an integer.

---

## Solution

``` javascript
largestPairSum=arr=>arr.sort((a,b)=>b-a).slice(0,2).reduce((acc,cur)=>acc+cur)
```