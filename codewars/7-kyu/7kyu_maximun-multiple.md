202207252058
Name:  **Maximum Multiple**
Link: [Codewars](https://www.codewars.com/kata/5aba780a6a176b029800041c/)
Level:  [[7 kyu]]
Tags: [[Fundamentals]] [[Arrays]]

---

# Maximum Multiple

**_Given_** a **_Divisor and a Bound_** , _Find the largest integer N_ , Such That ,

**_N_** is _divisible by divisor_    
**_N_** is _less than or equal to bound_
**_N_** is _greater than 0_.

**Example**:

``` javascript
maxMultiple (2,7) ==> return (6)
```

---

## Solution

``` javascript
const maxMultiple = (divisor, bound) => {
  let result
  for(let i=0; i <= bound; i++){
    if (i % divisor === 0) result = i
  }
  return result
}
```