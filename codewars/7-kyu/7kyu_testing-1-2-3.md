202207261046
Name: **Testing 1-2-3**
Link: [Codewars](https://www.codewars.com/kata/54bf85e3d5b56c7a05000cf9)
Level:  [[7 kyu]]
Tags: [[Arrays]] [[Fundamentals]]

---

# Testing 1-2-3

Your team is writing a fancy new text editor and you've been tasked with implementing the line numbering.

Write a function which takes a list of strings and returns each line prepended by the correct number.

The numbering starts at 1. The format is `n: string`. Notice the colon and space in between.

**Examples**:

``` javascript
[] --> []
["a", "b", "c"] --> ["1: a", "2: b", "3: c"]
```


---

## Solution

``` javascript
const number=arr=>{
  let result = []
  arr.map((e,i,a)=>{`${result.push((i+1) + ': '+ e)}`, 0})
  return result
}
```