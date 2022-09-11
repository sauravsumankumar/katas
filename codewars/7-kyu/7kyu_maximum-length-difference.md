202209111805
Name: **Maximum Length Difference**
Link: [Codewars](https://www.codewars.com/kata/5663f5305102699bad000056)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Maximum Length Difference

You are given two arrays `a1` and `a2` of strings. Each string is composed with letters from `a` to `z`. Let `x` be any string in the first array and `y` be any string in the second array.

`Find max(abs(length(x) − length(y)))`

If `a1` and/or `a2` are empty return `-1` in each language except in Haskell (F#) where you will return `Nothing` (None).

**Example**

```js
a1 = ["hoqq", "bbllkw", "oox", "ejjuyyy", "plmiis", "xxxzgpsssa", "xxwwkktt", "znnnnfqknaz", "qqquuhii", "dvvvwz"]
a2 = ["cccooommaaqqoxii", "gggqaffhhh", "tttoowwwmmww"]
mxdiflg(a1, a2) --> 13
```

---

## Solution

``` js
const mxdiflg=(a1,a2)=>{
  if (a1.length === 0 || a2.length === 0) return -1
  
  let arrLengthsA1 = [],
      arrLengthsA2 = []
  
  a1.sort((a,b)=>b.length-a.length).map((e,i)=>arrLengthsA1.push(e.length))
  a2.sort((a,b)=>b.length-a.length).map((e,i)=>arrLengthsA2.push(e.length))
  
  const arrDifferenceA2 = arrLengthsA2[0] - arrLengthsA1[arrLengthsA1.length-1],
        arrDifferenceA1 = arrLengthsA1[0] - arrLengthsA2[arrLengthsA2.length-1]
  
  return arrDifferenceA2 > arrDifferenceA1 ? arrDifferenceA2 : 
         arrDifferenceA1 > arrDifferenceA2 ? arrDifferenceA1 : 
         arrDifferenceA1
  }

```

## Solution2

```js
const mxdiflg=(a1,a2)=>{
  if (a1.length === 0 || a2.length === 0) return -1
  
  a1.sort((a,b)=>b.length-a.length)
  a2.sort((a,b)=>b.length-a.length)
  
  let arrLengthsA1 = [],
      arrLengthsA2 = []
  a1.map((e,i)=>arrLengthsA1.push(e.length))a2.map((e,i)=>arrLengthsA2.push(e.length))
  
  const arrDifferenceA2 = arrLengthsA2[0] - arrLengthsA1[arrLengthsA1.length-1],
        arrDifferenceA1 = arrLengthsA1[0] - arrLengthsA2[arrLengthsA2.length-1]
  
  if (arrDifferenceA2 > arrDifferenceA1) return arrDifferenceA2
  if (arrDifferenceA1 > arrDifferenceA2) return arrDifferenceA1
  if (arrDifferenceA2 === arrDifferenceA1) return arrDifferenceA1
  }
```