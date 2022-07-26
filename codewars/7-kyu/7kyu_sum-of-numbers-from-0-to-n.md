202207261033
Name: **Sum of numbers from 0 to N**
Link: [Codewars](https://www.codewars.com/kata/56e9e4f516bcaa8d4f001763)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Sum of numbers from 0 to N

We want to generate a function that computes the series starting from 0 and ending until the given number.

**Example**:

``` javascript
Input:
> 6

Output:
"0+1+2+3+4+5+6 = 21"
```

---

## Solution

``` javascript
const SequenceSum = () => {
  function SequenceSum() {}

  SequenceSum.showSequence=count=>{
    let numbers = []
    for(let i=0; i<=count; i++){
      numbers.push(i)
    }
    if(count < 0) return `${count}<0`
    if(count === 0) return `${count}=0`
    return numbers.join('+') + ' = ' + numbers.reduce((a,b)=>a+b,0)
  };
  return SequenceSum;
})();
```
