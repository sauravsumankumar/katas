202207252111
Name: **Sum of the first nth term of Series**
Link: [Codewars]()
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Sum of the first nth term of Series

Your task is to write a function which returns the sum of following series up to nth term(parameter).

``` javascript
Series: 1 + 1/4 + 1/7 + 1/10 + 1/13 + 1/16 +...
```

---

## Solution

``` javascript
SeriesSum=n=>{
  let result = 0
  for(let i=0; i<n; i++){
    result += 1 / (1+i*3)
  }
  return  result.toFixed(2)
}
```