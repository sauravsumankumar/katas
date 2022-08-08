Name: **Multiplication table**
Link: [Codewars](https://www.codewars.com/kata/534d2f5b5371ecf8d2000a08)
Level:  [[6 kyu]]
Tags: [[Arrays]] [[Fundamentals]]

---

# Multiplication table

Your task, is to create `NxN` multiplication table, of size provided in parameter.

**Example**:

```js
1 2 3
2 4 6
3 6 9
```

Output: 

``` js
[[1,2,3],[2,4,6],[3,6,9]]
```


---

## Solution

``` javascript
multiplicationTable = size => {
  let table = []
    for(let row=1; row <= size ; row++){
      let block = []
      for(let column=1; column<=size; column++){
          block.push(row*column)
      }
      table.push(block)
    }
  return table
}
```