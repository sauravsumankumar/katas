202207252137
Name: **Sum Arrays**
Link: [Codewars](https://www.codewars.com/kata/53dc54212259ed3d4f00071c)
Level:  [[8 kyu]]
Tags: [[Arrays]] [[Fundamentals]]

---

# Sum Arrays

Write a function that takes an array of numbers and returns the sum of the numbers. The numbers can be negative or non-integer. If the array does not contain any numbers then you should return 0.

**Example**:
``` javascript
Input: `[1, 5.2, 4, 0, -1]`  
Output: `9.2`

Input: `[]`  
Output: `0`

Input: `[-2.398]`  
Output: `-2.398`
```


---

## Solution

``` javascript
sum=a=>a.reduce((acc,cur)=>acc+cur,0)
```