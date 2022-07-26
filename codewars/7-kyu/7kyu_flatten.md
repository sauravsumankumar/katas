202207261115
Name: **Flatten**
Link: [Codewars]()
Level:  [[7 kyu]]
Tags: [[Functional-programming]] [[Arrays]] [[Fundamentals]]

---

# Flatten

Write a function that flattens an `Array` of `Array` objects into a flat `Array`. Your function must only do one level of flattening.

``` javascript
flatten([1,2,3]) // => [1,2,3]
flatten([[1,2,3],["a","b","c"],[1,2,3]])  // => [1,2,3,"a","b","c",1,2,3]
flatten([[[1,2,3]]]) // => [[1,2,3]]
```


---

## Solution

``` javascript
const flatten = arr => arr.reduce((cur, acc)=>cur.concat(acc), [])
```