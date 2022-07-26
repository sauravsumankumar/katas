202207261043
Name: **Predict your age!**
Link: [Codewars](https://www.codewars.com/kata/5aff237c578a14752d0035ae)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Predict your age!

My grandfather always predicted how old people would get, and right before he passed away he revealed his secret!

In honour of my grandfather's memory we will write a function using his formula!

-   Take a list of ages when each of your great-grandparent died.
-   Multiply each number by itself.
-   Add them all together.
-   Take the square root of the result.
-   Divide by two.

**Example**:

```javascript
predictAge(65, 60, 75, 55, 60, 63, 64, 45) === 86
```


---

## Solution

``` javascript
predictAge=(n1,n2,n3,n4,n5,n6,n7,n8)=>{
  let ages = [n1,n2,n3,n4,n5,n6,n7,n8]
  let totalSumAges = ages.map(e=>e**2).reduce((a,b)=>a+b,0)
  return Math.floor(Math.sqrt(totalSumAges)/2)
}
```