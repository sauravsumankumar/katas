202207252236
Name: **Sum of Minimuns!**
Link: [Codewars](https://www.codewars.com/kata/5d5ee4c35162d9001af7d699)
Level:  [[7 kyu]]
Tags: [[Fundamentals]] [[Arrays]]

---

# Sum of Minimums!

Given a 2D ( nested ) list ( array, vector, .. ) of size `m * n`, your task is to find the sum of the minimum values in each row.

**Example**:

```javascript
[ [ 1, 2, 3, 4, 5 ]        #  minimum value of row is 1
, [ 5, 6, 7, 8, 9 ]        #  minimum value of row is 5
, [ 20, 21, 34, 56, 100 ]  #  minimum value of row is 20
]
```

So the function should return `26` because the sum of the minimums is `1 + 5 + 20 = 26`.

**Note**: You will always be given a non-empty list containing positive values.


---

## Solution

``` javascript
sumOfMinimums=arr=>[...arr].map((e)=>e.sort((a,b)=>a-b).slice(0,1).reduce((acc,cur)=>+acc+cur)).reduce((acc,cur)=>acc+cur)
```