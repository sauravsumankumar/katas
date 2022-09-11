202209111751
Name: **Make the Deadfish Swim**
Link: [Codewars](https://www.codewars.com/kata/51e0007c1f9378fa810002a9)
Level:  [[6 kyu]]]
Tags: [[Parsing]] [[Algorithms]]

---

# Make the Deadfish Swim

Write a simple parser that will parse and run Deadfish.

Deadfish has 4 commands, each 1 character long:

-   `i` increments the value (initially `0`)
-   `d` decrements the value
-   `s` squares the value
-   `o` outputs the value into the return array

Invalid characters should be ignored.

**Example**

```js 
parse("iiisdoso") => [ 8, 64 ]
```

---

## Solution 1

``` javascript
const parse=(data)=>{
  let result = []
  
  data.split('').reduce((cur, idx)=>{
    if (idx === 'i') cur++
    if (idx === 'd') cur--
    if (idx === 's') cur = cur**2
    if (idx === 'o') result.push(cur)
    return cur
  }, 0)
  
  return result
}
```

## Solution 2

``` javascript
const parse=(data)=>{
  let result = 0,
      resultArr = []
  
  data.split('').map(e=>{
    if (e === 'i') result++
    if (e === 'd') result--
    if (e === 's') result = result**2
    if (e === 'o') resultArr.push(result)
  })
  
  return resultArr
}
```