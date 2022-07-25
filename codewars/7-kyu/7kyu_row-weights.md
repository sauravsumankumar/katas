202207252230
Name: **Row Weights**
Link: [Codewars](https://www.codewars.com/kata/5abd66a5ccfd1130b30000a9)
Level:  [[7 kyu]]
Tags: [[Fundamentals]] [[Arrays]]

---

# Row Weights

**_Given_** _an array of positive integers (the weights of the people)_, **_return_** _a new array/tuple of two integers_, **_where_** **_the first_** one is the **_total weight of team 1_**, and **_the second_** one is the **_total weight of team 2_**.

## Notes

 **_Array size_** is _at least 1_.
 **_All numbers_** will be **positive**.

**Examples**:

``` javascript
rowWeights([13, 27, 49])  ==>  return (62, 27)
```

---

## Solution 1

``` javascript
function rowWeights(arr){
  const odd = arr.filter((e,i)=>i%2!==0).reduce((acc, cur)=>acc+cur,0)
  const even = arr.filter((e,i)=>i%2===0).reduce((acc, cur)=>acc+cur,0)
  return [even, odd]
}
```

## Solution 2

``` javascript
function rowWeights(arr){
  let odd = [], even = []
  arr.map((e,i)=>i%2?even.push(e):odd.push(e))
  odd=odd.reduce((acc, cur)=>acc+cur,0)
  even=even.reduce((acc,cur)=>acc+cur,0)
  return [odd, even]
}
```