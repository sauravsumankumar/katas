202208222209
Name: **Are they the "same"?**
Link: [Codewars](https://www.codewars.com/kata/550498447451fbbd7600041c)
Level:  [[6 kyu]]
Tags: [[Fundamentals]]

---

# Are they the "same"?

Given two arrays `a` and `b` write a function `comp(a, b)` (or`compSame(a, b)`) that checks whether the two arrays have the "same" elements, with the same _multiplicities_ (the multiplicity of a member is the number of times it appears). "Same" means, here, that the elements in `b` are the elements in `a` squared, regardless of the order.

**Example**:

```javascript
a = [121, 144, 19, 161, 19, 144, 19, 11]  
b = [121, 14641, 20736, 361, 25921, 361, 20736, 361]
```

---

## Solution1

``` javascript
const comp=(arr1, arr2)=>{
  if(!arr1 || !arr2) return false
  const original = arr1.sort((a,b)=>a-b)
  const aimed = arr2.sort((a,b)=>a-b).map(e=>Math.sqrt(e)*-1)
  const findDifference = () => -original.reduce((a,b)=>a+b,0) === aimed.reduce((a,b)=>a+b,0)
  return findDifference()
}
```


## Solution2

``` javascript
const comp = (arr1,arr2) => {
  if (!arr1 || !arr2) return false
  
  const original = arr1.sort((a,b)=>a-b),
        aimed = arr2.sort((a,b)=>a-b).map(e=>Math.sqrt(e)*-1),
        findDifference = () => -original.reduce((a,b)=>a+b,0) === aimed.reduce((a,b)=>a+b,0)
  
  return findDifference()
}
```