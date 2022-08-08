202208082103
Name: **Twisted Sum**
Link: [Codewars](https://www.codewars.com/kata/527e4141bb2ea5ea4f00072f)
Level:  [[6 kyu]]
Tags: [[Mathematics]] [[Algorithms]]

---

# Twisted Sum

Find the sum of the digits of all the numbers from `1` to `N` (both ends included).

**Examples**:

``` js
# N = 4
1 + 2 + 3 + 4 = 10

# N = 10
1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + (1 + 0) = 46

# N = 12
1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + (1 + 0) + (1 + 1) + (1 + 2) = 51
```

---

## Solution

``` javascript
const twistedSum = n =>{
  let array = []
  
  for (let i=1; i<=n; i++){
    if (i>9) array.push(`${i}`.split('').reduce((acc,cur)=>+acc+ +cur))
    if (i<=9) array.push(i)
  }
  return array.reduce((acc,cur)=>acc+cur,0)
}
```


```